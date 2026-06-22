---
title: Improving Time Series Forecasting via Instance-aware Post-hoc Revision
title_zh: 通过实例感知后置修正改进时间序列预测
authors: "Zhiding Liu, Mingyue Cheng, GuanHao Zhao, Jiqian Yang, Qi Liu, Enhong Chen"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=H7e5RpeIi4"
tags: ["query:ts-forecast"]
score: 7.0
evidence: 模型无关的框架，通过识别并修正有偏预测实例来提升深度预测模型性能。
tldr: 发现现有预测方法在实例层面因分布偏移、缺失值等问题表现不佳，提出一种模型无关的后置修正框架PIR，先识别有偏预测，再进行修正。实验表明该方法能显著提升各类深度预测模型的性能，为解决实例级偏差提供了通用工具。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-h7e5rpeii4/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1420, \"height\": 566, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h7e5rpeii4/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1376, \"height\": 736, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h7e5rpeii4/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1415, \"height\": 572, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h7e5rpeii4/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1436, \"height\": 632, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h7e5rpeii4/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1423, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h7e5rpeii4/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1437, \"height\": 1074, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h7e5rpeii4/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1422, \"height\": 820, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-h7e5rpeii4/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1474, \"height\": 975, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h7e5rpeii4/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1260, \"height\": 283, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h7e5rpeii4/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1297, \"height\": 598, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h7e5rpeii4/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1455, \"height\": 1688, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h7e5rpeii4/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1458, \"height\": 350, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h7e5rpeii4/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1452, \"height\": 446, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h7e5rpeii4/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1318, \"height\": 478, \"label\": \"Table\"}]"
motivation: 实例级变异导致预测偏差，即使整体性能良好也需局部修正。
method: 提出PIR框架，在后预测阶段识别并修订有偏实例。
result: 在多个基准上，PIR普遍提升了多种预测模型的准确率。
conclusion: 实例感知后置修正为提升时间序列预测可靠性提供了新途径。
---

## Abstract
Time series forecasting plays a pivotal role in various real-world applications and has attracted significant attention in recent decades. While recent methods have achieved remarkable accuracy by incorporating advanced inductive biases and training strategies, we observe that instance-level variations remain a significant challenge. These variations—stemming from distribution shifts, missing data, and long-tail patterns—often lead to suboptimal forecasts for specific instances, even when overall performance appears strong. To address this issue, we propose a model-agnostic framework, PIR, designed to enhance forecasting performance through Post-forecasting Identification and Revision. Specifically, PIR first identifies biased forecast instances by estimating their predictive accuracy. Based on this, the framework revises the forecasts using contextual information, including covariates and historical time series, from both local and global perspectives in a post-processing fashion. Extensive experiments on real-world datasets with mainstream forecasting models demonstrate that PIR effectively mitigates instance-level errors and significantly improves forecasting reliability.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
模型无关的框架，通过识别并修正有偏预测实例来提升深度预测模型性能。

### 2. 核心内容
发现现有预测方法在实例层面因分布偏移、缺失值等问题表现不佳，提出一种模型无关的后置修正框架PIR，先识别有偏预测，再进行修正。实验表明该方法能显著提升各类深度预测模型的性能，为解决实例级偏差提供了通用工具。

### 3. 对应检索需求
deep learning based neural forecasting techniques。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=H7e5RpeIi4](https://openreview.net/forum?id=H7e5RpeIi4)
