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

大家好！我是**李博文**，目前是本科三年级学生，就读于[华中科技大学网络空间安全学院](https://cse.hust.edu.cn/index.htm)信息安全专业。

我对人工智能充满热情，自入学以来，积极参与各类科研项目和学术竞赛，曾获得**华中科技大学本科特优生**（1%）、2021-2022年度**国家奖学金**及多项校内表彰。在科研方面，我参与并主导了多个项目，包括但不限于**计算机视觉与其安全问题**、**大语言模型与其安全问题**等领域。

# 🎓 Education Background

- **排名：** GPA 排名：**3/98 (3.1%)**、加权平均分排名：**3/98 (3.1%)** <span style="font-size: 15px;">[[排名证明]](https://lbw15507.github.io/docs/paimingzhengming.pdf)</span>  
- **成绩均分：** GPA：4.65/5.0、加权平均分：92.48/100  
- **语言能力：** 已通过 CET4 和 CET6，具有长期阅读英文文献的习惯，多次参与全英学术论文的撰写与投稿  
- **核心课程：** 微积分上 (100)、微积分下 (100)、线性代数 (94)、概率论与数理统计 (93)、离散数学 (93, 97)、数据结构 (96, 98)、算法设计与分析 (98)、汇编语言程序设计 (94, 97)、编译原理 (95, 96)、计算机组成原理 (93, 99)、操作系统原理 (90, 95)、密码学 (94, 98)、软件安全 (94, 98)  
- **编程能力：** 熟练掌握 C/C++ 和 Python，曾获多项编程类和算法类赛事的国家级奖项，代码能力强；熟练掌握 PyTorch，熟悉各类深度学习模型及其编程实现，曾获蓝桥杯 AI 编程赛国家级奖项；长期担任数学建模竞赛编程手，熟练使用 Python 和 MATLAB 进行建模编程，获多项数学建模奖项  
- **在校荣誉：** 曾获 **华中科技大学本科特优生** (全校前1%) <span style="font-size: 15px;">[[证明]](https://lbw15507.github.io/docs/HUSTteyousheng.pdf)</span>，2021-2022年度 **国家奖学金** <span style="font-size: 15px;">[[证明]](https://lbw15507.github.io/docs/guojiang.pdf)</span>

# 🔥 News

# 🔍 Research Experience-Computer Vision and Security

## **💡💡💡 NumbOD - 空域频域混合攻击方法研究** <sub> &nbsp;&nbsp;[[OpenReview]](https://lbw15507.github.io/docs/AAAI25openreview.jpg)</sub>

- **时间：** 2023.9 - 2024.7  
- **领域：** **计算机视觉（目标检测）、对抗攻击**  
- **角色：** 第二作者  
- **研究背景：**  
  1. 随着深度学习的快速发展，各种架构的目标检测器（ODs）在自动驾驶等复杂场景中取得了重大成功。
  2. 先前针对 ODs 的对抗性攻击主要集中在设计针对其特定结构（如 NMS 和 RPN）的定制攻击，这些方法虽然有效，但其可扩展性受限。
  3. 针对 ODs 的大多数攻击努力来源于最初为分类任务设计的图像级攻击，这可能导致在与目标对象无关的区域（如背景）进行冗余计算和干扰。
  4. 因此，如何设计一种高效的、模型不可知的攻击方法来全面评估 ODs 的漏洞仍是一个挑战和未解决的问题。
- **我们的方法：**  
  1. 针对空域和频域的攻击进行了设计，提出了一种全新的针对目标检测器的空域频域混合攻击方法：
     - **空域攻击：** 从回归和分类角度为图像中的物体分配候选框作为攻击目标，通过策略性地添加噪声来改变目标的位置、大小和标签。
     - **频域攻击：** 应用离散小波变换将图像划分为高频和低频分量，将噪声集中在语义相关的高频区域，减少对非关键目标的无效攻击。
  2. 实现了针对 8 个检测模型的端到端空域频域混合攻击，这是首个通用的对抗攻击框架，显著提高了对各种模型的攻击效果。
- **项目成果：**  
  * 相关论文已完成，初版投稿于 **ACM MM**，但未被收录（获得 borderline 评价）。根据审稿意见进行大幅改进后，论文已重新投稿至 **AAAI 2025**（第二作者）。

---

## **💡💡 CumFormer - 基于渐进式域间隙解耦的大雾场景语义分割** <sub> &nbsp;&nbsp;[[项目主页]](https://lbw15507.github.io/CumFormer/README.html) | [[项目代码]](https://github.com/lbw15507/CumFormer)</sub>

- **时间：** 2023.11 - 2024.5  
- **领域：** **计算机视觉、域适应**  
- **角色：** 第三作者  
- **研究背景：**  
  1. 当前语义分割模型大多基于清晰场景的图片进行训练，极少考虑恶劣天气的影响，这导致它们在恶劣天气下的表现不佳，特别是在雾天场景的语义分割中表现尤为差劲。
  2. 许多现有方法使用领域自适应技术将分割知识从清晰场景转移到模糊场景，但由于雾导致的图像质量下降和不同城市风格之间的域差异大，这些方法的效果并不理想。
  3. 最新研究尝试引入一个中间域来解耦域间隙，并逐步实现雾天场景的语义分割，但这种方法对中间域信息的探索仍不足。
- **我们的方法：**  
  1. 针对语义分割模型在恶劣天气视觉场景中的局限性，采用多层次教师自训练方法：将大的域差距拆解为多个小的域差距，对应不同的任务，以控制模型在自训练过程中的域差距。
  2. 结合交替训练策略，充分利用源域的参考信息，逐步提升从源域迁移到目标域的分割能力，展示出优异的抗雾干扰性能。
- **项目成果：**  
  * 相关工作已完成，正在参加**第二十六届中国机器人及人工智能大赛**，并已**进入国赛阶段**。
  * 论文撰写中，计划完稿后投稿至 **IEEE TIP (CCF-A)**（第三作者）。

---

## **💡💡 MODnet++ - 基于 Encoder-Decoder 架构的双轨视频人像分割**

- **时间：** 2022.12 - 2023.8  
- **领域：** **计算机视觉（语义分割）**  
- **角色：** 团队负责人  
- **研究背景：**  
  1. 当前，深度学习在人像分割应用中取得了显著成果，但仍存在优化空间：
     - 现有方法在细节和边缘分割上不够精细。
     - 高计算成本导致模型运行速度较慢，不适合实时应用。
- **我们的方法：**  
  1. 设计了一个基于 MODNet 的轻量级抠图目标分解模型，使用编码器提取空间特征，递归解码器提取视频时序特征：
     - 在编码器中，使用 MobileNetV3-large 作为骨干网络，提取多尺度特征层，并加入交叉注意力模块以增强网络表达能力。
     - 在递归解码器中，使用 convGRU 提取时序信息，充分利用视频连续帧之间的关联。
     - 对编码器和递归解码器输出的 Alpha matte 进行补丁修复，实现对图像细节部分的精细分割。
  2. 结合知识蒸馏技术，实现了高精度和轻量化的视频人像分割效果。
- **项目成果：**  
  * 该项目成果已申请**校级大学生创新创业项目（团队负责人）**。

# 🧠 Research Experience-Large Language Models

## **💡 LLMPLA - 针对LLM应用程序的系统提示窃取攻击**

- **时间：** 2024.4 - 2024.8  
- **领域：** **大语言模型、人工智能安全、系统提示符窃取**  
- **角色：** 第一作者（实验阶段）  
- **研究背景：**  
  1. LLM应用程序是指托管在GPT Store等平台上，用户可以使用它们来解决各种明确的下游任务（如高质量翻译、定制的Web搜索体验等）的新兴应用程序。
  2. LLM应用程序的具体工作流程涉及接收来自用户的查询，将其与系统提示符相结合构造提示，发送给后端的LLM，并将响应返回给用户以完成相应功能。
  3. 这些应用程序的功能和性能高度依赖于它的系统提示符，通常被视为开发者的知识产权。
  4. 通过提示泄漏攻击窃取系统提示符会严重威胁开发人员的知识产权，因此，设计一种高效的系统提示窃取攻击来评估相关漏洞迫在眉睫。
- **我们的方法：**  
  1. 受到现有越狱攻击的启发，我们将查询优化为对抗性查询，使得目标LLM应用程序更可能在输入时显示其系统提示符。
  2. 我们将此问题视作一个优化问题，涉及影子系统提示符和影子LLM的数据集，优化目标是找到一个对抗性查询，使影子LLM应用程序输出其影子系统提示符作为响应。
- **项目进展：**  
  * 目前正处于实验阶段，且**实验效果较为良好**。

---

## **💡 FuzzJailbreaker - 用于发现Jailbreak的通用模糊测试框架** <sub> &nbsp;&nbsp;[[项目主页]](https://lbw15507.github.io/Demo_FuzzJailbreaker/) | [[项目代码]](https://github.com/lbw15507/FuzzJailbreaker)</sub>

- **时间：** 2024.3 - 2024.8  
- **领域：** **大语言模型、人工智能安全**  
- **角色：** 团队（主力成员）  
- **研究背景：**  
  1. LLMs的普及引入了安全风险，尤其是越狱漏洞问题。
  2. 尽管LLM提供者（如OpenAI）不断更新模型版本和防御机制来修补漏洞，但这种攻防之间的“猫鼠游戏”使得模型所有者长期处于被动防御状态。
  3. 现有的安全微调机制受限于高质量标记数据的稀缺，且往往未能全面公开测试数据集，导致无法防护所有越狱类别，只能对已知越狱Prompt进行防护。
  4. 频繁的安全性迭代需要高昂的人力成本。
- **我们的方法：**  
  1. 参考传统安全中的模糊测试思路，将越狱Prompt解构为模糊模板、约束条件和非法问题，并自动生成大量随机但结构化的越狱Prompt来测试模型。
  2. 建立了一套高度自动化的流程，从自动生成越狱Prompt到模型测试再到结果标注评估，均无需人工干预。
- **项目进展：**  
  * 已完成相关工作，正在参与**“挑战杯”全国大学生课外学术科技作品竞赛揭榜挂帅赛道**。
  * **已与复旦团队研发的统一越狱框架EasyJailbreak取得联系并加入其开源框架**。

---

## **💡 Kaggle: LMSYS-Chatbot Arena Human Preference Predictions** <sub> &nbsp;&nbsp;[[比赛介绍]](https://www.kaggle.com/competitions/lmsys-chatbot-arena)</sub>

- **时间：** 2024.5 - 2024.8  
- **领域：** **大语言模型、LLM问答**  
- **角色：** 团队（主力成员）  
- **研究背景：**  
  * 本次比赛的目标是预测用户在两个人工智能对话系统（LLM）之间的对决中更偏爱哪个回答。参赛者将获得一组来自Chatbot Arena的对话数据（这些对话由不同的LLM生成回答），通过开发一个获胜的机器学习模型，帮助改进聊天机器人与人类互动的方式，并确保它们更好地符合人类的偏好。
- **项目成果：**  
  * 获得了0.99268的Final Score，最终摘得本次竞赛的**银牌（Top 4.5%）**。&nbsp;<span style="font-size: 16px;">
    <a href="https://lbw15507.github.io/docs/AWARDkaggleLMSYS.png">[证明]</a></span>

---

## **💡 Kaggle: LLM Prompt Recovery** <sub> &nbsp;&nbsp;[[比赛介绍]](https://www.kaggle.com/competitions/llm-prompt-recovery)</sub>

- **时间：** 2024.2 - 2024.4  
- **领域：** **大语言模型、Prompt还原**  
- **角色：** 团队（主力成员）  
- **研究背景：**  
  * NLP的工作流程越来越多地涉及重写文本，但如何有效地恢复LLM Prompt还存在很大的优化空间。本次比赛旨在恢复用于重写给定文本的LLM Prompt，参赛者将根据1300多篇原始文本的数据集进行测试，每篇文本都与来自Gemma（Google的开放模型系列）的重写版本配对。
- **项目成果：**  
  * 获得了0.6619的Final Score，最终摘得本次竞赛的**银牌（Top 2.7%）**。&nbsp;<span style="font-size: 16px;">
    <a href="https://lbw15507.github.io/docs/AWARDkagglepromptrecovery.png">[证明]</a></span>

---

## **💡 Kaggle: LLM Science Exam** <sub> &nbsp;&nbsp;[[比赛介绍]](https://www.kaggle.com/competitions/kaggle-llm-science-exam/)</sub>

- **时间：** 2023.7 - 2023.10  
- **领域：** **大语言模型、LLM for Science**  
- **角色：** 团队（主力成员）  
- **研究背景：**  
  * 本次比赛的参赛者将回答由大型语言模型编写的科学难题，比赛的进展可以帮助研究人员更好地了解LLM自我测试的能力和在资源受限环境下运行的LLM的潜力。
- **项目成果：**  
  * 获得了0.903094的Final Score，最终摘得本次竞赛的**铜牌（Top 5.2%）**。&nbsp;<span style="font-size: 16px;">
    <a href="https://lbw15507.github.io/docs/AWARDkagglellmscienceexam.png">[证明]</a></span>

# 🏆 Competition Awards

- **Kaggle: Chatbot Arena Human Preference Predictions：银牌** *国家级* 2024 &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/AWARDkaggleLMSYS.png)  
- **Kaggle: LLM Prompt Recovery：银牌** *国家级* 2024 &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/AWARDkagglepromptrecovery.png)  
- **Kaggle: LLM Science Exam：铜牌** *国家级* 2024 &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/AWARDkagglellmscienceexam.png)  
- **蓝桥杯项目实战赛人工智能赛道(全国总决赛)：三等奖** *国家级* 2024 &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/AWARDlanqiaobeiAIguo.pdf)  
- **睿抗机器人开发者大赛编程技能赛(全国总决赛)：三等奖** *国家级* 2024 &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/AWARDraicomguo.pdf)  
- **“华数杯”全国大学生数学建模竞赛(全国总决赛)：二等奖** *国家级* 2022 &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/AWARDhuashubei.pdf)  
- **全国大学生数学竞赛(非数学类)：一等奖** *国家级* 2022 &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/AWARDshuxuejingsaiguo.pdf)  
- **美国大学生数学建模竞赛：H奖** *国际级* 2023 &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/meisaiH.pdf)  
- **睿抗机器人开发者大赛编程技能赛(湖北赛区)：二等奖** *省部级* 2024 &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/AWARDraicomsheng.pdf)  

# 🥇 Scholarships and Honors

- **2021-2022** 国家奖学金（该年度年级成绩排名：3/98，前3.1%）*华中科技大学* &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/guojiang.pdf)  
- **2022-2023** 华中科技大学本科特优生（全校前1%）*华中科技大学* &nbsp;&nbsp;[[证明]](https://lbw15507.github.io/docs/HUSTteyousheng.pdf)   

# 📖 Educations

- **2021.9 - 至今**，本科生，华中科技大学，专业：信息安全  
