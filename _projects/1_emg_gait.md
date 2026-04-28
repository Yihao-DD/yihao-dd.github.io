---
layout: page
title: EMG-Free Gait Muscle-Force Prediction
description: Predicting lower-limb muscle forces during gait without EMG input — a deep learning pipeline trained on 49-subject leave-one-subject-out evaluation.
importance: 1
category: research
related_publications: false
---

A subject-independent pipeline that recovers AnyBody-reference muscle forces from gait kinematics alone, evaluated leave-one-subject-out across 49 subjects.

The central finding is a **state-representation bottleneck**: models conditioned on joint angles alone saturate at R² ≈ 0.724, while adding explicit muscle fiber length lifts performance to **R² ≈ 0.908**. A no-ground-reaction-force variant still retains R² ≈ 0.895, suggesting fiber length is the dominant recoverable geometric state for this task.

Ongoing analyses cover ablation, robustness under noise, per-muscle accuracy, and validation on the Grand Challenge knee-contact dataset.

*University of Southern California &nbsp;·&nbsp; Feb 2026 – present*
