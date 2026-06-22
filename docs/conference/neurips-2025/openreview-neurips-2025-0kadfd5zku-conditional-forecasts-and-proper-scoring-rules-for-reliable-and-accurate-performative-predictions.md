---
title: Conditional Forecasts and Proper Scoring Rules for Reliable and Accurate Performative Predictions
title_zh: 条件预测与适当评分规则：实现可靠准确的表演性预测
authors: "Philip Boeken, Onno Zoeter, Joris M. Mooij"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=0KAdFd5zku"
tags: ["query:ts-forecast"]
score: 7.0
evidence: 在表演性预测场景下概率预测评分规则的理论进展。
tldr: 研究预测影响结果本身的表演性预测问题，证明条件独立可保证分布不变，但经典评分规则仍会失效。提出两种解决方案：决策论中的分离性预测激励相容，以及基于无偏分化估计的评分。为推动真实场景下可靠概率预测提供了理论根基。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-0kadfd5zku/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 308, \"height\": 106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0kadfd5zku/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1199, \"height\": 307, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0kadfd5zku/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1094, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0kadfd5zku/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 414, \"height\": 109, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0kadfd5zku/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1145, \"height\": 344, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0kadfd5zku/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 737, \"height\": 579, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0kadfd5zku/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1325, \"height\": 658, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0kadfd5zku/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1331, \"height\": 661, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0kadfd5zku/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1332, \"height\": 1265, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-0kadfd5zku/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1434, \"height\": 535, \"label\": \"Figure\"}]"
motivation: 表演性预测中标准概率评分规则失效，难以获得可靠预测。
method: 理论分析条件独立下的预测不变性，提出激励相容评分与无偏估计评分。
result: 给出了一般不可能性定理，并鉴定了两种可靠评分方案。
conclusion: 为表演性环境下的概率预测奠定了理论基础。
---

## Abstract
Performative predictions are forecasts which influence the outcomes they aim to predict, undermining the existence of correct forecasts and standard methods of elicitation and estimation. We show that conditioning forecasts on covariates that separate them from the outcome renders the target distribution forecast-invariant, guaranteeing well-posedness of the forecasting problem. However, even under this condition, classical proper scoring rules fail to elicit correct forecasts. We prove a general impossibility result and identify two solutions: (i) in decision-theoretic settings, elicitation of correct and incentive-compatible forecasts is possible if forecasts are separating; (ii) scoring with unbiased estimates of the divergence between the forecast and the induced distribution of the target variable yields correct forecasts. Applying these insights to parameter estimation, conditional forecasts and proper scoring rules enable performatively stable estimation of performatively correct parameters, resolving the issues raised by Perdomo et al. (2020). Our results expose fundamental limits of classical forecast evaluation and offer new tools for reliable and accurate forecasting in performative settings.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
在表演性预测场景下概率预测评分规则的理论进展。

### 2. 核心内容
研究预测影响结果本身的表演性预测问题，证明条件独立可保证分布不变，但经典评分规则仍会失效。提出两种解决方案：决策论中的分离性预测激励相容，以及基于无偏分化估计的评分。为推动真实场景下可靠概率预测提供了理论根基。

### 3. 对应检索需求
advances in probabilistic time series forecasting models。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=0KAdFd5zku](https://openreview.net/forum?id=0KAdFd5zku)
