---
title: '[DL-Tutorial] Deep Energy-Based Generative Models'
date: 2022-11-28
permalink: /posts/2022/11/28/deep-energy-based-generative-models/
tags:
  - Research
  - Deep Learning Tutorial
---

> Original Tutorial: https://uvadlc-notebooks.readthedocs.io/en/latest/tutorial_notebooks/tutorial8/Deep_Energy_Models.html#Energy-Models

In this tutorial, we will look at energy-based deep learning models, and focus on their application as generative models. Energy models have been a popular tool before the huge deep learning hype around 2012 hit. However, in recent years, energy-based models have gained increasing attention because of improved training methods and tricks being proposed. Although they are still in a research stage, they have shown to outperform strong Generative Adversarial Networks (Lecture/Tutorial 10) in certain cases which have been the state of the art of generating images (blog post about strong energy-based models, blog post about the power of GANs). Hence, it is important to be aware of energy-based models, and as the theory can be abstract sometimes, we will show the idea of energy-based models with a lot of examples.

First, let’s import our standard libraries below.

# Energy Models

In the first part of this tutorial, we will review the theory of the energy-based models. While most of the previous models had the goal of classification or regression, energy-based models are motivated from a different perspective: **density estimation**. Given a dataset with a lot of elements, we want to estimate the probability distribution over the whole data space. As an example, if we model images from CIFAR10, our goal would be to have a probability distribution over all possible images of size $32 \times 32 \times 3$ where those images have a high likelihood that look realistic and are one of the 10 CIFAR classes. Simple methods like interpolation between images don’t work because images are extremely high-dimensional (especially for large HD images). Hence, we turn to deep learning methods that have performed well on complex data.

However, how do we predict a probability distribution $p(\mathbf{x})$ over so many dimensions using a simple neural network? The problem is that we cannot just predict a score between 0 and 1, because a probability distribution over data needs to fulfill two properties:
1. The probability distribution needs to assign any possible value of $\mathbf{x}$ a non-negative value: $p(\mathbf{x}) \geq 0$.
2. The probability density must sum/integrate to 1 over **all** possible inputs: $\int_{\mathbf{x}} p(\mathbf{x}) d\mathbf{x} = 1$.

Luckily, there are actually many approaches for this, and one of them are energy-based models. The fundamental idea of energy-based models is that you can turn any function that predicts values larger than zero into a probability distribution by dviding by its volume. Imagine we have a neural network, which has as output a single neuron, like in regression. We can call this network $E_{\theta}(\mathbf{x})$, where $\theta$ are our parameters of the network, and $\mathbf{x}$ the input data (e.g. an image). The output of $E_{\theta}$ is a scalar value between $-\infty$ and $\infty$. Now, we can use basic probability theory to *normalize* the scores of all possible inputs:

$$
q_{\theta}(\mathbf{x}) = \frac{\exp\left(-E_{\theta}(\mathbf{x})\right)}{Z_{\theta}} \hspace{5mm}\text{where}\hspace{5mm} 
Z_{\theta} = \begin{cases}\int_{\mathbf{x}} \exp \left(-E_\theta(\mathbf{x})\right) d \mathbf{x} & \text { if } x \text { is continuous } \\ \sum_{\mathbf{x}} \exp \left(-E_\theta(\mathbf{x})\right) & \text { if } x \text { is discrete }\end{cases}
$$


The $\exp$-function ensures that we assign a probability greater than zero to any possible input. We use a negative sign in front of $E$ because we call $E_{\theta}$ to be the energy function: **data points with high likelihood have a low energy**, while data points with low likelihood have a high energy. $Z_{\theta}$ is our normalization terms that ensures that the density integrates/sums to 1. We can show this by integrating over $q_{\theta}(\mathbf{x})$:

$$
\int_{\mathbf{x}} q_\theta(\mathbf{x}) d \mathbf{x}=\int_{\mathbf{x}} \frac{\exp \left(-E_\theta(\mathbf{x})\right)}{\int_{\tilde{\mathbf{x}}} \exp \left(-E_\theta(\tilde{\mathbf{x}})\right) d \tilde{\mathbf{x}}} d \mathbf{x}=\frac{\int_{\mathbf{x}} \exp \left(-E_\theta(\mathbf{x})\right) d \mathbf{x}}{\int_{\tilde{\mathbf{x}}} \exp \left(-E_\theta(\tilde{\mathbf{x}})\right) d \tilde{\mathbf{x}}}=1
$$

Note that we call the probability distribution $q_{\theta}(\mathbf{x})$ because this is the learned distribution by the model, and is trained to be as close as possible to the *true*, unknown distribution $p(\mathbf{x})$, i.e. **estimating $p_\theta(\mathbf{x})$ using a network**. The main benefit of this formulation of the probability distribution is its great **flexibility** as we can choose $E_{\theta}$ in whatever way we like, without any constraints.

Nevertheless, when looking at the equation above, we can see a fundamental issue: **How do we calculate $Z_{\theta}$?** There is no chance that we can calculate $Z_{\theta}$ analytically for high-dimensional input and/or larger neural networks, but the task requires us to know $Z_{\theta}$. Although we can't determine the exact likelihood of a point, there exist methods with which we can train energy-based models. Thus, we will look next at "Contrastive Divergence" for training the model.

# Contrastive Divergence

When we train a model on generative modeling, it is usually done by maximum likelihood estimation (MLE). In other words, we try to **maximize the likelihood of the examples in the training set**. As the exact likelihood of a point cannot be determined due to the unknown normalization constant $Z_{\theta}$, we need to train energy-based models slightly different. We **cannot just maximize the un-normalized probability $\exp(-E_{\theta}(\mathbf{x}_{\text{train}}))$** because there is no guarantee that $Z_{\theta}$ stays constant, or that $\mathbf{x}_{\text{train}}$ is becoming more likely than the others. However, if we base our training on comparing the likelihood of points, we can create a stable objective. Namely, we can re-write our maximum likelihood objective where we maximize the probability of $\mathbf{x}_{\text{train}}$ compared to a randomly sampled data point of our model:

$$
\begin{split}
\nabla_{\theta}\mathcal{L}_{\text{MLE}}(\mathbf{\theta};p) & = -\mathbb{E}_{p(\mathbf{x})}\left[\nabla_{\theta}\log q_{\theta}(\mathbf{x})\right]\\
& = \mathbb{E}_{p(\mathbf{x})}\left[\nabla_{\theta}E_{\theta}(\mathbf{x})\right] - \mathbb{E}_{q_{\theta}(\mathbf{x})}\left[\nabla_{\theta}E_{\theta}(\mathbf{x})\right]
\end{split}
$$

Note that the loss is still an objective we want to minimize. Thus, we try to minimize the energy for data points from the dataset, while maximizing the energy for randomly sampled data points from our model (how we sample will be explained below). Although this objective sounds intuitive, how is it actually derived from our original distribution $q_{\theta}(\mathbf{x})$? The trick is that we approximate $Z_{\theta}$ by a single Monte-Carlo sample. This gives us the exact same objective as written above.

Visually, we can look at the objective as follows (figure credit - [Stefano Ermon and Aditya Grover](https://deepgenerativemodels.github.io/assets/slides/cs236_lecture11.pdf)):


<center width=\"100%\"><img src="./images/blog_posts/2022-11-28-deep-energy-based-generative-models/contrastive_divergence.svg" width=\"700px\"></center>

$f_{\theta}$ represents $\exp(-E_{\theta}(\mathbf{x}))$ in our case. Because the larger likelihood has small energy value, thus the correct answer has large $\exp(-E_{\theta}(\mathbf{x}))$ value after training. The point on the right, called \"correct answer\", represents a data point from the dataset (i.e. $x_{\text{train}}$), and the left point, \"wrong answer\", a sample from our model (i.e. $x_{\text{sample}}$). Thus, we try to \"pull up\" the probability of the data points in the dataset, while \"pushing down\" randomly sampled points. The two forces for pulling and pushing are in balance iff $q_{\theta}(\mathbf{x})=p(\mathbf{x})$.


# Sampling from Energy-Based Models

For sampling from an energy-based model, we can apply a Markov Chain Monte Carlo (MCMC) using Langevin Dynamics. **The idea of the algorithm is to start from a random point, and slowly move towards the direction of higher probability using the gradients of $E_{\theta}$.** Nevertheless, this is not enough to fully capture the probability distribution. We need to add noise $\omega$ at each gradient step to the current sample. Under certain conditions such as that we perform the gradient steps an infinite amount of times, we would be able to create an exact sample from our modeled distribution. (**Note. More steps we take, more accurate sample we generate.**) However, as this is not practically possible, we usually limit the chain to $K$ steps ($K$ is a hyperparameter that needs to be finetuned). Overall, the sampling procedure can be summarized in the following algorithm:

<center width=\"100%\" style=\"padding:15px\"><img src="./images/blog_posts/2022-11-28-deep-energy-based-generative-models/sampling.svg" width=\"750px\"></center>


# Applications of Energy-based models beyond generation

Modeling the probability distribution for sampling new data is not the only application of energy-based models. Any application which requires us to compare two elements is much simpler to learn because we just need to go for the higher energy. A couple of examples are shown below (figure credit - [Stefano Ermon and Aditya Grover](https://deepgenerativemodels.github.io/assets/slides/cs236_lecture11.pdf)). A classification setup like object recognition or sequence labeling can be considered as an energy-based task as we just need to find the $Y$ input that minimizes the output $E(X, Y)$ (hence maximizes probability). Similarly, a popular application of energy-based models is denoising of images. Given an image $X$ with a lot of noise, we try to minimize the energy by finding the true input image $Y$.

<center width=\"100%\"><img src="./images/blog_posts/2022-11-28-deep-energy-based-generative-models/energy_models_application.svg" width=\"600px\"></center>

Nonetheless, we will focus on generative modeling here as in the next couple of lectures, we will discuss more generative deep learning approaches.

# Image generation

As an example for energy-based models, we will train a model on image generation. Specifically, we will look at how we can generate MNIST digits with a very simple CNN model. **However, it should be noted that energy models are not easy to train and often diverge if the hyperparameters are not well tuned.** We will rely on training tricks proposed in the paper [Implicit Generation and Generalization in Energy-Based Models](https://arxiv.org/abs/1903.08689) by Yilun Du and Igor Mordatch ([blog](https://openai.com/blog/energy-based-models/)). The important part of this notebook is however to see how the theory above can actually be used in a model.

## Dataset

First, we can load the MNIST dataset below. Note that we need to normalize the images between -1 and 1 instead of mean 0 and std 1 because during sampling, we have to limit the input space. Scaling between -1 and 1 makes it easier to implement it.

```python
# Transformations applied on each image => make them a tensor and normalize between -1 and 1
transform = transforms.Compose([transforms.ToTensor(),
                                transforms.Normalize((0.5,), (0.5,))
                               ])

# Loading the training dataset. We need to split it into a training and validation part
train_set = MNIST(root=DATASET_PATH, train=True, transform=transform, download=True)

# Loading the test set
test_set = MNIST(root=DATASET_PATH, train=False, transform=transform, download=True)

# We define a set of data loaders that we can use for various purposes later.
# Note that for actually training a model, we will use different data loaders
# with a lower batch size.
train_loader = data.DataLoader(train_set, batch_size=128, shuffle=True,  drop_last=True,  num_workers=4, pin_memory=True)
test_loader  = data.DataLoader(test_set,  batch_size=256, shuffle=False, drop_last=False, num_workers=4)
```

## CNN Model

First, we implement our CNN model. The MNIST images are of size 28x28, hence we only need a small model. As an example, we will apply several convolutions with stride 2 that downscale the images. If you are interested, you can also use a deeper model such as a small ResNet, but for simplicity, we will stick with the tiny network.

It is a good practice to use a smooth activation function like Swish instead of ReLU in the energy model. This is because we will rely on the gradients we get back with respect to the input image, which should not be sparse. (**Maybe I can have a try for this point?**)

```python
class Swish(nn.Module):

    def forward(self, x):
        return x * torch.sigmoid(x)


class CNNModel(nn.Module):

    def __init__(self, hidden_features=32, out_dim=1, **kwargs):
        super().__init__()
        # We increase the hidden dimension over layers. Here pre-calculated for simplicity.
        c_hid1 = hidden_features//2
        c_hid2 = hidden_features
        c_hid3 = hidden_features*2

        # Series of convolutions and Swish activation functions
        self.cnn_layers = nn.Sequential(
                nn.Conv2d(1, c_hid1, kernel_size=5, stride=2, padding=4), # [16x16] - Larger padding to get 32x32 image
                Swish(),
                nn.Conv2d(c_hid1, c_hid2, kernel_size=3, stride=2, padding=1), #  [8x8]
                Swish(),
                nn.Conv2d(c_hid2, c_hid3, kernel_size=3, stride=2, padding=1), # [4x4]
                Swish(),
                nn.Conv2d(c_hid3, c_hid3, kernel_size=3, stride=2, padding=1), # [2x2]
                Swish(),
                nn.Flatten(),
                nn.Linear(c_hid3*4, c_hid3),
                Swish(),
                nn.Linear(c_hid3, out_dim)
        )

    def forward(self, x):
        x = self.cnn_layers(x).squeeze(dim=-1)
        return x
```

In the rest of the notebook, the output of the model will actually not represent $E_{\theta}(\mathbf{x})$, but $-E_{\theta}(\mathbf{x})$. This is a standard implementation practice for energy-based models, as some people also write the energy probability density as $q_{\theta}(\mathbf{x}) = \frac{\exp\left(f_{\theta}(\mathbf{x})\right)}{Z_{\theta}}$. In that case, the model would actually represent $f_{\theta}(\mathbf{x})$. In the training loss etc., we need to be careful to not switch up the signs.

