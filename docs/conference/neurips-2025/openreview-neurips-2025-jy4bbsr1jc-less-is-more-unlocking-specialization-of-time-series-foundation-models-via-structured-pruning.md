---
title: "Less is More: Unlocking Specialization of Time Series Foundation Models via Structured Pruning"
title_zh: 少即是多：通过结构化剪枝解锁时间序列基础模型的专家化
authors: "Lifan Zhao, Yanyan Shen, Zhaoyang Liu, Xue Wang, Jiaji Deng"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=jy4bBsr1Jc"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 通过结构化剪枝实现时序基础模型任务特化，保留先验知识
tldr: 针对时序基础模型（TSFM）微调后性能仍逊于专用模型的问题，本文通过实证分析揭示TSFM存在稀疏性和冗余，提出结构化剪枝方法，在保留任务相关子结构的同时去除冗余，实现轻量特化。实验表明剪枝后的TSFM在多个下游预测任务上优于全参数微调和专用模型，推进了TSFM的高效适配。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-jy4bbsr1jc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1451, \"height\": 332, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jy4bbsr1jc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1446, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jy4bbsr1jc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1452, \"height\": 478, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jy4bbsr1jc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1452, \"height\": 475, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jy4bbsr1jc/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1437, \"height\": 530, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jy4bbsr1jc/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1428, \"height\": 499, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jy4bbsr1jc/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1416, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jy4bbsr1jc/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1437, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jy4bbsr1jc/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1449, \"height\": 511, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jy4bbsr1jc/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1456, \"height\": 725, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-jy4bbsr1jc/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1439, \"height\": 349, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jy4bbsr1jc/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1515, \"height\": 951, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jy4bbsr1jc/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 696, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jy4bbsr1jc/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 696, \"height\": 431, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jy4bbsr1jc/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1365, \"height\": 626, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jy4bbsr1jc/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1470, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jy4bbsr1jc/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1085, \"height\": 836, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jy4bbsr1jc/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1450, \"height\": 745, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jy4bbsr1jc/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1446, \"height\": 706, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jy4bbsr1jc/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 926, \"height\": 2375, \"label\": \"Table\"}]"
motivation: 大规模时序基础模型微调后仍不如专用模型，存在参数冗余问题。
method: 分析TSFM的计算稀疏性，提出结构化剪枝保留任务相关子网络。
result: 剪枝后的TSFM在多个预测任务上超越微调基线和专用模型。
conclusion: 结构化剪枝是一种高效的TSFM适配方法，兼具性能和效率。
---

## Abstract
Scaling laws motivate the development of Time Series Foundation Models (TSFMs) that pre-train vast parameters and achieve remarkable zero-shot forecasting performance. Surprisingly, even after fine-tuning, TSFMs cannot consistently outperform smaller, specialized models trained on full-shot downstream data. 
A key question is how to realize effective adaptation of TSFMs for a target forecasting task. Through empirical studies on various TSFMs, the pre-trained models often exhibit inherent sparsity and redundancy in computation, suggesting that TSFMs have learned to activate task-relevant network substructures to accommodate diverse forecasting tasks. To preserve this valuable prior knowledge, we propose a structured pruning method to regularize the subsequent fine-tuning process by focusing it on a more relevant and compact parameter space.  
Extensive experiments on seven TSFMs and six benchmarks demonstrate that fine-tuning a smaller, pruned TSFM significantly improves forecasting performance compared to fine-tuning original models. This ``prune-then-finetune'' paradigm often enables TSFMs to achieve state-of-the-art performance and surpass strong specialized baselines. 
Source code is made publicly available at \url{https://github.com/SJTU-DMTai/Prune-then-Finetune}.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
通过结构化剪枝实现时序基础模型任务特化，保留先验知识。

### 2. 核心内容
针对时序基础模型（TSFM）微调后性能仍逊于专用模型的问题，本文通过实证分析揭示TSFM存在稀疏性和冗余，提出结构化剪枝方法，在保留任务相关子结构的同时去除冗余，实现轻量特化。实验表明剪枝后的TSFM在多个下游预测任务上优于全参数微调和专用模型，推进了TSFM的高效适配。

### 3. 对应检索需求
Frontier academic papers on time series forecasting with emphasis on methodological innovations。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=jy4bBsr1Jc](https://openreview.net/forum?id=jy4bBsr1Jc)
