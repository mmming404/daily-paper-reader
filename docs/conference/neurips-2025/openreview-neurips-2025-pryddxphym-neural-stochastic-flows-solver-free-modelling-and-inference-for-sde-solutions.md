---
title: "Neural Stochastic Flows: Solver-Free Modelling and Inference for SDE Solutions"
title_zh: 神经随机流：SDE解的免求解器建模与推断
authors: "Naoki Kiyohara, Edward Johns, Yingzhen Li"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=PrYDDxphym"
tags: ["query:ts-forecast"]
score: 8.0
evidence: 基于条件归一化流的免求解器SDE建模，适用于随机时间序列
tldr: 针对传统SDE建模需昂贵数值求解器的问题，本文提出神经随机流（NSF），利用条件归一化流直接学习SDE转移规律，实现任意时间点间的单步采样，速度提升可达两个数量级。该方法能有效处理噪声和不规则采样时间序列，为随机过程建模和预测提供了灵活的概率框架。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-pryddxphym/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1399, \"height\": 490, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pryddxphym/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1353, \"height\": 389, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pryddxphym/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1430, \"height\": 360, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pryddxphym/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1256, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pryddxphym/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 589, \"height\": 330, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pryddxphym/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1442, \"height\": 191, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pryddxphym/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1441, \"height\": 716, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pryddxphym/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1443, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pryddxphym/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1426, \"height\": 409, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 802, \"height\": 681, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1448, \"height\": 496, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 789, \"height\": 492, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 802, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1257, \"height\": 714, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1292, \"height\": 1109, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1466, \"height\": 794, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1479, \"height\": 928, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1061, \"height\": 240, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1442, \"height\": 191, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 831, \"height\": 304, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1137, \"height\": 304, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1023, \"height\": 225, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 588, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 767, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 717, \"height\": 341, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pryddxphym/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1070, \"height\": 263, \"label\": \"Table\"}]"
motivation: 传统SDE建模在时间点间采样需反复调用数值求解器，计算代价高。
method: 提出神经随机流，用条件归一化流直接学习SDE转移，保留随机流性质。
result: 在合成和真实数据上，NSF采样速度远快于传统方法，同时准确拟合SDE分布。
conclusion: NSF为随机时间序列建模提供高效的概率生成工具，支持不确定性量化。
---

## Abstract
Stochastic differential equations (SDEs) are well suited to modelling noisy and/or irregularly-sampled time series, which are omnipresent in finance, physics, and machine learning applications. Traditional approaches require costly simulation of numerical solvers when sampling between arbitrary time points. We introduce Neural Stochastic Flows (NSFs) and their latent dynamic versions, which learns (latent) SDE transition laws directly using conditional normalising flows, with architectural constraints that preserve properties inherited from stochastic flow. This enables sampling between arbitrary states in a single step, providing up to two orders of magnitude speedup for distant time points. Experiments on synthetic SDE simulations and real-world tracking and video data demonstrate that NSF maintains distributional accuracy comparable to numerical approaches while dramatically reducing computation for arbitrary time-point sampling, enabling applications where numerical solvers remain prohibitively expensive.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
基于条件归一化流的免求解器SDE建模，适用于随机时间序列。

### 2. 核心内容
针对传统SDE建模需昂贵数值求解器的问题，本文提出神经随机流（NSF），利用条件归一化流直接学习SDE转移规律，实现任意时间点间的单步采样，速度提升可达两个数量级。该方法能有效处理噪声和不规则采样时间序列，为随机过程建模和预测提供了灵活的概率框架。

### 3. 对应检索需求
Probabilistic and generative forecasting methods with uncertainty quantification techniques。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=PrYDDxphym](https://openreview.net/forum?id=PrYDDxphym)
