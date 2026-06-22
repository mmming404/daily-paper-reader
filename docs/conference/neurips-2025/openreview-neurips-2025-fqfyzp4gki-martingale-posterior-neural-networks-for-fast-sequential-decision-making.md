---
title: Martingale Posterior Neural Networks for Fast Sequential Decision Making
title_zh: 鞅后验神经网络用于快速序贯决策
authors: "Gerardo Duran-Martin, Leandro Sánchez-Betancourt, Alvaro Cartea, Kevin Patrick Murphy"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=fqfYzp4GKi"
tags: ["query:ts-forecast"]
score: 6.0
evidence: 鞅后验预测用于序贯决策，可应用于概率预测
tldr: 本文提出基于鞅后验的预测优先方法，直接用神经网络参数化一步超前预测后验，通过类卡尔曼滤波递归更新，实现快速贝叶斯序贯决策。该方法将贝叶斯决策与参数空间推断解耦，可有效用于序列预测任务中的不确定性量化，为概率时间序列预测提供了一种高效的在线学习框架。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1003, \"height\": 500, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1136, \"height\": 377, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1294, \"height\": 382, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1291, \"height\": 524, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1274, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1425, \"height\": 482, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1273, \"height\": 740, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1424, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1417, \"height\": 479, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1142, \"height\": 688, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1436, \"height\": 705, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1142, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1435, \"height\": 710, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1212, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1423, \"height\": 527, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1429, \"height\": 716, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1425, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1431, \"height\": 715, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-fqfyzp4gki/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1139, \"height\": 812, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-fqfyzp4gki/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fqfyzp4gki/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 812, \"height\": 210, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fqfyzp4gki/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1457, \"height\": 2266, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fqfyzp4gki/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1275, \"height\": 178, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fqfyzp4gki/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 973, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-fqfyzp4gki/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 523, \"height\": 680, \"label\": \"Table\"}]"
motivation: 传统贝叶斯神经网络参数空间推断复杂，不便于快速序贯决策。
method: 采用鞅后验预测优先视角，用神经网络建模一步预测后验并在线更新。
result: 算法在决策任务中效率高且提供校准不确定性。
conclusion: 为概率预测提供了解耦参数推断的快速决策方案。
---

## Abstract
We introduce scalable algorithms for online learning of neural network parameters and Bayesian sequential decision making.
Unlike classical Bayesian neural networks,
which induce predictive uncertainty through a posterior over model parameters,
our methods adopt a predictive-first perspective based on martingale posteriors.
In particular, we work directly with the one-step-ahead posterior predictive, which we
parameterize with a neural network and update sequentially with incoming observations.
This decouples Bayesian decision-making from parameter-space inference:
we sample from the posterior predictive for decision making,
and update the parameters of the posterior predictive via fast, frequentist Kalman-filter-like
recursions. 
Our algorithms operate in a fully online, replay-free setting, providing principled uncertainty quantification without costly posterior sampling.
Empirically, they achieve competitive performance–speed trade-offs in non-stationary contextual bandits and Bayesian optimization,
offering 10–100 times faster inference than classical Thompson sampling while maintaining comparable or superior decision performance.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
鞅后验预测用于序贯决策，可应用于概率预测。

### 2. 核心内容
本文提出基于鞅后验的预测优先方法，直接用神经网络参数化一步超前预测后验，通过类卡尔曼滤波递归更新，实现快速贝叶斯序贯决策。该方法将贝叶斯决策与参数空间推断解耦，可有效用于序列预测任务中的不确定性量化，为概率时间序列预测提供了一种高效的在线学习框架。

### 3. 对应检索需求
advances in probabilistic time series forecasting models。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=fqfYzp4GKi](https://openreview.net/forum?id=fqfYzp4GKi)
