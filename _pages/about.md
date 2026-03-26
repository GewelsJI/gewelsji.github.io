---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

# 🧍‍♂️ Biography
Gepeng Ji is a final-year PhD candidate at the School of Computing, Australian National University, advised by [Professor Nick Barnes](https://scholar.google.com/citations?user=yMXs1WcAAAAJ&hl=en). Prior to this, he received his Master's degree from the School of Computer Science at Wuhan University in 2021. He has published over 30 peer-reviewed academic papers, with more than 10,000+ citations and an h-index of 24, and holds six Chinese technical patents. He regularly serves as a reviewer for top-tier AI journals and conferences, including TPAMI, IJCV, TMI, CVPR, ICCV, and MICCAI. He was named to the Stanford/Elsevier Top 2% Scientists List in both 2024 and 2025.


# 👨‍💻 Research Interests
His research centers on <span style="color: #aa0404; font-weight: bold;">subtle visual perception (微视觉感知)</span>, aiming to model hard-to-detect patterns -- often imperceptible to human vision yet semantically meaningful -- in complex environments using advanced AI techniques, including computer vision, multimodal learning, and reinforcement learning. Empowering such perceptual capabilities in intelligent systems has broad real-world implications, including 1️⃣ **healthcare AI**, where early identification of subtle anomalies in medical imaging can enable timely and potentially life-saving interventions; 2️⃣ **camouflaged scene understanding**, where objects blend into their surroundings due to low contrast and unclear boundaries; and 3️⃣ **ultra-precision vision applications**, where identifying ultra-tiny objects or subtle structures requires fine-grained representation and accurate localization.

# 🔥 News

<div style="
  display: flex;
  gap: 10px;
  border-left: 4px solid #3b82f6;
  background: #f0f7ff;
  padding: 12px 16px;
  border-radius: 6px;
  align-items: flex-start;
">
  <div>🚨</div>
  <div>
    <strong>NOTE</strong><br>
    I am currently on the academic job market and open to postdoctoral and research positions. Please feel free to reach out if you think my background may be a good fit for your group. I am also open to interdisciplinary collaborations and welcome connections with researchers from diverse backgrounds, especially in medical applications.
  </div>
</div>

<br>

- `2026.03` We are excited to launch the [Colon-X](https://github.com/ai4colonoscopy/Colon-X) project, an open initiative aimed at advancing intelligent colonoscopy toward clinical reasoning.
- `2026.01` Our paper "Frontiers in Intelligent Colonoscopy" is now officially available on [Springer](https://link.springer.com/article/10.1007/s11633-025-1597-6) platform. Code can be found on our [GitHub repository](https://github.com/ai4colonoscopy/IntelliScope).

# 📝 Representative Publications 

^ indicates equal contribution, and * denotes corresponding author. For a full list of publications, please visit my 🎓[Google Scholar](https://scholar.google.com/citations?user=oaxKYKUAAAAJ&hl=en) profile. 

## 🚩 <span style="color: #aa0404;">[Research Topic #1] Healthcare AI</span>

<!---------------------------- PraNet ---------------------------->
<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:8px 16px;
  background:#fafafa;
  margin-bottom:8px;
">
  <h3 style="color:#1d4ed8;">
    [MICCAI 2020] PraNet: Parallel Reverse Attention Network for Polyp Segmentation
  </h3>

  <p>
    Deng-Ping Fan, <strong>Ge-Peng Ji</strong>, Tao Zhou, Geng Chen, Huazhu Fu*, Jianbing Shen*, Ling Shao, and Ali Borji<br>
    Medical Image Computing and Computer Assisted Intervention, Virtual, October 4-8, 2020
  </p>

  <div style="display:flex; gap:20px; align-items:flex-start;">

  <div style="flex:0 0 300px;">
    <img
      src="images/academic-related/miccai2020-pranet.png"
      width="300"
      style="display:block; width:300px; height:auto;"
    />
  </div>

  <div style="flex:1; min-width:0;">

  <p>
    <strong>Links:</strong>
    📄Paper (<a href="https://arxiv.org/abs/2006.11392">arXiv</a>; <a href="https://link.springer.com/chapter/10.1007/978-3-030-59725-2_26">Springer</a>; <a href="https://dengpingfan.github.io/papers/[2020][MICCAI]PraNet_Chinese.pdf">中译文</a>) |
    📦<a href="https://github.com/DengPingFan/PraNet">Project Page</a> | 
    📦<a href="https://gitcode.com/Ascend/ModelZoo-PyTorch/tree/master/ACL_PyTorch/contrib/cv/segmentation/PraNet">Huawei Ascend ModelZoo</a> |
    🎬<a href="https://youtu.be/ukJKJosu1f8?si=lMpQekJ84NKuRZX5">Technical Video at MedicoEval'2020 Workshop</a> <span class='show_paper_citations' data='oaxKYKUAAAAJ:g5m5HwL7SMYC'></span>
  </p>

  <p>
    <strong>Keywords:</strong>
    <span style="color:#54b937;">
      #polyp-segmentation, #intelligent-colonoscopy
    </span>
  </p>

  <p>
    <strong>TL;DR:</strong> A pioneering work that introduced a <u>reverse attention mechanism</u> for early lesion detection (particularly effective for weak boundaries), now widely recognized as a standard baseline in medical image segmentation.
  </p>

  <p>
    <strong>Impact:</strong>
    Early acceptance & Oral Presentation (Top 13%) |
    <a href="https://miccai.org/index.php/about-miccai/awards/young-scientist-impact-award/">MICCAI2025 Young Scientist Publication Impact Award</a> (see <a href="images/academic-related/miccai2020-pranet-YSPIA-certificate.jpg">certificate</a> & <a href="images/academic-related/miccai2020-pranet-YSPIA-photo.png">award ceremony photo</a>) |
    <a href="https://scholar.google.com/citations?hl=en&view_op=list_hcore&venue=QLpioUFGyGMJ.2025">#1 most-cited MICCAI paper</a>
    (by <a href="https://scholar.google.com/citations?view_op=metrics_intro&hl=en">Google Scholar Metrics 2025</a>) |
    Ranked #1 in accuracy at the MediaEval 2020 Medico Task |
    Most Influential <a href="images/academic-related/miccai2020-pranet-jittor-award.png">Application Paper Award</a> at the Jittor Developer Conference 2021 |
    Featured in the <a href="https://hai.stanford.edu/ai-index/2022-ai-index-report">Stanford AI Index Report 2022</a>
  </p>
</div>
</div>
</div>
<!---------------------------- PraNet ---------------------------->


<!---------------------------- PNS-Net ---------------------------->
<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:8px 16px;
  background:#fafafa;
  margin-bottom:8px;
">
  <!-- 标题 -->
  <h3 style="color:#1d4ed8;">
    [MICCAI 2021] Progressively Normalized Self-Attention Network for Video Polyp Segmentation
  </h3>

  <!-- 作者 -->
  <p>
    <strong>Ge-Peng Ji^</strong>, Yu-Cheng Chou^, Deng-Ping Fan*, Geng Chen, Huazhu Fu*, Debesh Jha, Ling Shao<br>
    Medical Image Computing and Computer Assisted Intervention, Strasbourg, France, September 27-October 1, 2021
  </p>

  <!-- 左图右文 -->
  <div style="display:flex; gap:20px; align-items:flex-start;">

  <!-- 左图 -->
  <div style="flex:0 0 300px;">
    <img
      src="images/academic-related/miccai2021-pnsnet.png"
      width="300"
      style="display:block; width:300px; height:auto;"
    />
  </div>

  <!-- 右侧 -->
  <div style="flex:1; min-width:0;">

  <!-- 链接 -->
  <p>
    <strong>Links:</strong>
    📄Paper (<a href="https://arxiv.org/abs/2105.08468">arXiv</a>; <a href="https://link.springer.com/chapter/10.1007/978-3-030-87193-2_14">Springer</a>; <a href="https://dengpingfan.github.io/papers/[2021][MICCAI]PNSNet_Chinese.pdf">中译文</a>) |
    📦<a href="https://github.com/GewelsJI/PNS-Net">Project Page</a> |
    🎬<a href="https://youtu.be/JxhoDcg1l78">Introduction Video (YouTube)</a>
  </p>

  <!-- 关键词 -->
  <p>
    <strong>Keywords:</strong>
    <span style="color:#54b937;">#video-polyp-segmentation, #intelligent-colonoscopy</span>
  </p>

  <!-- 亮点 -->
  <p>
    <strong>TL;DR:</strong> We propose a new self-attention mechanism for video polyp segmentation -- an extensible, <u>plug-and-play design</u> that delivers <u>ultra-fast inference</u> (170+ FPS on a single RTX 2080 GPU).
  </p>

  <!-- 影响力 -->
  <p>
    <strong>Impact:</strong> Early acceptance (Top 13%) |
    <a href="https://miccai2021.org/en/MICCAI-2021-TRAVEL-AWARDS.html">MICCAI 2021 Student Travel Award</a> (Top 5.8% = 95/1630)
  </p>
</div>
</div>
</div>
<!---------------------------- PNS-Net ---------------------------->


<!---------------------------- SUN-SEG ---------------------------->
<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:8px 16px;
  background:#fafafa;
  margin-bottom:8px;
">
  <!-- 标题 -->
  <h3 style="color:#1d4ed8;">
    [MIR 2022] Video Polyp Segmentation: A Deep Learning Perspective
  </h3>

  <!-- 作者 -->
  <p>
    <strong>Ge-Peng Ji^</strong>, Guobao Xiao^, Yu-Cheng Chou^, Deng-Ping Fan*, Kai Zhao, Geng Chen, and Luc Van Gool<br>
    Machine Intelligence Research, 2022, 19 (6): 531-549. (IF: 8.7; 中国最具国际影响力学术期刊)
  </p>

  <!-- 左图右文 -->
  <div style="display:flex; gap:20px; align-items:flex-start;">

  <!-- 左图 -->
  <div style="flex:0 0 300px;">
    <img
      src="images/academic-related/mir2022-sunseg.png"
      width="300"
      style="display:block; width:300px; height:auto;"
    />
  </div>

  <!-- 右侧 -->
  <div style="flex:1; min-width:0;">

  <!-- 关键词 -->
  <p>
    <strong>Keywords:</strong>
    <span style="color:#54b937;">
      #video-benchmark, #video-polyp-segmentation, #intelligent-colonoscopy
    </span>
  </p>

  <!-- 链接 -->
  <p>
    <strong>Links:</strong>
    📄Paper (<a href="https://arxiv.org/abs/2203.14291">arXiv</a>; 
    <a href="https://link.springer.com/article/10.1007/s11633-022-1371-y">Springer</a>; <a href="https://dengpingfan.github.io/papers/[2022][MIR]VPS_Chinese.pdf">中译文</a>) |
    📦<a href="https://github.com/GewelsJI/VPS">Project Page</a> |
    🎬<a href="https://github.com/GewelsJI/VPS/assets/38354957/9bea01ae-9582-494f-8bf6-f83307eebc08">Introduction Video (~2min)</a>
  </p>

  <!-- 亮点 -->
  <p>
    <strong>TL;DR:</strong> A comprehensive benchmark and systematic study for video polyp segmentation, providing standardized evaluation and insights for future research.
  </p>

</div>
</div>
</div>
<!---------------------------- SUN-SEG ---------------------------->


<!---------------------------- colongpt ---------------------------->
<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:8px 16px;
  background:#fafafa;
  margin-bottom:8px;
">
  <!-- 标题 -->
  <h3 style="color:#1d4ed8;">
    [MIR 2026] Frontiers in Intelligent Colonoscopy
  </h3>

  <!-- 作者 -->
  <p>
    <strong>Ge-Peng Ji</strong>, Jingyi Liu, Peng Xu, Nick Barnes, Fahad Shahbaz Khan, Salman Khan, Deng-Ping Fan*<br>
    Machine Intelligence Research, 2026, 23 (1), 70-114. (IF: 8.7; 中国最具国际影响力学术期刊)
  </p>

  <!-- 左图右文 -->
  <div style="display:flex; gap:20px; align-items:flex-start;">

  <!-- 左图 -->
  <div style="flex:0 0 300px;">
    <img
      src="images/academic-related/mir2026-colongpt.png"
      width="300"
      style="display:block; width:300px; height:auto;"
    />
  </div>

  <!-- 右侧 -->
  <div style="flex:1; min-width:0;">

  <!-- 关键词 -->
  <p>
    <strong>Keywords:</strong>
    <span style="color:#54b937;">
      #survey, #multimodal-benchmark, #multimodal-large-language-model, #intelligent-colonoscopy
    </span>
  </p>

  <!-- 链接 -->
  <p>
    <strong>Links:</strong>
    📄Paper (<a href="https://arxiv.org/abs/2410.17241">arXiv</a>; 
    <a href="https://link.springer.com/article/10.1007/s11633-025-1597-6">Springer</a>; <a href="https://dengpingfan.github.io/papers/[2026][MIR]IntelliScope_Chinese.pdf">中译文</a>) |
    📦<a href="https://github.com/ai4colonoscopy/IntelliScope">Project Page</a> |
    🗂️<a href="https://docs.google.com/spreadsheets/d/1V_s99Jv9syzM6FPQAJVQqOFm5aqclmrYzNElY6BI18I/edit?usp=sharing">ColonSurvey</a> |
    🤗<a href="https://huggingface.co/datasets/ai4colonoscopy/ColonINST-v1">ColonINST</a> |
    🤗<a href="https://huggingface.co/ai4colonoscopy/ColonGPT">ColonGPT</a>
  </p>

  <!-- 亮点 -->
  <p>
    <strong>TL;DR:</strong> A comprehensive survey of intelligent colonoscopy, covering the latest advances in multimodal benchmarks and large language models, and providing insights into future research directions.
  </p>

</div>
</div>
</div>
<!---------------------------- colongpt ---------------------------->


<!---------------------------- colon-x ---------------------------->
<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:8px 16px;
  background:#fafafa;
  margin-bottom:8px;
">
  <!-- 标题 -->
  <h3 style="color:#1d4ed8;">
    [arXiv 2026] Colon-X: Advancing Intelligent Colonoscopy toward Clinical Reasoning
  </h3>

  <!-- 作者 -->
  <p>
    <strong>Ge-Peng Ji</strong>, Jingyi Liu, Deng-Ping Fan*, Huazhu Fu, Nick Barnes
  </p>

  <!-- 左图右文 -->
  <div style="display:flex; gap:20px; align-items:flex-start;">

  <!-- 左图 -->
  <div style="flex:0 0 300px;">
    <img
      src="images/academic-related/arxiv2026-colonx.png"
      width="300"
      style="display:block; width:300px; height:auto;"
    />
  </div>

  <!-- 右侧 -->
  <div style="flex:1; min-width:0;">

  <!-- 关键词 -->
  <p>
    <strong>Keywords:</strong>
    <span style="color:#54b937;">
      #multimodal-benchmark, #multimodal-large-language-model, #multimodal-reasoning, #intelligent-colonoscopy
    </span>
  </p>

  <!-- 链接 -->
  <p>
    <strong>Links:</strong>
    📄Paper (<a href="https://arxiv.org/abs/2512.03667">arXiv</a>) |
    📦<a href="https://github.com/ai4colonoscopy/Colon-X">Project Page</a> 
  </p>

  <!-- 亮点 -->
  <p>
    <strong>TL;DR:</strong> Introducing COLON-X, a multimodal benchmark designed to advance intelligent colonoscopy toward clinical reasoning, featuring comprehensive datasets and evaluation protocols for multimodal learning and reasoning in colonoscopy.
  </p>

</div>
</div>
</div>
<!---------------------------- colon-x ---------------------------->

#### 🚩 <span style="color: #aa0404;">[Research Topic #2] Camouflaged Scene Understanding</span>

Camouflaged scene understanding focuses on the perception and analysis of objects that blend into their surroundings, making them difficult to detect due to low contrast and unclear boundaries. This research area is crucial for applications such as wildlife monitoring, search and rescue operations, and military surveillance. The core challenge lies in developing models that can effectively capture subtle visual cues and contextual information to accurately identify camouflaged objects in complex environments.


<!---------------------------- cod10k ---------------------------->
<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:8px 16px;
  background:#fafafa;
  margin-bottom:8px;
">
  <!-- 标题 -->
  <h3 style="color:#1d4ed8;">
    [TPAMI 2021] Concealed Object Detection (extended version of <a href="https://openaccess.thecvf.com/content_CVPR_2020/papers/Fan_Camouflaged_Object_Detection_CVPR_2020_paper.pdf">CVPR 2020</a>)
  </h3>

  <!-- 作者 -->
  <p>
    Deng-Ping Fan, <strong>Ge-Peng Ji</strong>, Ming-Ming Cheng*, and Ling Shao<br>
    IEEE Transactions on Pattern Analysis and Machine Intelligence, 2022, 44 (10): 6024-6042. (IF: 18.6)
  </p>

  <!-- 左图右文 -->
  <div style="display:flex; gap:20px; align-items:flex-start;">

  <!-- 左图 -->
  <div style="flex:0 0 300px;">
    <img
      src="images/academic-related/cvpr2020-cod10k-v1.png"
      width="300"
      style="display:block; width:300px; height:auto;"
    />
  </div>

  <!-- 右侧 -->
  <div style="flex:1; min-width:0;">

  <!-- 关键词 -->
  <p>
    <strong>Keywords:</strong>
    <span style="color:#54b937;">
      #image-benchmark, #camouflaged-object-detection, #concealed-object-detection
    </span>
  </p>

  <!-- 链接 -->
  <p>
    <strong>Links:</strong>
    📄TPAMI 2021 Journal Paper (<a href="https://arxiv.org/abs/2102.10274">arXiv</a>; <a href="https://ieeexplore.ieee.org/document/9444794">IEEE Xplore</a>; <a href="https://github.com/GewelsJI/SINet-V2">GitHub</a>; <a href="https://drive.google.com/file/d/1g0VDGPDPiN3mwV2TjNTQIo8FedGr_v8G/view?usp=share_link"> Supplementary Material</a>; <a href="https://drive.google.com/file/d/1vfymY0GrzbvkxUNYEkWzHBdO1JmEOVQQ/view?usp=share_link">中译文</a>) |
    📄CVPR 2020 Conference Paper (<a href="https://openaccess.thecvf.com/content_CVPR_2020/html/Fan_Camouflaged_Object_Detection_CVPR_2020_paper.html">CVF Open Access</a>; <a href="https://github.com/DengPingFan/SINet/">Github</a>; <a href="https://drive.google.com/file/d/1fE9YVD0k6oNowxY1Ds4ZpYeBAmbJlAyk/view?usp=share_link">中译文</a>) |
    📦<a href="https://dengpingfan.github.io/pages/COD.html">Project Page</a> |
    📦<a href="https://drive.google.com/file/d/1vRYAie0JcNStcSwagmCq55eirGyMYGm5/view?usp=sharing">Download COD10K dataset</a> |
    🎮<a href="https://mmcheng.net/cod/">Online Playground</a>
  </p>

  <!-- 亮点 -->
  <p>
    <strong>TL;DR:</strong> Introducing COD10K, a large-scale benchmark for camouflaged object detection, featuring comprehensive datasets and evaluation protocols for advancing the field of camouflage-aware computer vision.
  </p>

  <p>
    <strong>Impact:</strong> CVPR Oral Paper (Top 5.7% = 335/5865) | ESI Hot Paper (Top 0.1%) | <a href="images/academic-related/tpami2021-sinetv2-jittor-award.png">Distinguish Paper</a> at the Jittor Developer Conference 2021 | Covered by <a href="https://www.newscientist.com/article/2243247-an-ai-trained-to-spot-hidden-objects-can-see-through-camouflage/">"New Scientist"</a> magazine (see the <a href="images/academic-related/cvpr2020-cod10k-new-scientist.png">media snapshot</a>) | <a href="https://cg.cs.tsinghua.edu.cn/jittor/news/2021-06-11-00-00-cod/">推动国产Jittor生态体系建设</a>
  </p>  
</div>
</div>
</div>
<!---------------------------- cod10k ---------------------------->


<!---------------------------- dgnet ---------------------------->
<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:8px 16px;
  background:#fafafa;
  margin-bottom:8px;
">
  <!-- 标题 -->
  <h3 style="color:#1d4ed8;">
    [MIR 2023] Deep Gradient Learning for Efficient Camouflaged Object Detection
  </h3>

  <!-- 作者 -->
  <p>
    <strong>Ge-Peng Ji</strong>, Deng-Ping Fan*, Yu-Cheng Chou, Dengxin Dai, Alexander Liniger, Luc Van Gool<br>
    Machine Intelligence Research, 2023, 20 (1): 92-108. (IF: 8.7; JCR Q1; 中国最具国际影响力学术期刊)
  </p>

  <!-- 左图右文 -->
  <div style="display:flex; gap:20px; align-items:flex-start;">

  <!-- 左图 -->
  <div style="flex:0 0 300px;">
    <img
      src="images/academic-related/mir2023-dgnet.png"
      width="300"
      style="display:block; width:300px; height:auto;"
    />
  </div>

  <!-- 右侧 -->
  <div style="flex:1; min-width:0;">

  <!-- 关键词 -->
  <p>
    <strong>Keywords:</strong>
    <span style="color:#54b937;">
      #efficient-camouflaged-object-segmentation, #polyp-segmentation, #industrial-defect-segmentation
    </span>
  </p>

  <!-- 链接 -->
  <p>
    <strong>Links:</strong>
    📄Paper (<a href="https://arxiv.org/abs/2205.12853">arXiv</a>; <a href="https://link.springer.com/article/10.1007/s11633-022-1365-9">Springer</a>) |
    📦<a href="https://github.com/GewelsJI/DGNet">Project Page</a> (supporting <a href="https://github.com/GewelsJI/DGNet/tree/main/lib_pytorch">PyTorch</a>/<a href="https://github.com/GewelsJI/DGNet/tree/main/lib_jittor">Jittor</a>/<a href="https://github.com/GewelsJI/DGNet/tree/main/lib_ascend">Ascend</a> platforms) |
    🎬<a href="https://github.com/GewelsJI/DGNet/assets/38354957/ceff5686-8b91-4e03-b164-0780c402b68a">Introduction video (~2min)</a>
    
  </p>

  <!-- 亮点 -->
  <p>
    <strong>TL;DR:</strong> Introducing DGNet (Deep Gradient Network), a novel approach for efficient camouflaged object detection that leverages gradient-based learning to enhance detection performance while significantly reducing computational overhead.
  </p>

</div>
</div>
</div>
<!---------------------------- dgnet ---------------------------->

<!---------------------------- sam4cod ---------------------------->
<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:8px 16px;
  background:#fafafa;
  margin-bottom:8px;
">
  <!-- 标题 -->
  <h3 style="color:#1d4ed8;">
    [SCIS 2023] SAM Struggles in Concealed Scenes -- Empirical Study on Segment Anything
  </h3>

  <!-- 作者 -->
  <p>
    <strong>Ge-Peng Ji</strong>, Deng-Ping Fan, Peng Xu*, Ming-Ming Cheng, Bowen Zhou, Luc Van Gool<br>
    SCIENCE CHINA Information Sciences, 2023, 66: 226101. (IF: 7.6; CiteScore: 12.6; CCF-A; 中国最具国际影响力学术期刊)
  </p>

  <!-- 左图右文 -->
  <div style="display:flex; gap:20px; align-items:flex-start;">

  <!-- 左图 -->
  <div style="flex:0 0 300px;">
    <img
      src="images/academic-related/scis2023-sam4cod.png"
      width="300"
      style="display:block; width:300px; height:auto;"
    />
  </div>

  <!-- 右侧 -->
  <div style="flex:1; min-width:0;">

  <!-- 关键词 -->
  <p>
    <strong>Keywords:</strong>
    <span style="color:#54b937;">
      #image-benchmark, #promptable-segmentation, #camouflaged-object-segmentation, #polyp-segmentation, #industrial-defect-segmentation
    </span>
  </p>

  <!-- 链接 -->
  <p>
    <strong>Links:</strong>
    📄Paper (<a href="https://arxiv.org/abs/2304.06022">arXiv</a>; <a href="https://link.springer.com/article/10.1007/s11432-023-3881-x">Springer</a>) | 📰<a href="https://mp.weixin.qq.com/s/o4wNhZ1SAE0ARhPQRH2T2g">获《中国科学信息科学》官方微信公众号专题解读</a>
  </p>

  <!-- 亮点 -->
  <p>
    <strong>TL;DR:</strong> SAM evaluation on concealed scenes, revealing significant performance gaps and highlighting the need for specialized approaches in camouflaged object detection.
  </p>
</div>
</div>
</div>
<!---------------------------- sam4cod ---------------------------->


#### 🚩 <span style="color: #aa0404;">[Research Topic #3] Ultra-Precision Vision Applications</span>

In real-world vision systems such as autonomous driving (e.g., distant traffic signs and lane markings), image matting (e.g., hair-level boundary extraction), and remote sensing (e.g., tiny object detection in high-resolution imagery), even pixel-level inaccuracies can lead to critical failures. Our goal is to <u><b>unlock ultra-precision representations</b></u> in complex vision systems, enabling precise structure delineation and reliable tiny object localization.


<!---------------------------- fsnet ---------------------------->
<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:8px 16px;
  background:#fafafa;
  margin-bottom:8px;
">
  <!-- 标题 -->
  <h3 style="color:#1d4ed8;">
    [ICCV 2021] Full-Duplex Strategy for Video Object Segmentation
  </h3>

  <!-- 作者 -->
  <p>
    <strong>Ge-Peng Ji</strong>, Deng-Ping Fan*, Keren Fu, Zhe Wu, Jianbing Shen, Ling Shao<br>
    International Conference on Computer Vision, Virtual, October 11-17, 2021
  </p>

  <!-- 左图右文 -->
  <div style="display:flex; gap:20px; align-items:flex-start;">

  <!-- 左图 -->
  <div style="flex:0 0 300px;">
    <img
      src="images/academic-related/iccv2021-fsnet.png"
      width="300"
      style="display:block; width:300px; height:auto;"
    />
  </div>

  <!-- 右侧 -->
  <div style="flex:1; min-width:0;">

  <!-- 关键词 -->
  <p>
    <strong>Keywords:</strong>
    <span style="color:#54b937;">
      #video-object-segmentation, #video-salient-object-detection
    </span>
  </p>

  <!-- 链接 -->
  <p>
    <strong>Links:</strong>
    📄ICCV 2021 Conference Paper (<a href="https://arxiv.org/pdf/2108.03151v2">arXiv</a>; <a href="https://ieeexplore.ieee.org/document/9711449">IEEE Xplore</a>; <a href="https://drive.google.com/file/d/1CcaFWNo23wCMusx95JY4Cuyl6v5T73in/view?usp=share_link">中译文</a>) | 📄CVMJ 2023 Journal Extension (IF: 18.3; 中国最具国际影响力学术期刊; <a href="https://arxiv.org/pdf/2108.03151v3">arXiv</a>; <a href="https://ieeexplore.ieee.org/document/10897692">IEEE Xplore</a>) | 
    📦<a href="https://github.com/GewelsJI/FSNet">Project Page</a>
  </p>

  <!-- 亮点 -->
  <p>
    <strong>TL;DR:</strong> A pioneering work that introduces a full-duplex learning strategy to capture static–dynamic interactions, enabling precise segmentation of moving objects in dynamic scenes.
  </p>

  <p>
    <strong>Impact:</strong>
    Honorable Mention Award at CVMJ 2023 (see the <a href="images/academic-related/cvmj2023-certificate.png">certificate</a>)
  </p>
</div>
</div>
</div>
<!---------------------------- fsnet ---------------------------->

<!---------------------------- lawdis ---------------------------->
<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:8px 16px;
  background:#fafafa;
  margin-bottom:8px;
">
  <!-- 标题 -->
  <h3 style="color:#1d4ed8;">
    [ICCV 2025] LawDIS: Language-Window-based Controllable Dichotomous Image Segmentation
  </h3>

  <!-- 作者 -->
  <p>
    Xinyu Yan, Meijun Sun, <strong>Ge-Peng Ji</strong>, Fahad Shahbaz Khan, Salman Khan, Deng-Ping Fan*<br>
    International Conference on Computer Vision, Honolulu, Hawaii, USA, October 19-23, 2025
  </p>

  <!-- 左图右文 -->
  <div style="display:flex; gap:20px; align-items:flex-start;">

  <!-- 左图 -->
  <div style="flex:0 0 300px;">
    <img
      src="images/academic-related/iccv2025-lawdis.gif"
      width="300"
      style="display:block; width:300px; height:auto;"
    />
  </div>

  <!-- 右侧 -->
  <div style="flex:1; min-width:0;">

  <!-- 关键词 -->
  <p>
    <strong>Keywords:</strong>
    <span style="color:#54b937;">
      #promptable-segmentation, #stable-diffusion, #dischotomous-image-segmentation
    </span>
  </p>

  <!-- 链接 -->
  <p>
    <strong>Links:</strong>
    📄Paper (<a href="https://arxiv.org/abs/2508.01152">arXiv</a>; <a href="https://openaccess.thecvf.com/content/ICCV2025/html/Yan_LawDIS_Language-Window-based_Controllable_Dichotomous_Image_Segmentation_ICCV_2025_paper.html">CVF Open Access</a>; <a href="https://drive.google.com/file/d/14GQIMlyZJrK4wkEIY1IiIOsy5enTowzZ/view?usp=share_link">中译文</a>) | 
    📦<a href="https://github.com/XinyuYanTJU/LawDIS">Project Page</a> |
    🎬<a href="https://github.com/user-attachments/assets/7d4c33a5-eff9-4474-a454-bff2b6ec78fa">introduction video (~1min)</a>
  </p>

  <!-- Most high-precision segmentation methods rely on global refinement, which is spatially non-monotonic -- improving some regions often degrades others.  -->
  <!-- 亮点 -->
  <p>
    <strong>TL;DR:</strong>
    <u>Describe, segment, and post-refine</u> -- LawDIS enables human users to precisely segment objects with simple language instructions, and post-refine user-specified regions interactively.
  </p>
</div>
</div>
</div>
<!---------------------------- lawdis ---------------------------->

<!-- # 📖 Educations
- `2022.09 - Present` Ph.D., School of Computing, Australian National University, Canberra, Australia.
- `2018.09 - 2021.06` M.S., School of Computer Science, Wuhan University, Wuhan, China. -->

# 💻 Working Experience
- `2023.03 - 2023.09` Visiting Scholar, Machine Learning Department, Mohamed bin Zayed University of Artificial Intelligence (MBZUAI), Abu Dhabi, UAE.
- `2022.04 - 2022.07` Research Assistant, Sensing Intelligence and Machine Learning Laboratory (SIGMA Lab), Wuhan University, Wuhan, China.
- `2021.06 - 2022.04` Research Intern (Talent Program), Alibaba Group (ICBU Technology Department), Hangzhou, China.
- `2020.11 - 2021.04` Research Intern, Inception Institute of Artificial Intelligence (IIAI-CV&Med Team), Abu Dhabi, UAE.

# 💬 Invited Talks

* `2026.03.19` ANU Seminar Talk "Multimodal Intelligence in Colonoscopy: Perception, Understanding, and Reasoning"
* `2023.09.23` 国际图象图形学学术会议(ICIG 2023) - 多模态数据感知与学习Workshop大会报告 "Towards AI-Powered Colonoscopy" ([Page1](http://icig2023.csig.org.cn/workshops/)/[Page2](https://mp.weixin.qq.com/s/GzdW9xxDqh_ldmJnLcu65w))
* `2023.07.06` 机器智能前沿论坛·第2期 "伪装场景感知及多模态应用: 一种基于梯度先验信息学习的高效伪装目标分割方法" ([Page](https://mp.weixin.qq.com/s/ehlYTWJN8csYPs54e-oRbA) & [Recorded Video](https://www.bilibili.com/video/BV1ku411b7pR?t=602.3))
* `2023.03.31` 中国图象图形学学会第三期学生会员分享论坛会议 "Towards AI-Powered Colonoscopy" ([Page](https://mp.weixin.qq.com/s/s-laGFgOqRIuDHW-cK1SuA)) 
* `2023.01.06` Shenzhen University Talking 2023: "Towards AI-Powered Colonoscopy" 
* `2022.12.07` Anhui University Talking 2022: "Colonoscopy in the AI Era" 
* `2022.10.10` VALSE 2021 Workshop 6 -- Spotlight Talking: "Camouflaged Object Detection and its Applications" ([Poster](http://valser.org/2021/#/poster)) 
* `2021.11.15` Synced-ICCV 2021 "Full-Duplex Strategy for Video Object Segmentation"
* `2021.08.28` CSIG-ICCV 2021 "Full-Duplex Strategy for Video Object Segmentation" ([Page](https://event.baai.ac.cn/event/162#section-one)) 
* `2021.05.15` Alibaba Group ICBU Talking 2021: "Camouflaged Object Detection in the Deep Learning Era"


# 🏆 Honors and Awards
- `2025` MICCAI Young Scientist Publication Impact Award (Top ~0.2% from 2020-2024 accepted papers, [Link](https://miccai.org/index.php/about-miccai/awards/young-scientist-impact-award/))
- `2025` CVPR 2025 Outstanding Reviewer Award (Top 5.6%=711/12000+, [Link](https://cvpr.thecvf.com/Conferences/2025/ProgramCommittee#all-outstanding-reviewer))
- `2025` Stanford/Elsevier Top 2% Scientists List 2025 ([Link](https://topscinet.com/scientist_profile/Ji,%20Gepeng/2020/?stype=single_year#google_vignette))
- `2024` MICCAI2024 Young Scientist Publication Impact Award Shortlist
- `2024` Stanford/Elsevier Top 2% Scientists List 2024 ([Link](https://topresearcherslist.com/Home/Profile/924272))
- `2024` CVM Honorable Paper Mention Award in 2023 ([Journal Updates](https://link.springer.com/journal/41095/updates/26965690))
- `2024` MIR Outstanding Reviewer Award in 2023 ([MIR Journal News](https://link.springer.com/journal/11633/updates/26630820))
- `2023` IEEE Transactions on Medical Imaging Distinguished Reviewer (Bronze Level 2022 – 2023)
- `2021` Jittor Developer Conference Distinguished Paper & Most Influential (Application) Paper
- `2021` MICCAI Student Travel Award ([MICCAI link](https://www.miccai2021.org/en/MICCAI-2021-TRAVEL-AWARDS.html))
- `2020` Multimedia Evaluation Benchmark Workshop (Ranking Top-1 in terms of accuracy metric)
- `2019` Sparse Representation and Intelligent Analysis Competition of Remote Sensing Images (Co-organized by Huawei Co., LTD \& Wuhan University), Object Detection Track (Ranking: Top 6%).

# 📃 Academic Services

#### Program Committee Member & Conference Reviewer

* International Conference on Learning Representations ([ICLR@2022](https://iclr.cc/Conferences/2022), [ICLR@2023](https://iclr.cc/Conferences/2023))<br>
* International Conference on Machine Learning ([ICML@2022](https://icml.cc/Conferences/2022), [ICML@2023](https://icml.cc/Conferences/2023))<br>
* Conference on Neural Information Processing Systems ([NeurIPS@2022](https://nips.cc/Conferences/2022), [NeurIPS@2023](https://neurips.cc/Conferences/2023))<br>
* IEEE/CVF Computer Vision and Pattern Recognition Conference ([CVPR@2022](https://cvpr2022.thecvf.com/), [CVPR@2023](https://cvpr2023.thecvf.com/), [CVPR@2024](https://cvpr2024.thecvf.com/), [CVPR@2025](https://cvpr2025.thecvf.com/))<br>
* International Conference on Computer Vision ([ICCV@2023](https://iccv2023.thecvf.com))<br>
* European Conference on Computer Vision ([ECCV@2022](https://eccv2022.ecva.net/))<br>
* International Joint Conference on Artificial Intelligence ([IJCAI@2021](https://ijcai-21.org/), [IJCAI@2022](https://ijcai-22.org/), [IJCAI@2023](https://ijcai-23.org))<br>
* International Conference on Medical Image Computing and Computer Assisted Intervention ([MICCAI@2020](https://miccai2020.org/en/), [MICCAI@2022](https://miccai2022.org/), [MICCAI@2023](https://conferences.miccai.org/2023/en/))<br>
* IEEE International Conference on Acoustics, Speech, & Signal Processing ([ICASSP@2023](https://2023.ieeeicassp.org/))
* IEEE International Conference on Image Processing ([ICIP@2022](https://2022.ieeeicip.org/), [ICIP@2023](https://2023.ieeeicip.org))<br>
* IEEE International Symposium on Mixed and Augmented Reality ([ISMAR@2021](https://ismar21.org/))<br>
* Chinese Conference on Pattern Recognition and Computer Vision ([PRCV@2021](http://2021.prcv.cn/), PRCV2023)<br>
* Australasian Joint Conference on Artificial Intelligence ([AJCAI@2023](https://ajcai2023.org))<br>

#### Journal Reviewer

* IEEE Transactions on Pattern Analysis and Machine Intelligence ([TPAMI](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=34))
* International Journal of Computer Vision ([IJCV](https://www.springer.com/journal/11263/))<br>
* IEEE Transactions on Image Processing ([TIP](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=83))<br>
* IEEE Journal of Biomedical and Health Informatics ([JBHI](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=6221020))<br>
* IEEE Transactions on Medical Imaging ([TMI](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=42))<br>
* IEEE Transactions on Visualization and Computer Graphics ([TVCG](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=2945))<br>
* IEEE Transactions on Circuits and Systems for Video Technology ([TCSVT](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=76))<br>
* IEEE Transactions on Multimedia ([TMM](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=6046))<br>
* Computational Visual Media ([CVM](https://www.springer.com/journal/41095))<br>
* Machine Intelligence Research ([MIR](https://www.springer.com/journal/11633))<br>
* Information Fusion ([IF](https://www.sciencedirect.com/journal/information-fusion))
* Neurocomputing ([NC](https://www.elsevier.com/journals/neurocomputing/0925-2312))<br>
* Computer Vision and Image Understanding ([CVIU](https://www.sciencedirect.com/journal/computer-vision-and-image-understanding))<br>
* Scientific Reports ([Link](https://www.nature.com/srep/))<br>
* Expert Systems with Applications ([ESWA](https://www.sciencedirect.com/journal/expert-systems-with-applications))<br>
* Digital Signal Processing ([DSP](https://www.sciencedirect.com/journal/digital-signal-processing))<br>
* Sensors ([Link](https://www.mdpi.com/journal/sensors))<br>
* Signal Processing: Image Communication ([SPIC](https://www.sciencedirect.com/journal/signal-processing-image-communication))<br>
* The Visual Computer ([TVC](https://www.springer.com/journal/371/?utm_source=letpub&utm_medium=display&utm_content=mpu&utm_campaign=SRCN_3_ll01_cn_letpuborganic_cs_371))<br>
* International Journal of Imaging Systems and Technology ([IJIST](https://onlinelibrary.wiley.com/journal/10981098))
* Diagnostics ([Link](https://www.mdpi.com/journal/diagnostics))<br>
* Biocybernetics and Biomedical Engineering ([BBE](https://www.journals.elsevier.com/biocybernetics-and-biomedical-engineering))<br>

# 🔗 Useful Resources
- [中国计算机学会(CCF)推荐国际学术会议和期刊目录](https://ccf.atom.im) & [官方公示(2026.03)](https://www.ccf.org.cn/Academic_Evaluation/By_category/)
- [AI conference deadlines](https://github.com/ccfddl/ccf-deadlines)
- [Best Paper Awards in Computer Science (1996-2023)](https://jeffhuang.com/best_paper_awards/)
- [剑桥大学:语言和写作决定人生发展的潜力](https://www.isee-ai.cn/~zhwshi/writing.pdf)