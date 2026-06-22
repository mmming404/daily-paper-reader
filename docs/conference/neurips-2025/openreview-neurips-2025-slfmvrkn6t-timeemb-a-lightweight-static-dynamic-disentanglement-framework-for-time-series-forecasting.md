---
title: "TimeEmb: A Lightweight Static-Dynamic Disentanglement Framework for Time Series Forecasting"
title_zh: TimeEmb：一种面向时间序列预测的轻量级静态-动态解耦框架
authors: "Mingyuan Xia, Chunxu Zhang, Zijian Zhang, Hao Miao, Qidong Liu, Yuanshao Zhu, Bo Yang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=sLfMvrkn6T"
tags: ["query:ts-forecast"]
score: 8.0
evidence: 轻量级框架，解耦静态与动态成分，应对非平稳时间序列预测。
tldr: 针对时间序列非平稳性问题，提出TimeEmb轻量级框架，创新性地将时序分解为时不变和时变成分，分别捕捉长期模式与短期波动。实验表明该解耦表示能有效提升分布偏移下的预测稳定性和准确性，为解耦学习在时序预测中提供了简洁方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-slfmvrkn6t/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 714, \"height\": 578, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-slfmvrkn6t/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 797, \"height\": 410, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-slfmvrkn6t/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1400, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-slfmvrkn6t/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1446, \"height\": 311, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-slfmvrkn6t/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 570, \"height\": 929, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-slfmvrkn6t/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1324, \"height\": 480, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-slfmvrkn6t/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1346, \"height\": 491, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-slfmvrkn6t/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1398, \"height\": 406, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1450, \"height\": 853, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1446, \"height\": 291, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1450, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1463, \"height\": 274, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1253, \"height\": 1334, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1254, \"height\": 1335, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 896, \"height\": 369, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 833, \"height\": 676, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1206, \"height\": 761, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1205, \"height\": 764, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1031, \"height\": 1245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1115, \"height\": 825, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-slfmvrkn6t/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1203, \"height\": 755, \"label\": \"Table\"}]"
motivation: 现有方法混淆时变与时不变成分，导致分布偏移下预测性能下降。
method: 提出静态-动态解耦框架TimeEmb，显式分离并分别建模。
result: 解耦方法在多个非平稳基准上取得优越且稳定的预测效果。
conclusion: 静态-动态解耦是提高时序预测鲁棒性的有效策略。
---

## Abstract
Temporal non-stationarity, the phenomenon that time series distributions change over time, poses fundamental challenges to reliable time series forecasting. Intuitively, the complex time series can be decomposed into two factors, i.e., time-invariant and time-varying components, which indicate static and dynamic patterns, respectively. Nonetheless, existing methods often conflate the time-varying and time-invariant components, and jointly learn the combined long-term patterns and short-term fluctuations, leading to suboptimal performance facing distribution shifts. To address this issue, we initiatively propose a lightweight static-dynamic decomposition framework, TimeEmb, for time series forecasting. TimeEmb innovatively separates time series into two complementary components: (1) time-invariant component, captured by a novel global embedding module that learns persistent representations across time series, and (2) time-varying component, processed by an efficient frequency-domain filtering mechanism inspired by full-spectrum analysis in signal processing. Experiments on real-world datasets demonstrate that TimeEmb outperforms state-of-the-art baselines and requires fewer computational resources. We conduct comprehensive quantitative and qualitative analyses to verify the efficacy of static-dynamic disentanglement. This lightweight framework can also improve existing time-series forecasting methods with simple integration. To ease reproducibility, our code is available at https://github.com/showmeon/TimeEmb.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
轻量级框架，解耦静态与动态成分，应对非平稳时间序列预测。

### 2. 核心内容
针对时间序列非平稳性问题，提出TimeEmb轻量级框架，创新性地将时序分解为时不变和时变成分，分别捕捉长期模式与短期波动。实验表明该解耦表示能有效提升分布偏移下的预测稳定性和准确性，为解耦学习在时序预测中提供了简洁方案。

### 3. 对应检索需求
deep learning based neural forecasting techniques。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=sLfMvrkn6T](https://openreview.net/forum?id=sLfMvrkn6T)
