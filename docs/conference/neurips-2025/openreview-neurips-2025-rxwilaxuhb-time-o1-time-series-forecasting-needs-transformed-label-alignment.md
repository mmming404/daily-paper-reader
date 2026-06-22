---
title: "Time-o1: Time-Series Forecasting Needs Transformed Label Alignment"
title_zh: Time-o1：时间序列预测需要变换标签对齐
authors: "Hao Wang, Licheng Pan, Zhichao Chen, Xu Chen, Qingyang Dai, Lei Wang, Haoxuan Li, Zhouchen Lin"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=RxWILaXuhb"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 通过变换增强损失函数解相关标签序列成分，改进训练
tldr: 针对时间序列预测中均方误差损失忽视标签自相关性、任务过多导致优化困难的问题，本文提出Time-o1，一种变换增强损失函数。通过将标签序列转换为独立成分并区分重要性，训练时对齐最重要的成分，有效缓解自相关偏差，简化优化。实验表明该损失函数可提升多种模型的长期预测精度。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-rxwilaxuhb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1456, \"height\": 282, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rxwilaxuhb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1433, \"height\": 320, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rxwilaxuhb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1423, \"height\": 319, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rxwilaxuhb/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1466, \"height\": 669, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rxwilaxuhb/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1444, \"height\": 316, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rxwilaxuhb/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1429, \"height\": 1309, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rxwilaxuhb/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1457, \"height\": 607, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rxwilaxuhb/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1429, \"height\": 1310, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rxwilaxuhb/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1466, \"height\": 1503, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rxwilaxuhb/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1468, \"height\": 1506, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1461, \"height\": 567, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1455, \"height\": 438, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1422, \"height\": 584, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1400, \"height\": 225, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 707, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 708, \"height\": 327, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1480, \"height\": 1803, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1463, \"height\": 347, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1444, \"height\": 488, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1462, \"height\": 1387, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1363, \"height\": 828, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rxwilaxuhb/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1439, \"height\": 345, \"label\": \"Table\"}]"
motivation: 标准损失函数忽视标签自相关性，导致长期预测优化困难。
method: 提出变换增强损失Time-o1，将标签序列解相关并加权对齐关键成分。
result: 在多个模型上应用Time-o1，长期预测性能提升明显。
conclusion: 通过损失函数创新可有效应对时序预测的特定挑战，提高训练效果。
---

## Abstract
Training time-series forecasting models poses unique challenges in loss function design. Most existing approaches adopt temporal mean squared error, but this study reveals two critical limitations: (1) it ignores the presence of label autocorrelation, which biases it from the true label sequence likelihood;  (2) it involves excessive number of tasks, which complicates optimization, especially for long-term forecasting. To address these issues, we introduce Time-o1, a transform-enhanced loss function for time-series forecasting. The central idea is to transform the label sequence into decorrelated components with discriminated significance. Models are then trained to align the most significant components, thereby effectively mitigating label autocorrelation and reducing task amount. Experiments demonstrate that Time-o1 achieves state-of-the-art performance and is compatible with various forecast models. Code is available at https://github.com/Master-PLC/Time-o1.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
通过变换增强损失函数解相关标签序列成分，改进训练。

### 2. 核心内容
针对时间序列预测中均方误差损失忽视标签自相关性、任务过多导致优化困难的问题，本文提出Time-o1，一种变换增强损失函数。通过将标签序列转换为独立成分并区分重要性，训练时对齐最重要的成分，有效缓解自相关偏差，简化优化。实验表明该损失函数可提升多种模型的长期预测精度。

### 3. 对应检索需求
Frontier academic papers on time series forecasting with emphasis on methodological innovations。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=RxWILaXuhb](https://openreview.net/forum?id=RxWILaXuhb)
