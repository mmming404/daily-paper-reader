---
title: Enhancing the Maximum Effective Window for Long-Term Time Series Forecasting
title_zh: 增强长期时间序列预测的最大有效窗口
authors: "Jiahui Zhang, Zhengyang Zhou, Wenjie Du, Yang Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=Gmwsy7TlFI"
tags: ["query:ts-forecast"]
score: 8.0
evidence: 最大有效窗口度量与模型无关模块以改进长期预测
tldr: 长序列预测中，更长的历史窗口理论上提供更多信息，但Transformer模型容易受到噪声和注意力分散影响。本文提出最大有效窗口（MEW）指标评估模型对长窗口的利用能力，并设计两个模型无关模块增强MEW。实验表明，模块可即插即用提升多种Transformer模型的长期预测精度，为充分利用历史数据提供了通用方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-gmwsy7tlfi/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 459, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gmwsy7tlfi/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1399, \"height\": 551, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gmwsy7tlfi/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1398, \"height\": 359, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gmwsy7tlfi/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1440, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gmwsy7tlfi/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1449, \"height\": 1081, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-gmwsy7tlfi/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1399, \"height\": 785, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gmwsy7tlfi/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1442, \"height\": 300, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gmwsy7tlfi/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1281, \"height\": 151, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gmwsy7tlfi/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1453, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gmwsy7tlfi/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1444, \"height\": 1036, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gmwsy7tlfi/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1464, \"height\": 234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gmwsy7tlfi/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 903, \"height\": 637, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gmwsy7tlfi/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1083, \"height\": 315, \"label\": \"Table\"}]"
motivation: 长窗口输入带来噪声和冗余，Transformer难以有效利用。
method: 提出MEW指标和两个即插即用模块，增强模型对长序列的处理能力。
result: 模块显著提升了多种Transformer模型的长期预测表现。
conclusion: 通过度量与增强MEW，实现了更有效的长期历史信息利用。
---

## Abstract
Long-term time series forecasting (LTSF) aims to predict future trends based on historical data. While longer lookback windows theoretically offer more comprehensive insights, Transformer-based models often struggle with them. On one hand, longer windows introduce more noise and redundancy, hindering the model's learning process. On the other hand, Transformers suffer from attention dispersion and are prone to overfitting to noise, especially when processing long sequences. In this paper, we introduce the Maximum Effective Window (MEW) metric to assess a model's ability to effectively utilize the lookback window. We also propose two model-agnostic modules to enhance MEW, enabling models to better leverage historical data for improved performance. Specifically, to reduce redundancy and noise, we introduce the Information Bottleneck Filter (IBF), which employs information bottleneck theory to extract the most essential subsequences from the input. Additionally, we propose the Hybrid-Transformer-Mamba (HTM), which incorporates the Mamba mechanism for selective forgetting of long sequences while harnessing the Transformer's strong modeling capabilities for shorter sequences. We integrate these two modules into various Transformer-based models, and experimental results show that they effectively enhance MEW, leading to improved overall performance. Our code is available at \url{https://github.com/forever-ly/PIH}.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
最大有效窗口度量与模型无关模块以改进长期预测。

### 2. 核心内容
长序列预测中，更长的历史窗口理论上提供更多信息，但Transformer模型容易受到噪声和注意力分散影响。本文提出最大有效窗口（MEW）指标评估模型对长窗口的利用能力，并设计两个模型无关模块增强MEW。实验表明，模块可即插即用提升多种Transformer模型的长期预测精度，为充分利用历史数据提供了通用方案。

### 3. 对应检索需求
innovative model architectures for time series forecasting。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=Gmwsy7TlFI](https://openreview.net/forum?id=Gmwsy7TlFI)
