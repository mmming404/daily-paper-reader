---
title: "Abstain Mask Retain Core: Time Series Prediction by Adaptive Masking Loss with Representation Consistency"
title_zh: 弃掩留核：通过自适应掩码损失与表示一致性进行时间序列预测
authors: "Renzhao Liang, Sizhe Xu, Chenggang Xie, Jingru Chen, Feiyang Ren, Shu Yang, Takahiro Yabe"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=KrglRiOKYT"
tags: ["query:ts-forecast"]
score: 8.0
evidence: 基于信息瓶颈理论提出自适应掩码损失以保留时间序列预测中的核心信号
tldr: 该论文发现适当截断历史数据可提高预测精度，据此提出基于信息瓶颈的自适应掩码损失，强制模型聚焦核心信号，去除冗余特征，从而提升时间序列预测性能。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-krglriokyt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1417, \"height\": 404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-krglriokyt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1131, \"height\": 277, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-krglriokyt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1451, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-krglriokyt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1443, \"height\": 807, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-krglriokyt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1454, \"height\": 1231, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 439, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1444, \"height\": 422, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1012, \"height\": 579, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1018, \"height\": 293, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1440, \"height\": 1415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1457, \"height\": 1097, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1454, \"height\": 399, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 588, \"height\": 953, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1443, \"height\": 284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1444, \"height\": 300, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-krglriokyt/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1448, \"height\": 226, \"label\": \"Table\"}]"
motivation: 发现长序列信息增益假设存在局限，模型易学习噪声等冗余特征，损害信号提取。
method: 提出自适应掩码损失，结合表示一致性，基于信息瓶颈理论有选择地保留关键序列信息。
result: 在多个预测任务上显著优于标准训练方法，有效抑制冗余特征学习。
conclusion: 通过自适应掩码实现信息瓶颈，为时间序列预测提供了一种简单而有效的特征选择策略。
---

## Abstract
Time series forecasting plays a pivotal role in critical domains such as energy management and financial markets. Although deep learning-based approaches (e.g., MLP, RNN, Transformer) have achieved remarkable progress, the prevailing "long-sequence information gain hypothesis" exhibits inherent limitations. Through systematic experimentation, this study reveals a counterintuitive phenomenon: appropriately truncating historical data can paradoxically enhance prediction accuracy, indicating that existing models learn substantial redundant features (e.g., noise or irrelevant fluctuations) during training, thereby compromising effective signal extraction. Building upon information bottleneck theory, we propose an innovative solution termed Adaptive Masking Loss with Representation Consistency (AMRC), which features two core components: 1) Dynamic masking loss, which adaptively identified highly discriminative temporal segments to guide gradient descent during model training; 2) Representation consistency constraint, which stabilized the mapping relationships among inputs, labels, and predictions. Experimental results demonstrate that AMRC effectively suppresses redundant feature learning while significantly improving model performance. This work not only challenges conventional assumptions in temporal modeling but also provides novel theoretical insights and methodological breakthroughs for developing efficient and robust forecasting models. We have made our code available at \url{https://github.com/MazelTovy/AMRC}.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
基于信息瓶颈理论提出自适应掩码损失以保留时间序列预测中的核心信号。

### 2. 核心内容
该论文发现适当截断历史数据可提高预测精度，据此提出基于信息瓶颈的自适应掩码损失，强制模型聚焦核心信号，去除冗余特征，从而提升时间序列预测性能。

### 3. 对应检索需求
innovative model architectures for time series forecasting。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=KrglRiOKYT](https://openreview.net/forum?id=KrglRiOKYT)
