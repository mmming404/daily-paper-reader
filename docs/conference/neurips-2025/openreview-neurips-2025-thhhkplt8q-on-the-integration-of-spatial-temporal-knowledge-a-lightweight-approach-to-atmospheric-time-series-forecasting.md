---
title: "On the Integration of Spatial-Temporal Knowledge: A Lightweight Approach to Atmospheric Time Series Forecasting"
title_zh: 论时空知识整合：大气时间序列预测的轻量化方法
authors: "Yisong Fu, Fei Wang, Zezhi Shao, Boyu Diao, Lin Wu, Zhulin An, Chengqing Yu, Yujie Li, Yongjun Xu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=thHhKPlt8q"
tags: ["query:ts-forecast"]
score: 7.0
evidence: 提出使用时空位置嵌入替代注意力的轻量化大气时间序列预测方法
tldr: 从大气动力学视角重新审视大气时间序列预测，发现时空位置嵌入本身即可建模时空相关，无需注意力机制，据此提出轻量级模型，大幅减少参数量并保持预测精度。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 702, \"height\": 508, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1277, \"height\": 494, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1278, \"height\": 698, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1331, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1250, \"height\": 831, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 777, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1024, \"height\": 405, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1364, \"height\": 401, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1413, \"height\": 725, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1426, \"height\": 721, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-thhhkplt8q/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1412, \"height\": 724, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-thhhkplt8q/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 1088, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-thhhkplt8q/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1439, \"height\": 290, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-thhhkplt8q/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 727, \"height\": 427, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-thhhkplt8q/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1437, \"height\": 422, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-thhhkplt8q/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1393, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-thhhkplt8q/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1440, \"height\": 466, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-thhhkplt8q/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 747, \"height\": 298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-thhhkplt8q/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1357, \"height\": 283, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-thhhkplt8q/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1448, \"height\": 288, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-thhhkplt8q/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1439, \"height\": 243, \"label\": \"Table\"}]"
motivation: 现有Transformer结构复杂，参数多训练长，限制大气预报可扩展性。
method: 提出基于时空位置嵌入的轻量模型，利用地理坐标和时间特征直接建模相关。
result: 模型参数和训练时间大幅减少，预测精度与大型模型可比。
conclusion: 时空位置嵌入可作为大气预报的有效归纳偏置，为轻量化模型设计提供新思路。
---

## Abstract
Transformers have gained attention in atmospheric time series forecasting (ATSF) for their ability to capture global spatial-temporal correlations. However, their complex architectures lead to excessive parameter counts and extended training times, limiting their scalability to large-scale forecasting. In this paper, we revisit ATSF from a theoretical perspective of atmospheric dynamics and uncover a key insight: spatial-temporal position embedding (STPE) can inherently model spatial-temporal correlations even without attention mechanisms. Its effectiveness arises from integrating geographical coordinates and temporal features, which are intrinsically linked to atmospheric dynamics. Based on this, we propose **STELLA**, a **S**patial-**T**emporal knowledge **E**mbedded **L**ightweight mode**L** for ASTF, utilizing only STPE and an MLP architecture in place of Transformer layers. With 10k parameters and one hour of training, STELLA achieves superior performance on five datasets compared to other advanced methods. The paper emphasizes the effectiveness of spatial-temporal knowledge integration over complex architectures, providing novel insights for ATSF.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
提出使用时空位置嵌入替代注意力的轻量化大气时间序列预测方法。

### 2. 核心内容
从大气动力学视角重新审视大气时间序列预测，发现时空位置嵌入本身即可建模时空相关，无需注意力机制，据此提出轻量级模型，大幅减少参数量并保持预测精度。

### 3. 对应检索需求
innovative model architectures for time series forecasting。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=thHhKPlt8q](https://openreview.net/forum?id=thHhKPlt8q)
