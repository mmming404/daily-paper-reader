---
title: "Conformal Prediction Beyond the Seen: A Missing Mass Perspective for Uncertainty Quantification in Generative Models"
title_zh: 超越可见的共形预测：从缺失质量视角看生成模型的不确定性量化
authors: "Sima Noorani, Shayan Kiyani, George J. Pappas, Hamed Hassani"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=KoVKLxn3Nb"
tags: ["query:ts-forecast"]
score: 7.0
evidence: 从缺失质量角度为黑盒生成模型提供共形预测不确定性量化
tldr: 针对生成式AI模型的安全部署需求，本文提出一种仅需有限查询的共形预测不确定性量化框架。通过缺失质量视角，在覆盖保证、查询预算及预测集信息量之间实现新权衡。该方法适用于黑盒生成模型，为在时序生成式预测等应用中提供可解释的不确定性量化提供了通用工具箱。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-kovklxn3nb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1442, \"height\": 1064, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kovklxn3nb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1165, \"height\": 1704, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kovklxn3nb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1436, \"height\": 941, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-kovklxn3nb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1449, \"height\": 345, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kovklxn3nb/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 951, \"height\": 454, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kovklxn3nb/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 900, \"height\": 1670, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kovklxn3nb/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1257, \"height\": 639, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kovklxn3nb/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 834, \"height\": 339, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kovklxn3nb/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 938, \"height\": 420, \"label\": \"Table\"}]"
motivation: 生成模型的不确定性量化对于安全部署至关重要，但传统共形预测依赖结构化输出。
method: 提出基于缺失质量视角的查询式共形预测，仅通过有限查询构建预测集。
result: 方法在覆盖、预算和信息量之间取得有效平衡，适用于黑盒生成模型。
conclusion: 为生成模型提供了无需结构化输出的通用不确定性量化新范式。
---

## Abstract
Uncertainty quantification (UQ) is essential for safe deployment of generative AI models such as large language models (LLMs), especially in high-stakes applications. Conformal prediction (CP) offers a principled uncertainty quantification framework, but classical methods focus on regression and classification, relying on geometric distances or softmax scores--tools that presuppose structured outputs. We depart from this paradigm by studying CP in a query-only setting, where prediction sets must be constructed solely from finite queries to a black-box generative model, introducing a new trade-off between coverage, test-time query budget, and informativeness. We introduce **Conformal Prediction with Query Oracle** (CPQ), a framework characterizing the optimal interplay between these objectives. Our finite-sample algorithm is built on two core principles: one governs the optimal query policy, and the other defines the optimal mapping from queried samples to prediction sets. Remarkably, both are rooted in the classical **missing mass problem** in statistics. Specifically, the optimal query policy depends on the rate of decay--or the derivative--of the missing mass, for which we develop a novel estimator. Meanwhile, the optimal mapping hinges on the missing mass itself, which we estimate using Good-Turing estimators. We then turn our focus to implementing our method for language models, particularly in open-ended LLM tasks involving question answering, multi-step reasoning, and structured information extraction, where outputs are vast, variable, and often under-specified. Fine-grained experiments on three real-world open-ended tasks and two LLMs, show CPQ's applicability to **any black-box LLM** and highlight: (1) individual contribution of each principle to CPQ’s performance, and (2) CPQ's ability to yield significantly more informative prediction sets than existing conformal methods for language uncertainty quantification.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
从缺失质量角度为黑盒生成模型提供共形预测不确定性量化。

### 2. 核心内容
针对生成式AI模型的安全部署需求，本文提出一种仅需有限查询的共形预测不确定性量化框架。通过缺失质量视角，在覆盖保证、查询预算及预测集信息量之间实现新权衡。该方法适用于黑盒生成模型，为在时序生成式预测等应用中提供可解释的不确定性量化提供了通用工具箱。

### 3. 对应检索需求
Probabilistic and generative forecasting methods with uncertainty quantification techniques。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=KoVKLxn3Nb](https://openreview.net/forum?id=KoVKLxn3Nb)
