---
layout: page
permalink: /phddefence/
title: PhD defence
description: 
nav: false
nav_order: 10
---
<img src="/assets/img/wordcloud_banner.png" alt="wordcloud" width="930"/>

## High Performance Online Deep Neural Network Training from Synthetic Data with Active Learning for Scientific Computing

> or "How to train neural networks to model physical systems accurately — through smarter data, not more compute?"

📅 Date: Tuesday, 21 April 2026, 15:00 (CEST, UTC+2) <br>
📍 Location: France, Grenoble -- UGA Campus, IMAG Building, ground floor, Seminar Room 1 <br>

📜 Manuscript: TBA. <br>
🎞️ Slides: [PDF](/assets/pdf/short.pdf) <br>
🎬 Recording of the defence: [YouTube](https://youtu.be/ze_d4kR1doc) <br>

### Lay Summary

Scientific simulations are expensive. Deep learning surrogates promise to replace them — but training one still requires running hundreds or thousands of simulations, sampled blindly before training even begins. This creates a compounding problem: costly data, poor coverage, and a workflow that cannot adapt to what the model actually needs. The field has focused on building better models; this thesis argues the bottleneck is in the data.

We build on an online training framework [Melissa](https://linktr.ee/melissa.inria) in which simulation data is streamed directly into the training process, removing the need for data storage. Within this setting, we develop active learning methods that monitor training progress and steer data creation toward the most informative configurations -- spending the compute budget where it matters most. The proposed methods are lightweight, model-agnostic, and show consistent gains in surrogate accuracy and reliability across diverse physical systems and model architectures.

### Full Abstract

Numerical simulations of partial differential equations (PDEs) are central to scientific computing, enabling the study of complex physical systems from climate modelling to drug discovery. However, their computational cost often limits their applicability when large numbers of simulations are required. Deep learning offers a promising alternative: neural networks (NNs) can be trained to mimic numerical solvers and deliver orders-of-magnitude prediction speedups and generalisation across a range of system configurations. Yet the training data itself comes from those same solvers. In principle, data can be generated at any desired input configuration, but every sample requires a computationally expensive solver run. Moreover, there is no prior knowledge of which configurations will matter for training.

Traditional workflows require the entire dataset to be generated and stored on disk before training begins, introducing I/O bottlenecks, imposing storage-driven limits on dataset size and fidelity, and forcing the dataset to be fixed upfront, leaving only uninformative priors (e.g., uniform) for configuration sampling. The outcome is datasets that are expensive to produce, store, and load, yet still often unrepresentative, leading to inefficient training and unreliable surrogates. The field has so far focused mainly on model-centric solutions — optimised NN architectures and training objectives -- to improve efficiency and reduce data requirements. These, however, treat the symptom rather than the cause: the data generation and I/O constraints remain unaddressed.

This thesis addresses the problem from a data-centric perspective. We leverage an existing online training framework [Melissa](https://linktr.ee/melissa.inria) that overlaps data creation with surrogate training, streaming simulation data directly into the training process, eliminating the need for storage and the associated I/O bottlenecks. Within this setting, we implement adaptive steering of data creation informed by the training process, and develop query-synthesis active learning methods for online surrogate training. These methods adapt the prior sampling distribution over solver input configurations to expose the NN to more informative training data, aiming to increase generalisation accuracy within a fixed compute budget. The proposed methods are model-agnostic and lightweight, and demonstrate consistent improvements in surrogate reliability and accuracy across a diverse set of PDEs and NN architectures.

<img src="/assets/img/trajectory32-1.png" alt="lines" width="930"/>
