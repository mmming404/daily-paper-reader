---
title: "TimePerceiver: An Encoder-Decoder Framework for Generalized Time-Series Forecasting"
title_zh: TimePerceiver：面向广义时间序列预测的编解码框架
authors: "Jaebin Lee, Hankook Lee"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=RCeZ063p33"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 统一编解码框架，实现外推、内插等广义时序预测
tldr: 现有预测研究偏重编码器设计而忽视解码和训练，TimePerceiver提出统一编解码框架，将预测任务泛化为包含外推、内插、填补等目标，输入输出段可任意放置。结合有效训练策略，该框架在多种时序基准上取得领先性能，为广义预测提供了整体方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-rcez063p33/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 449, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rcez063p33/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1448, \"height\": 548, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rcez063p33/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1057, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rcez063p33/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1411, \"height\": 419, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-rcez063p33/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1435, \"height\": 513, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 1326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1443, \"height\": 416, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 580, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 503, \"height\": 341, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1075, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1448, \"height\": 479, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1441, \"height\": 197, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1446, \"height\": 1288, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1445, \"height\": 1282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1445, \"height\": 1282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1438, \"height\": 1090, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 550, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 785, \"height\": 318, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 484, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1004, \"height\": 347, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1153, \"height\": 445, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-rcez063p33/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1010, \"height\": 460, \"label\": \"Table\"}]"
motivation: 以往工作将编码、解码和训练割裂，未充分利用统一框架的潜力。
method: 设计TimePerceiver，实现编码器-解码器联合，支持多种预测目标。
result: 在多个预测任务上性能达到最优，验证了统一框架的优势。
conclusion: 整体性编解码设计为时序预测提供了更通用、更强大的解决方案。
---

## Abstract
In machine learning, effective modeling requires a holistic consideration of how to encode inputs, make predictions (i.e., decoding), and train the model. However, in time-series forecasting, prior work has predominantly focused on encoder design, often treating prediction and training as separate or secondary concerns. In this paper, we propose TimePerceiver, a unified encoder-decoder forecasting framework that is tightly aligned with an effective training strategy. To be specific, we first generalize the forecasting task to include diverse temporal prediction objectives such as extrapolation, interpolation, and imputation. Since this generalization requires handling input and target segments that are arbitrarily positioned along the temporal axis, we design a novel encoder-decoder architecture that can flexibly perceive and adapt to these varying positions. For encoding, we introduce a set of latent bottleneck representations that can interact with all input segments to jointly capture temporal and cross-channel dependencies. For decoding, we leverage learnable queries corresponding to target timestamps to effectively retrieve relevant information. Extensive experiments demonstrate that our framework consistently and significantly outperforms prior state-of-the-art baselines across a wide range of benchmark datasets.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
统一编解码框架，实现外推、内插等广义时序预测。

### 2. 核心内容
现有预测研究偏重编码器设计而忽视解码和训练，TimePerceiver提出统一编解码框架，将预测任务泛化为包含外推、内插、填补等目标，输入输出段可任意放置。结合有效训练策略，该框架在多种时序基准上取得领先性能，为广义预测提供了整体方案。

### 3. 对应检索需求
Frontier academic papers on time series forecasting with emphasis on methodological innovations。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=RCeZ063p33](https://openreview.net/forum?id=RCeZ063p33)
