---
title: Online Time Series Forecasting with Theoretical Guarantees
title_zh: 具有理论保证的在线时间序列预测
authors: "Zijian Li, Changze Zhou, Minghao Fu, Sanjay Manjunath, Fan Feng, Guangyi Chen, Yingyao Hu, Ruichu Cai, Kun Zhang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=0XCZWAo7wN"
tags: ["query:ts-forecast"]
score: 7.0
evidence: 提出通过识别隐变量实现在线时间序列预测的理论框架及保证
tldr: 针对在线时间序列预测中未知分布漂移问题，理论证明引入隐变量可降低贝叶斯风险，并提出通过最少相邻观测识别隐变量的实用算法，为自适应预测提供理论保证。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-0xczwao7wn/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 434, \"height\": 228, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0xczwao7wn/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 853, \"height\": 575, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0xczwao7wn/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 638, \"height\": 582, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0xczwao7wn/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1404, \"height\": 331, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1412, \"height\": 133, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1456, \"height\": 660, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1457, \"height\": 658, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1437, \"height\": 1398, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 856, \"height\": 295, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1118, \"height\": 258, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1262, \"height\": 1667, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1386, \"height\": 1592, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1386, \"height\": 1633, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1595, \"height\": 1671, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1269, \"height\": 1509, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1454, \"height\": 315, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1028, \"height\": 762, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1454, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1454, \"height\": 413, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1454, \"height\": 410, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-0xczwao7wn/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1454, \"height\": 412, \"label\": \"Table\"}]"
motivation: 在线场景下数据分布随时间变动，现有方法缺乏对隐变量影响的理论认识。
method: 提出理论框架TOT，证明隐变量降低贝叶斯风险，并设计用最小相邻观测识别隐变量的方式。
result: 理论保证结合实用算法，在基准上表现出适应分布漂移的优越性能。
conclusion: 隐变量建模为在线预测提供了理论基础和实用方案，有助于自动化处理非平稳环境。
---

## Abstract
This paper is concerned with online time series forecasting, where unknown distribution shifts occur over time, i.e., latent variables influence the mapping from historical to future observations. To develop an automated way of online time series forecasting, we propose a Theoretical framework for Online Time-series forecasting (TOT in short) with theoretical guarantees. Specifically, we prove that supplying a forecaster with latent variables tightens the Bayes risk—the benefit endures under estimation uncertainty of latent variables and grows as the latent variables achieve a more precise identifiability. To better introduce latent variables into online forecasting algorithms, we further propose to identify latent variables with minimal adjacent observations. Based on these results, we devise a model-agnostic blueprint by employing a temporal decoder to match the distribution of observed variables and two independent noise estimators to model the causal inference of latent variables and mixing procedures of observed variables, respectively. Experiment results on synthetic data support our theoretical claims. Moreover, plug-in implementations built on several baselines yield general improvement across multiple benchmarks, highlighting the effectiveness in real-world applications.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
提出通过识别隐变量实现在线时间序列预测的理论框架及保证。

### 2. 核心内容
针对在线时间序列预测中未知分布漂移问题，理论证明引入隐变量可降低贝叶斯风险，并提出通过最少相邻观测识别隐变量的实用算法，为自适应预测提供理论保证。

### 3. 对应检索需求
Frontier academic papers on time series forecasting with emphasis on methodological innovations。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=0XCZWAo7wN](https://openreview.net/forum?id=0XCZWAo7wN)
