---
title: "Time Series Generation Under Data Scarcity: A Unified Generative Modeling Approach"
title_zh: 数据稀缺条件下的时间序列生成：一种统一生成式建模方法
authors: "Tal Gonen, Itai Pemper, Ilan Naiman, Nimrod Berman, Omri Azencot"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=p324ryBKTc"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 提出基于扩散的生成框架，在数据稀缺条件下合成高保真时间序列。
tldr: 在时间序列数据稀缺条件下，对现有生成模型进行大规模评估，发现全数据与稀缺数据之间存在巨大性能差距。为此提出一个基于扩散的统一生成框架，通过在大规模异质时序数据集上预训练，仅用少量样本即可合成高保真时间序列。该工作为小样本时间序列生成和下游任务提供了坚实基线。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-p324rybktc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1476, \"height\": 506, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-p324rybktc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1444, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-p324rybktc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1435, \"height\": 489, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-p324rybktc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1164, \"height\": 1086, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 904, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1413, \"height\": 248, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 850, \"height\": 354, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1439, \"height\": 193, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1442, \"height\": 157, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1508, \"height\": 815, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1284, \"height\": 542, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 446, \"height\": 337, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 937, \"height\": 490, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 825, \"height\": 345, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 650, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 859, \"height\": 833, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 853, \"height\": 584, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1231, \"height\": 902, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1441, \"height\": 2022, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1399, \"height\": 2022, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1399, \"height\": 2021, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1384, \"height\": 2024, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1404, \"height\": 2020, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1393, \"height\": 2021, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-p324rybktc/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1036, \"height\": 1953, \"label\": \"Table\"}]"
motivation: 现有生成模型在数据稀缺时性能骤降，缺乏系统性研究。
method: 提出预训练扩散模型，结合大规模异质时序数据预训练与小样本微调。
result: 在多个领域上合成了高质量时间序列，显著缩小稀缺与丰富数据间的性能差距。
conclusion: 扩散生成框架为小样本时间序列生成提供了有效解决方案。
---

## Abstract
Generative modeling of time series is a central challenge in time series analysis, particularly under data-scarce conditions. Despite recent advances in generative modeling, a comprehensive understanding of how state-of-the-art generative models perform under limited supervision remains lacking. In this work, we conduct the first large-scale study evaluating leading generative models in data-scarce settings, revealing a substantial performance gap between full-data and data-scarce regimes. To close this gap, we propose a unified diffusion-based generative framework that can synthesize high-fidelity time series across diverse domains using just a few examples. Our model is pretrained on a large, heterogeneous collection of time series datasets, enabling it to learn generalizable temporal representations. It further incorporates architectural innovations such as dynamic convolutional layers for flexible channel adaptation and dataset token conditioning for domain-aware generation. Without requiring abundant supervision, our unified model achieves state-of-the-art performance in few-shot settings—outperforming domain-specific baselines across a wide range of subset sizes. Remarkably, it also surpasses all baselines even when tested on full datasets benchmarks, highlighting the strength of pretraining and cross-domain generalization. We hope this work encourages the community to revisit few-shot generative modeling as a key problem in time series research and pursue unified solutions that scale efficiently across domains.  Code is available at https://github.com/azencot-group/ImagenFew.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
提出基于扩散的生成框架，在数据稀缺条件下合成高保真时间序列。

### 2. 核心内容
在时间序列数据稀缺条件下，对现有生成模型进行大规模评估，发现全数据与稀缺数据之间存在巨大性能差距。为此提出一个基于扩散的统一生成框架，通过在大规模异质时序数据集上预训练，仅用少量样本即可合成高保真时间序列。该工作为小样本时间序列生成和下游任务提供了坚实基线。

### 3. 对应检索需求
generative models for time series forecasting。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=p324ryBKTc](https://openreview.net/forum?id=p324ryBKTc)
