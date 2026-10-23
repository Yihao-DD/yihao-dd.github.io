---
permalink: /zh/
title: ""
excerpt: "王奕豪 — 北京大学深圳研究生院研究助理；南加州大学应用数据科学硕士。网络根因分析与自进化智能体。"
author_profile: true
lang: zh
---


<div class="hp-hero" markdown="1">

# 👋 你好，我是王奕豪

<p class="hp-sub">研究助理 · 北京大学深圳研究生院</p>

<span class="hp-accent"></span>

</div>

<div class="hp-bio" markdown="1">

我是 **王奕豪**（Yihao Wang），英文名 Ian。目前在**北京大学深圳研究生院**担任研究助理，正在申请 2027 年秋季入学的博士项目。2026 年 8 月于**南加州大学**取得应用数据科学硕士学位，本科毕业于**香港浸会大学**计算机科学专业。

我关心的是那些"应该能自己变好"的系统——能自己诊断故障的网络、能改写自身技能的智能体、能用自己的输出训练自己的模型——以及它们应该相信哪些改变。现在做的是**数据中心网络的根因分析**：把疑似根因放到一个物理结构化的世界模型上回放并撤销，确认之后再去动真实网络。此前，**SAGE** 研究自进化智能体何时应该接受对自身的修改，**SAVE** 研究模型如何在没有外部教师的情况下从自己的失败中学习。

</div>

<div class="hp-section-title"><span class="hp-ico">🔬</span> 研究兴趣</div>

<div class="hp-interests">
  <div class="hp-card">
    <div class="hp-card-title"><span class="hp-card-star" aria-hidden="true">★</span> 网络根因分析 <span class="hp-card-note">当前工作</span></div>
    <div class="hp-card-desc">在物理结构化的世界模型上回放疑似根因、撤销它、确认症状消失——然后才动网络。</div>
  </div>
  <div class="hp-card">
    <div class="hp-card-title">自进化智能体</div>
    <div class="hp-card-desc">智能体应该接受哪些对自身技能的修改：依据逐题配对的证据，而不是一个平均分。</div>
  </div>
  <div class="hp-card">
    <div class="hp-card-title">可验证的自蒸馏</div>
    <div class="hp-card-desc">把模型自己的失败变成经验证器确认的训练信号，并且在去掉脚手架之后仍然成立。</div>
  </div>
</div>

<div class="hp-section-title"><span class="hp-ico">🧭</span> 研究工作</div>

<div class="hp-bio" markdown="1">

<div class="hp-pub-title" style="font-size:1.08em; margin-bottom:0.2em;">网络根因分析</div>

<p style="margin:0 0 0.9em 0;"><span class="hp-pub-badge hp-pub-badge-review">当前工作</span> <span style="font-size:0.88em; color:#777;">北京大学 · 2026 年 9 月起</span></p>

今天的数据中心网络根因分析只输出一个标签，没有办法检验；错误的处置（比如关掉一条丢包链路）会把丢包变成拥塞。我把根因当作一个因果主张：撤销它，症状就应该消失。为了让这个主张可检验，世界模型由一个解析骨架（water-filling 带宽分配、DCTCP、逐跳丢包）和一个 Transformer 残差组成——每种故障通过显式的项进入骨架，残差只学骨架没覆盖的部分；训练数据是共享随机种子的 ns-3 孪生仿真，因此故障和修复的效应是因果的而不是相关的。推断分四步：提议 → 验证 → 弃权 → 撤销——一个摊销头提名 129 个候选根因（含"无故障"），回放似然给每个候选打分，前几名难分高下时弃权，在模型里撤销根因来预测症状是否真的消失。

</div>

<div class="hp-bio" markdown="1">

<div class="hp-pub-title" style="font-size:1.08em; margin-bottom:0.2em;">SAGE：自进化智能体的统计接受门</div>

<p style="margin:0 0 0.9em 0;"><span class="hp-pub-badge hp-pub-badge-review">审稿中</span> <span style="font-size:0.88em; color:#777;">AAAI 2027 · 第一作者</span></p>

自进化智能体通过修改一份技能文档来变强。此前的工作几乎都在研究怎样提出更好的修改，而"收不收"这一步一直是一条规则：验证集平均分涨了就收。这条规则看不见一次修改到底做了什么——它可能修好几道题、同时弄坏技能原本已经会的题——而且在小而有噪声的验证集上，运气好的修改和真正好的修改得到同样的奖励。SAGE 让当前技能和修改后的技能在同一批题上逐题比较，统计赢和退步，一次退步的代价高于一次赢；只有当单侧配对检验表明赢不是噪声时才接受，否则保留当前技能。在参数的边界取值下，SAGE 恰好退化为标准规则。

在 5 个基准、4 个开源模型、同等预算下，20 个设置里有 19 个回退率下降、13 个降到零；最终技能在全部 20 个设置中得分最高，平均比此前的最好方法高 8.73 分。

</div>

<div class="hp-bio" markdown="1">

<div class="hp-pub-title" style="font-size:1.08em; margin-bottom:0.2em;">SAVE：面向 LLM 智能体的可验证自蒸馏</div>

<p style="margin:0 0 0.9em 0;"><span class="hp-pub-badge hp-pub-badge-review">论文撰写中</span> <span style="font-size:0.88em; color:#777;">第一作者</span></p>

STaR 式的自蒸馏只能从当前模型已经能采样正确的轨迹里学习；它从来做不对的输入会被拒绝采样丢掉，于是模型只是在强化自己已会的东西。SAVE 让一个智能体阅读这些失败，把反复出现的失败模式提炼成一个临时 harness，带着 harness 重新生成失败的输入；只保留确定性验证器通过的输出，再和原有的成功轨迹一起、在不带脚手架的原始输入上做蒸馏。训练和评测时 harness 都已去掉，留下来的东西都在权重里。

在 function calling 任务上做五轮自蒸馏、数据量 / token / 步数预算全部对齐：去脚手架的准确率达到 95.9%（4,896/5,106），而只用自采样成功轨迹的自蒸馏为 71.9%（3,673/5,106）；第一轮几乎持平，差距逐轮扩大到 24.0 分。

</div>

<div class="hp-section-title"><span class="hp-ico">📚</span> 学术发表</div>

<p style="font-size:0.85em; color:#777; margin: 0 0 0.6em 0;">
  <strong style="color:#990000;">加粗</strong>表示本人。
</p>

<div class="hp-pub-group">
  <div class="hp-pub-group-title">审稿中</div>
  <ol class="hp-pub-list">
    <li class="hp-pub">
      <div class="hp-pub-authors"><strong>Yihao Wang</strong> et al.</div>
      <div class="hp-pub-title">SAGE: A Statistical Acceptance Gate for Self-Evolving Agents</div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-review">审稿中</span>
        AAAI 2027
      </div>
    </li>
    <li class="hp-pub">
      <div class="hp-pub-authors">Linhan Xia, Rui Liu, Zhaofeng Zhang, <strong>Yihao Wang</strong>, Shengxin Zhu</div>
      <div class="hp-pub-title">LoCA: Forward-Only LLM Tuning after One-Shot Calibration with Local Credit Assignment</div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-review">审稿中</span>
        AAAI 2027
      </div>
    </li>
  </ol>
</div>

<div class="hp-pub-group">
  <div class="hp-pub-group-title">会议论文</div>
  <ol class="hp-pub-list">
    <li class="hp-pub">
      <div class="hp-pub-authors">Jiaqi Li, Qi Pan, <strong>Yihao Wang</strong></div>
      <div class="hp-pub-title"><a href="https://doi.org/10.54254/2755-2721/44/20230079" target="_blank" rel="noopener">Sentiment Analysis Applied on Amazon Reviews</a></div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-ei">EI</span>
        国际机器学习与自动化会议，刊于 <em>Applied and Computational Engineering</em> 44（2024）
      </div>
    </li>
    <li class="hp-pub">
      <div class="hp-pub-authors">Jianxin Ye, Zeqiao Huang, <strong>Yihao Wang</strong>, Jinming Chen</div>
      <div class="hp-pub-title"><a href="https://ieeexplore.ieee.org/document/10441854" target="_blank" rel="noopener">Fine-Grained Classification of Dog Breeds Based on the HERBS Method</a></div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-ei">EI</span>
        IEEE 电气、自动化与计算机工程国际会议（ICEACE 2023）
      </div>
    </li>
  </ol>
</div>

<div class="hp-section-title"><span class="hp-ico">📦</span> 早期工作</div>

<div class="hp-bio" markdown="1">

在转向语言模型之前，我做生物医学建模与成像。留下的一条经验：决定上限的通常是输入表示，而不是模型。

**无需肌电的肌力预测。** 只给关节角度时，五种网络结构全部停在 R² 0.724；把肌纤维长度作为显式输入后提高到 0.908。

**超声成像。** 在南加州大学 BioAcoustic Imaging Lab 搭建了从平面波切片重建小鼠脑血管三维结构的 Python 流水线。

**可解释的疾病检测。** 一条完全经典的 CT 流水线，每一步都可以检查：正交矩特征加元启发式特征选择。

</div>

<div class="hp-section-title"><span class="hp-ico">📰</span> 最新动态</div>

<ul class="hp-news">
  <li>
    <span class="hp-date">2026 年 9 月</span>
    <span class="hp-badge">RA</span>
    加入<strong>北京大学深圳研究生院</strong>担任研究助理，开始<strong>网络根因分析</strong>的工作。
  </li>
  <li>
    <span class="hp-date">2026 年 8 月</span>
    <span class="hp-badge">毕业</span>
    完成<strong>南加州大学</strong>应用数据科学硕士学位。
  </li>
  <li>
    <span class="hp-date">2026 年 8 月</span>
    <span class="hp-badge">已投稿</span>
    <strong>SAGE</strong>（第一作者）与 <strong>LoCA</strong>（合作者）投稿 <strong>AAAI 2027</strong>，审稿中。
  </li>
  <li>
    <span class="hp-date">2025 年 3 月</span>
    <span class="hp-badge">RA</span>
    加入南加州大学 <strong>BioAcoustic Imaging Lab</strong> 担任研究助理。
  </li>
  <li>
    <span class="hp-date">2025 年 1 月</span>
    进入<strong>南加州大学</strong>攻读应用数据科学硕士。
  </li>
</ul>

<div class="hp-section-title"><span class="hp-ico">🎓</span> 教育与任职</div>

<ul class="hp-edu">
  <li>
    <span class="hp-edu-school">北京大学深圳研究生院</span> — 研究助理
    <div class="hp-edu-meta">中国深圳 · 2026 年 9 月至今</div>
  </li>
  <li>
    <span class="hp-edu-school">南加州大学</span> — 应用数据科学硕士
    <div class="hp-edu-meta">美国洛杉矶 · 2025 年 1 月 – 2026 年 8 月</div>
  </li>
  <li>
    <span class="hp-edu-school">香港浸会大学</span> — 计算机科学与技术理学学士（荣誉）
    <div class="hp-edu-meta">中国珠海 · 2020 – 2024</div>
  </li>
</ul>

<div class="hp-cta" markdown="1">

💬 **欢迎联系。** 如果你的工作和我的相近，或者觉得我哪里做错了，都欢迎告诉我：[ywang642@usc.edu](mailto:ywang642@usc.edu)。简历在[这里](/files/Yihao_Wang_CV.pdf)。

✌️ **Fight On!**

</div>
