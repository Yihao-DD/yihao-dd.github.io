---
permalink: /
title: ""
excerpt: "Yihao Wang — Research Assistant at Peking University Shenzhen Graduate School; M.S. in Applied Data Science, University of Southern California. Network root-cause analysis and self-evolving LLM agents."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


<div class="hp-hero" markdown="1">

# 👋 Hi, I'm Yihao Wang

<p class="hp-sub">Research Assistant · Peking University Shenzhen Graduate School</p>

<span class="hp-accent"></span>

</div>

<div class="hp-bio" markdown="1">

I'm **Yihao Wang** (王奕豪) — Ian to most people. I'm a research assistant at **Peking University Shenzhen Graduate School**, and I'm applying to Ph.D. programs for fall 2027. I finished my M.S. in Applied Data Science at the **University of Southern California** in August 2026, after a B.Sc. in Computer Science at **Hong Kong Baptist University**.

What I keep coming back to is systems that are supposed to improve on their own — a network that diagnoses its own faults, an agent that rewrites its own skills, a model that trains on its own outputs — and the question of which changes they should trust. Right now that means **root-cause analysis for data-center networks**: a suspected cause is replayed on a physics-structured world model and undone there before anyone acts on the real network. Earlier, **SAGE** asked when a self-evolving agent should accept an edit to itself, and **SAVE** asked how a model can learn from its own failures without an external teacher.

</div>

<div class="hp-section-title"><span class="hp-ico">🔬</span> Research Interests</div>

<div class="hp-interests">
  <div class="hp-card">
    <div class="hp-card-title"><span class="hp-card-star" aria-hidden="true">★</span> Network Root-Cause Analysis <span class="hp-card-note">Current work</span></div>
    <div class="hp-card-desc">Replay a suspected cause on a physics-structured world model, undo it, and check that the symptom disappears — before touching the network.</div>
  </div>
  <div class="hp-card">
    <div class="hp-card-title">Self-Evolving LLM Agents</div>
    <div class="hp-card-desc">Which edits an agent should accept to its own skills, judged on paired per-item evidence rather than an average score.</div>
  </div>
  <div class="hp-card">
    <div class="hp-card-title">Verified Self-Distillation</div>
    <div class="hp-card-desc">Turning a model's own failures into verifier-approved training signal that still holds once the scaffold is removed.</div>
  </div>
</div>

<div class="hp-section-title"><span class="hp-ico">🧭</span> Research</div>

<div class="hp-bio" markdown="1">

<div class="hp-pub-title" style="font-size:1.08em; margin-bottom:0.2em;">Network Root-Cause Analysis</div>

<p style="margin:0 0 0.9em 0;"><span class="hp-pub-badge hp-pub-badge-review">Current work</span> <span style="font-size:0.88em; color:#777;">Peking University · since Sep 2026</span></p>

Root-cause analysis in data-center networks today ends with a label and no way to check it, and a wrong action — closing a lossy link, say — can turn loss into congestion. I treat a root cause as a causal claim: undo it, and the symptom should disappear. To make that claim checkable, the world model combines an analytic skeleton (water-filling bandwidth allocation, DCTCP, hop-by-hop loss), in which every fault enters through an explicit term, with a Transformer residual that learns only what the skeleton misses; it is trained on paired ns-3 twin runs that share seeds, so the effect of a fault or a repair is causal rather than correlational. Inference is propose → verify → abstain → undo: an amortized head nominates 129 candidate causes, "no fault" included; replay likelihood scores each one; the system abstains when the top candidates are too close to call; and undoing the cause in the model predicts whether the symptom actually goes away.

</div>

<div class="hp-bio" markdown="1">

<div class="hp-pub-title" style="font-size:1.08em; margin-bottom:0.2em;">SAGE: A Statistical Acceptance Gate for Self-Evolving Agents</div>

<p style="margin:0 0 0.9em 0;"><span class="hp-pub-badge hp-pub-badge-review">Under review</span> <span style="font-size:0.88em; color:#777;">AAAI 2027 · first author</span></p>

Self-evolving agents improve by editing a skill document. Almost all prior work went into proposing better edits, while the accept-or-reject step stayed a one-line rule: keep the edit if the average validation score goes up. That rule hides what an edit actually did — it can fix a few items while breaking ones the skill already solved — and on a small, noisy validation set it rewards lucky edits as readily as good ones. SAGE runs the current and the edited skill on the same items, counts wins against regressions with a regression costing more than a win, and commits only when a one-sided paired test says the wins are not noise; otherwise it keeps the current skill. The gate reduces exactly to the standard rule at a boundary setting of its parameters.

On 5 benchmarks and 4 open-source models under a matched budget, the regression rate fell in 19 of 20 settings and reached zero in 13, and the final skill scored highest in all 20 — 8.73 points above the previous state of the art on average.

</div>

<div class="hp-bio" markdown="1">

<div class="hp-pub-title" style="font-size:1.08em; margin-bottom:0.2em;">SAVE: Verified Self-Distillation for LLM Agents</div>

<p style="margin:0 0 0.9em 0;"><span class="hp-pub-badge hp-pub-badge-review">Paper in progress</span> <span style="font-size:0.88em; color:#777;">first author</span></p>

STaR-style self-distillation can only learn from trajectories the current model already samples correctly; the inputs it never solves are discarded by rejection sampling, so the model keeps reinforcing what it can already do. SAVE has an agent read those failures, distill the recurring patterns into a temporary harness, and regenerate the failed inputs with the harness in place; only outputs a deterministic verifier accepts are kept, and they are distilled together with the original successes on the plain, scaffold-free inputs. The harness is gone before training and evaluation, so whatever survives is in the weights.

Over five rounds of function-calling self-distillation under matched data, token and step budgets, scaffold-free accuracy reached 95.9% (4,896/5,106), against 71.9% (3,673/5,106) for self-distillation on self-sampled successes alone; a near tie in round 1 widened every round to a 24.0-point gap.

</div>

<div class="hp-section-title"><span class="hp-ico">📚</span> Publications</div>

<p style="font-size:0.85em; color:#777; margin: 0 0 0.6em 0;">
  <strong style="color:#990000;">Bold</strong> indicates myself.
</p>

<div class="hp-pub-group">
  <div class="hp-pub-group-title">Under Review</div>
  <ol class="hp-pub-list">
    <li class="hp-pub">
      <div class="hp-pub-authors"><strong>Yihao Wang</strong> et al.</div>
      <div class="hp-pub-title">SAGE: A Statistical Acceptance Gate for Self-Evolving Agents</div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-review">Under review</span>
        AAAI 2027
      </div>
    </li>
    <li class="hp-pub">
      <div class="hp-pub-authors">Linhan Xia, Rui Liu, Zhaofeng Zhang, <strong>Yihao Wang</strong>, Shengxin Zhu</div>
      <div class="hp-pub-title">LoCA: Forward-Only LLM Tuning after One-Shot Calibration with Local Credit Assignment</div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-review">Under review</span>
        AAAI 2027
      </div>
    </li>
  </ol>
</div>

<div class="hp-pub-group">
  <div class="hp-pub-group-title">Conference Papers</div>
  <ol class="hp-pub-list">
    <li class="hp-pub">
      <div class="hp-pub-authors">Jiaqi Li, Qi Pan, <strong>Yihao Wang</strong></div>
      <div class="hp-pub-title"><a href="https://doi.org/10.54254/2755-2721/44/20230079" target="_blank" rel="noopener">Sentiment Analysis Applied on Amazon Reviews</a></div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-ei">EI</span>
        International Conference on Machine Learning and Automation, in <em>Applied and Computational Engineering</em> 44 (2024)
      </div>
    </li>
    <li class="hp-pub">
      <div class="hp-pub-authors">Jianxin Ye, Zeqiao Huang, <strong>Yihao Wang</strong>, Jinming Chen</div>
      <div class="hp-pub-title"><a href="https://ieeexplore.ieee.org/document/10441854" target="_blank" rel="noopener">Fine-Grained Classification of Dog Breeds Based on the HERBS Method</a></div>
      <div class="hp-pub-venue">
        <span class="hp-pub-badge hp-pub-badge-ei">EI</span>
        IEEE International Conference on Electrical, Automation and Computer Engineering (ICEACE 2023)
      </div>
    </li>
  </ol>
</div>

<div class="hp-section-title"><span class="hp-ico">📦</span> Earlier Work</div>

<div class="hp-bio" markdown="1">

Before language models I worked on biomedical modeling and imaging. The lesson that stuck: the input representation, not the model, usually sets the ceiling.

**Muscle force prediction without EMG.** Five architectures all stalled at R² 0.724 when given joint angles alone. Adding explicit muscle fiber length as an input took it to 0.908.

**Ultrasound imaging.** Built the Python pipeline for 3D reconstruction of mouse brain vasculature from plane-wave slices at USC's BioAcoustic Imaging Lab.

**Interpretable disease detection.** A fully classical CT pipeline where every stage can be inspected, using orthogonal moments and metaheuristic feature selection.

</div>

<div class="hp-section-title"><span class="hp-ico">📰</span> News</div>

<ul class="hp-news">
  <li>
    <span class="hp-date">Sep 2026</span>
    <span class="hp-badge">RA</span>
    Joined <strong>Peking University Shenzhen Graduate School</strong> as a Research Assistant; started work on <strong>network root-cause analysis</strong>.
  </li>
  <li>
    <span class="hp-date">Aug 2026</span>
    <span class="hp-badge">Graduated</span>
    Completed the M.S. in Applied Data Science at the <strong>University of Southern California</strong>.
  </li>
  <li>
    <span class="hp-date">Aug 2026</span>
    <span class="hp-badge">Submitted</span>
    <strong>SAGE</strong> (first author) and <strong>LoCA</strong> (co-author) submitted to <strong>AAAI 2027</strong>; both under review.
  </li>
  <li>
    <span class="hp-date">Jun 2026</span>
    Started work on <strong>SAVE</strong>, verified self-distillation for LLM agents.
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

<div class="hp-section-title"><span class="hp-ico">🎓</span> Education & Appointments</div>

<ul class="hp-edu">
  <li>
    <span class="hp-edu-school">Peking University Shenzhen Graduate School</span> — Research Assistant
    <div class="hp-edu-meta">Shenzhen, China · Sep 2026 – present</div>
  </li>
  <li>
    <span class="hp-edu-school">University of Southern California</span> — M.S. in Applied Data Science
    <div class="hp-edu-meta">Los Angeles, CA, USA · Jan 2025 – Aug 2026</div>
  </li>
  <li>
    <span class="hp-edu-school">Hong Kong Baptist University</span> — B.Sc. (Honours) in Computer Science and Technology
    <div class="hp-edu-meta">Zhuhai, China · 2020 – 2024</div>
  </li>
</ul>

<div class="hp-cta" markdown="1">

💬 **Get in touch.** If my work is close to yours, or you think it is wrong somewhere, I'd like to hear about it. Reach me at [ywang642@usc.edu](mailto:ywang642@usc.edu). My CV is [here](/files/Yihao_Wang_CV.pdf).

✌️ **Fight On!**

</div>
