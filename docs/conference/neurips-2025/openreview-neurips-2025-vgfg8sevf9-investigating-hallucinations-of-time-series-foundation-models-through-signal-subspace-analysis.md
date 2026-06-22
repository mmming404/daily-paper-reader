---
title: Investigating Hallucinations of Time Series Foundation Models through Signal Subspace Analysis
title_zh: 通过信号子空间分析研究时间序列基础模型的幻觉
authors: "Yufeng Zou, Zijian Wang, Diego Klabjan, Han Liu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=vgfG8sEVf9"
tags: ["query:ts-forecast"]
score: 7.0
evidence: 通过信号子空间分析定义和分析时间序列基础模型的幻觉现象
tldr: 时间序列基础模型在零样本预测中可能产生幻觉，即预测序列与上下文动态不一致，但现有研究对此关注不足。本文首次形式化定义了此类幻觉，发现其源于前向传播中隐藏状态的上下文信息丢失。为此提出一种信号子空间识别方法，通过放大关键子空间来增强模型保持上下文的能力。实验表明，该方法能有效检测并缓解幻觉，为构建更可靠的时间序列基础模型提供了理论依据和技术手段。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-vgfg8sevf9/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1429, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vgfg8sevf9/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1446, \"height\": 427, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vgfg8sevf9/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 796, \"height\": 361, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vgfg8sevf9/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 800, \"height\": 360, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vgfg8sevf9/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1159, \"height\": 439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vgfg8sevf9/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1148, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vgfg8sevf9/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1015, \"height\": 2410, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vgfg8sevf9/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1013, \"height\": 2397, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-vgfg8sevf9/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1017, \"height\": 2437, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-vgfg8sevf9/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1442, \"height\": 636, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vgfg8sevf9/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1439, \"height\": 536, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vgfg8sevf9/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1438, \"height\": 786, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vgfg8sevf9/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1335, \"height\": 820, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vgfg8sevf9/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1436, \"height\": 324, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vgfg8sevf9/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1442, \"height\": 442, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vgfg8sevf9/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1435, \"height\": 1029, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vgfg8sevf9/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1440, \"height\": 550, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-vgfg8sevf9/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1437, \"height\": 350, \"label\": \"Table\"}]"
motivation: 现有时间序列基础模型在零样本预测时可能出现幻觉现象，但缺乏系统研究。
method: 提出信号子空间识别方法，通过分析隐藏状态捕捉上下文信息丢失，并放大关键子空间以增强模型。
result: 实验验证了所提方法能有效识别和缓解幻觉，提升预测可靠性。
conclusion: 该研究为时间序列基础模型的幻觉问题提供了理论基础和实用解决方案。
---

## Abstract
Times series foundation models (TSFMs) have emerged as a promising paradigm for time series analyses and forecasting, showing remarkable generalization performance across different domains. Despite the efforts made on hallucinations of foundation models, hallucinations of TSFMs have been underexplored in existing literature. In this paper, we formally define TSFM hallucinations in the zero-shot forecasting setting by examining whether a generated forecast exhibits different dynamics from those of the context. Our study reveals that TSFM hallucinations are associated with the loss of context information in hidden states during forward propagation. As such, we propose a methodology to identify signal subspaces of TSFMs and magnify the information through intervention. Experiments demonstrate that our proposed intervention approach effectively mitigates hallucinations and improves forecasting performance. The signal strength measure computed from signal subspaces shows strong predictive power of hallucinations and forecasting performance of the model. Our work contributes to deeper understanding of TSFM trustworthiness that could foster future research in this direction.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
通过信号子空间分析定义和分析时间序列基础模型的幻觉现象。

### 2. 核心内容
时间序列基础模型在零样本预测中可能产生幻觉，即预测序列与上下文动态不一致，但现有研究对此关注不足。本文首次形式化定义了此类幻觉，发现其源于前向传播中隐藏状态的上下文信息丢失。为此提出一种信号子空间识别方法，通过放大关键子空间来增强模型保持上下文的能力。实验表明，该方法能有效检测并缓解幻觉，为构建更可靠的时间序列基础模型提供了理论依据和技术手段。

### 3. 对应检索需求
Frontier academic papers on time series forecasting with emphasis on methodological innovations。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=vgfG8sEVf9](https://openreview.net/forum?id=vgfG8sEVf9)
