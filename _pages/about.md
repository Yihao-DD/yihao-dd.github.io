---
permalink: /
title: ""
excerpt: "Yihao Wang — M.S. student at the University of Southern California. Self-evolving LLM agents."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


<div class="hp-hero" markdown="1">

# 👋 Hi, I'm Yihao Wang

<p class="hp-sub">M.S. Student · Applied Data Science · University of Southern California</p>

<span class="hp-accent"></span>

</div>

<div class="hp-bio" markdown="1">

I'm Yihao Wang (王奕豪), also known as Ian. I'm an M.S. student in Applied Data Science at the University of Southern California.

I work on self-evolving LLM agents. My recent work is on one narrow step of that loop: how an agent decides to keep a change it just made to itself.

</div>

<div class="hp-section-title"><span class="hp-ico">🔬</span> Research Interests</div>

<div class="hp-interests">
  <div class="hp-card">
    <div class="hp-card-title">Self-Evolving LLM Agents</div>
    <div class="hp-card-desc">Agents that improve by editing their own skills or retraining their own weights.</div>
  </div>
  <div class="hp-card">
    <div class="hp-card-title">Criteria for Self-Modification</div>
    <div class="hp-card-desc">When an update should be accepted, and what it is allowed to break.</div>
  </div>
  <div class="hp-card">
    <div class="hp-card-title">Evaluation Design</div>
    <div class="hp-card-desc">Verifier-based scoring, matched budgets, and testing for capability retention.</div>
  </div>
</div>

<div class="hp-section-title"><span class="hp-ico">🧭</span> Research</div>

<div class="hp-bio" markdown="1">

<div class="hp-pub-title" style="font-size:1.08em; margin-bottom:0.2em;">Capability Retention in Self-Distillation</div>

<p style="margin:0 0 0.9em 0;"><span class="hp-pub-badge hp-pub-badge-review">In progress</span></p>

If an agent is walked through a failure with temporary support and you then train on the repaired trajectory, did it learn the capability or did it learn to rely on the support? I keep the support out of the student's input entirely and remove it at evaluation time. Whether the capability survives that removal is the result.

</div>

<div class="hp-bio" markdown="1">

<div class="hp-pub-title" style="font-size:1.08em; margin-bottom:0.2em;">SAGE: A Statistical Acceptance Gate for Self-Evolving Agents</div>

<p style="margin:0 0 0.9em 0;"><span class="hp-pub-badge hp-pub-badge-review">Under review</span> <span style="font-size:0.88em; color:#777;">2026</span></p>

Self-evolving agents improve by editing a skill document. Almost all prior work went into proposing better edits, and the accept-or-reject step stayed a one-line rule: keep the edit if the average validation score improves. SAGE replaces that rule. It runs the current and edited skill on the same validation items and counts what each edit fixed against what it broke. A break costs more than a fix, and the edit only goes through when the fixes are statistically convincing. When the evidence is thin the gate declines and keeps the current skill.

Tested on 5 benchmarks and 4 open-source models under a matched budget. Harmful edits dropped to zero in 13 of the 20 settings, and the gate produced the best final skill in all 20, beating the previous state of the art by 8.73 points on average.

</div>

<div class="hp-section-title"><span class="hp-ico">📚</span> Publications</div>

<p style="font-size:0.85em; color:#777; margin: 0 0 0.6em 0;">
  <strong style="color:#990000;">Bold</strong> indicates myself.
</p>

<div class="hp-pub-group">
  <div class="hp-pub-group-title">Under Review</div>
  <ol class="hp-pub-list">
    <li class="hp-pub">
      <div class="hp-pub-title">SAGE: A Statistical Acceptance Gate for Self-Evolving Agents</div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-review">Under review</span>
        2026
      </div>
    </li>
  </ol>
</div>

<div class="hp-pub-group">
  <div class="hp-pub-group-title">Conference Papers</div>
  <ol class="hp-pub-list">
    <li class="hp-pub">
      <div class="hp-pub-authors">Jiaqi Li, Qi Pan, <strong>Yihao Wang</strong></div>
      <div class="hp-pub-title">Sentiment Analysis Applied on Amazon Reviews</div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-ei">EI</span>
        International Conference on Machine Learning and Automation (ICMLA 2024)
      </div>
    </li>
    <li class="hp-pub">
      <div class="hp-pub-authors">Jianxin Ye, Zeqiao Huang, <strong>Yihao Wang</strong>, Jinming Chen</div>
      <div class="hp-pub-title">Fine-Grained Classification of Dog Breeds Based on the HERBS Method</div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-ei">EI</span>
        IEEE International Conference on Electrical, Automation and Computer Engineering (ICEACE 2023)
      </div>
    </li>
  </ol>
</div>

<div class="hp-section-title"><span class="hp-ico">📦</span> Earlier Work</div>

<div class="hp-bio" markdown="1">

Before moving to language models I worked on biomedical modeling and imaging.

**Muscle force prediction without EMG.** Five architectures all stalled at R² 0.724 when given joint angles alone. Adding explicit muscle fiber length as an input took it to 0.908. What limited the models was the input representation, not their capacity.

**Ultrasound imaging.** Built the Python pipeline for 3D reconstruction of mouse brain vasculature from plane-wave slices at USC's BioAcoustic Imaging Lab.

**Interpretable disease detection.** A fully classical CT pipeline where every stage can be inspected, using orthogonal moments and metaheuristic feature selection.

</div>

<div class="hp-section-title"><span class="hp-ico">📰</span> News</div>

<ul class="hp-news">
  <li>
    <span class="hp-date">Jul 2026</span>
    <span class="hp-badge">Submitted</span>
    <strong>SAGE</strong> submitted for review.
  </li>
  <li>
    <span class="hp-date">Jul 2026</span>
    <span class="hp-badge">Current</span>
    Started work on <strong>capability retention in self-distillation</strong>.
  </li>
  <li>
    <span class="hp-date">May 2026</span>
    Started work on <strong>SAGE</strong>, a statistical acceptance gate for self-evolving agents.
  </li>
  <li>
    <span class="hp-date">Mar 2025</span>
    <span class="hp-badge">RA</span>
    Joined the <strong>BioAcoustic Imaging Lab</strong> at USC as a Graduate Research Assistant.
  </li>
  <li>
    <span class="hp-date">Jan 2025</span>
    Began the M.S. in Applied Data Science at the <strong>University of Southern California</strong>.
  </li>
  <li>
    <span class="hp-date">Dec 2023</span>
    <span class="hp-badge">Accepted</span>
    Paper <strong>"Fine-Grained Classification of Dog Breeds Based on the HERBS Method"</strong> accepted at <strong>IEEE ICEACE 2023</strong> (EI indexed).
  </li>
</ul>

<div class="hp-section-title"><span class="hp-ico">🎓</span> Education</div>

<ul class="hp-edu">
  <li>
    <span class="hp-edu-school">University of Southern California</span> — M.S. in Applied Data Science
    <div class="hp-edu-meta">Los Angeles, CA, USA · In progress</div>
  </li>
  <li>
    <span class="hp-edu-school">Hong Kong Baptist University</span> — B.Sc. (Honours) in Computer Science
    <div class="hp-edu-meta">Zhuhai, China · 2020 – 2024</div>
  </li>
</ul>

<div class="hp-cta" markdown="1">

💬 **Get in touch.** If my work is close to yours, or you think it is wrong somewhere, I'd like to hear about it. Reach me at [ywang642@usc.edu](mailto:ywang642@usc.edu).

✌️ **Fight On!**

</div>
