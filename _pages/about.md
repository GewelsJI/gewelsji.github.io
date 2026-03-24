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
I am a final-year PhD candidate at the School of Computing, Australian National University, advised by [Professor Nick Barnes](https://scholar.google.com/citations?user=yMXs1WcAAAAJ&hl=en). Prior to this, I obtained my Master's degree from the School of Computer Science at Wuhan Universityin 2021. I have published over 30 academic papers, with more than 10,000+ citations and an h-index of 24, and hold six technical patents (CN). I regularly serve as a reviewer for top-tier AI journals and conferences, including TPAMI, TIP, IJCV, CVPR, ICCV, and NeurIPS. I was named to Stanford/Elsevier's list of the world's top 2% scientists for two consecutive years (2024 & 2025).


# 👨‍💻 Research Interests
My research centers on <span style="color: #fe3535;">subtle visual perception (微视觉感知)</span>, aiming to model hard-to-detect patterns -- often imperceptible to human vision yet semantically meaningful -- in complex environments using advanced AI techniques, including computer vision, multimodal learning, and reinforcement learning. Empowering such perceptual capabilities in intelligent systems has broad real-world implications, including 1️⃣ **healthcare AI**, where early identification of subtle anomalies in medical imaging can enable timely and potentially life-saving interventions; 2️⃣ **camouflaged scene understanding**, where objects blend into their surroundings due to low contrast and unclear boundaries; and 3️⃣ **ultra-precision applications**, where identifying ultra-tiny objects or subtle structures requires high spatial precision and fine-grained representation.

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
    I am currently on the academic job market and open to postdoctoral and research positions. Please feel free to contact me if you think I might be a good fit for your team. I am also open to interdisciplinary collaborations and welcome connections with researchers from diverse backgrounds, especially in medical applications.
  </div>
</div>

# 🔥 News
- `2026.03` We are excited to launch the [Colon-X](https://github.com/ai4colonoscopy/Colon-X) project, an open initiative aimed at advancing intelligent colonoscopy toward clinical reasoning.
- `2026.01` Our paper "Frontiers in Intelligent Colonoscopy" has officially available on [Springer](https://link.springer.com/article/10.1007/s11633-025-1597-6) platform. Code can be found on our [GitHub repository](https://github.com/ai4colonoscopy/IntelliScope).

# 📝 Representative Publications 

> Full publication list: [Google Scholar](https://scholar.google.com/citations?user=oaxKYKUAAAAJ&hl=en). \* stands for equal contribution and † means corresponding author.

#### 🚩 <span style="color: #aa0404;">[Research Topic #1] Healthcare AI</span>


<div style="
  border:2px solid #e5e7eb;
  border-radius:10px;
  padding:16px;
  background:#fafafa;
">

  <!-- 标题 -->
  <h4 style="color:#1d4ed8;">
    [MICCAI 2020] PraNet: Parallel Reverse Attention Network for Polyp Segmentation
  </h4>

  <!-- 作者 -->
  <p>
    Deng-Ping Fan, <strong>Ge-Peng Ji</strong>, Tao Zhou, Geng Chen, Huazhu Fu†, Jianbing Shen†, Ling Shao, and Ali Borji<br>
    Early acceptance & Oral (Accept rate = 13%) | <a href="https://miccai.org/index.php/about-miccai/awards/young-scientist-impact-award/">MICCAI2025 Young Scientist Publication Impact Award</a> |  <a href="https://scholar.google.com/citations?hl=en&view_op=list_hcore&venue=QLpioUFGyGMJ.2025">Rank#1 Cited Paper in MICCAI</a> ( (by <a href="https://scholar.google.com/citations?view_op=metrics_intro&hl=en">Google Scholar Metrics 2025</a>) | Top#1 Accuracy of MediaEval 2020 Workshop (Medico Track) | Most Influential Application Paper Award at the Jittor Developer Conference 2021 | Featured in the <a href="https://hai.stanford.edu/ai-index/2022-ai-index-report">Stanford AI Index Report 2022</a>
  </p>

  <!-- 左图右文 -->
  <div style="display:flex; gap:20px;">

    <!-- 左图 -->
    <img src="images/miccai2020-pranet.png" style="width:40%;">

    <!-- 右侧 -->
    <div>

      <!-- 关键词 -->
      <p style="color:#54b937;">
        #medical-image-segmentation, #reverse-attention, #polyp-segmentation, #colonoscopy
      </p>

      <!-- 链接 -->
      <p>
        <a href="https://arxiv.org/abs/2006.11392">Paper</a> |
        <a href="https://github.com/DengPingFan/PraNet">Project</a> |
        <a href="https://link.springer.com/chapter/10.1007/978-3-030-59725-2_26">Official Version</a> |
        <a href="https://dengpingfan.github.io/papers/[2020][MICCAI]PraNet_Chinese.pdf">中文译文</a> 
      </p>

      <!-- 亮点 -->
      <p>First work to propose a parallel reverse attention mechanism for polyp segmentation.</p>

    </div>

  </div>

</div>

pns-net

sun-seg

colongpt

colon-x

#### 🚩 <span style="color: #aa0404;">[Research Topic #2] Camouflaged Scene Understanding</span>

sinet sinet-v2 dgnet

#### 🚩 <span style="color: #aa0404;">[Research Topic #3] Ultra-Precision Applications</span>

lawdis

<!-- # 📖 Educations
- `2022.09 - Present` Ph.D., School of Computing, Australian National University, Canberra, Australia.
- `2018.09 - 2021.06` M.S., School of Computer Science, Wuhan University, Wuhan, China. -->

# 💻 Working Experience
- `2023.03 - 2023.09` Research Assistant, Machine Learning Department, Mohamed bin Zayed University of Artificial Intelligence (MBZUAI), Abu Dhabi, UAE.
- `2022.04 - 2022.07` Research Assistant, Sensing Intelligence and Machine Learning Laboratory (SIGMA Lab), Wuhan University, Wuhan, China.
- `2021.06 - 2022.04` Research Intern (Talent Program), Alibaba Group (ICBU Technology Department), Hangzhou, China.
- `2020.11 - 2021.04` Research Intern, Inception Institute of Artificial Intelligence (IIAI-CV&Med Team), Abu Dhabi, UAE.

# 💬 Invited Talks

* `2023.09.23` 国际图象图形学学术会议(ICIG 2023) - 多模态数据感知与学习Workshop大会报告 "Towards AI-Powered Colonoscopy" ([Page1](http://icig2023.csig.org.cn/workshops/)/[Page2](https://mp.weixin.qq.com/s/GzdW9xxDqh_ldmJnLcu65w))
* `2023.07.06` 机器智能前沿论坛·第2期 "伪装场景感知及多模态应用: 一种基于梯度先验信息学习的高效伪装目标分割方法" ([Page](https://mp.weixin.qq.com/s/ehlYTWJN8csYPs54e-oRbA) & [Recorded Video](https://www.bilibili.com/video/BV1ku411b7pR?t=602.3))
* `2023.03.31` 中国图象图形学学会第三期学生会员分享论坛会议 "Towards AI-Powered Colonoscopy" ([Page](https://mp.weixin.qq.com/s/s-laGFgOqRIuDHW-cK1SuA)) 
* `2023.01.06` Shenzhen Univeristy Talking 2023: "Towards AI-Powered Colonoscopy" 
* `2022.12.07` Anhui Univeristy Talking 2022: "Colonoscopy in the AI Era" 
* `2022.10.10` VALSE 2021 Workshop 6 -- Spotlight Talking: "Camouflaged Object Detection and its Applications" ([Poster](http://valser.org/2021/#/poster)) 
* `2021.11.15` Synced-ICCV 2021 "Full-Duplex Strategy for Video Object Segmentation"
* `2021.08.28` CSIG-ICCV 2021 "Full-Duplex Strategy for Video Object Segmentation" ([Page](https://event.baai.ac.cn/event/162#section-one)) 
* `2021.05.15` Alibaba Group ICBU Talking 2021: "Camouflaged Object Detection in the Deep Learning Era"


# 🏆 Honors and Awards
- `2025` MICCAI Young Scientist Publication Impact Award (Top~0.2% from 2020-2024 accepted papers, [Link](https://miccai.org/index.php/about-miccai/awards/young-scientist-impact-award/))
- `2025` CVPR 2025 Outstanding Reviewer Award (Top 5.6%=711/12000+, [Link](https://cvpr.thecvf.com/Conferences/2025/ProgramCommittee#all-outstanding-reviewer))
- `2025` Stanford/Elsevier Top 2% Scientists List 2025 ([Link](https://topscinet.com/scientist_profile/Ji,%20Gepeng/2020/?stype=single_year#google_vignette))
- `2024` MICCAI2024 Young Scientist Publication Impact Award Shortlist
- `2024` Stanford/Elsevier Top 2% Scientists List 2024 ([Link](https://topresearcherslist.com/Home/Profile/924272))
- `2024` CVM Honorable Paper Mention Award in 2023 ([Journal Updates](https://link.springer.com/journal/41095/updates/26965690))
- `2024` MIR Outstanding Reviewer Award in 2023 ([MIR Journal News](https://link.springer.com/journal/11633/updates/26630820))
- `2023` IEEE Transactions on Medical Imaging Distinguished Reviewer (Bronze Level 2022 – 2023)
- `2021` Jittor Developer Conference Distinguish Paper & Most Influential (Application) Paper
- `2021` MICCAI Student Travel Award ([MICCAI link](https://www.miccai2021.org/en/MICCAI-2021-TRAVEL-AWARDS.html))
- `2020` Multimedia Evaluation Benchmark Workshop (Ranking top-1 in terms of accuracy metric)
- `2019` Sparse Representation and Intelligent Analysis Competition of Remote Sensing Images (Co-organized by Huawei Co., LTD \& Wuhan University), Object Detection Track (Ranking: Top6%).

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

# 🔗 Useful Links
- [中国计算机学会(CCF)推荐国际学术会议和期刊目录](https://ccf.atom.im) & [官方公示(2026.03)](https://www.ccf.org.cn/Academic_Evaluation/By_category/)
- [AI conference deadlines](https://github.com/ccfddl/ccf-deadlines)
- [Best Paper Awards in Computer Science (1996-2023)](https://jeffhuang.com/best_paper_awards/)
- [剑桥大学:语言和写作决定人生发展的潜力](https://www.isee-ai.cn/~zhwshi/writing.pdf)