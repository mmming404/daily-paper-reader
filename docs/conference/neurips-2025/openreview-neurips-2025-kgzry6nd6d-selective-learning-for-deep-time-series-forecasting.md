---
title: Selective Learning for Deep Time Series Forecasting
title_zh: 深度时间序列预测的选择性学习策略
authors: "Yisong Fu, Zezhi Shao, Chengqing Yu, Yujie Li, Zhulin An, Cheems Wang, Yongjun Xu, Fei Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=kgzRy6nD6D"
tags: ["query:ts-forecast"]
score: 8.0
evidence: 提出一种新颖的深度学习时间序列预测选择性学习策略来对抗过拟合。
tldr: 针对深度时间序列模型因噪声和异常值易过拟合的问题，提出一种选择性学习策略，在优化时筛选泛化性好的时间步计算损失，引导模型忽略不可泛化的时间步。实验表明该方法能有效提升点预测的准确性和鲁棒性，为深度时序预测训练提供了新视角。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-kgzry6nd6d/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 507, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kgzry6nd6d/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1442, \"height\": 752, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kgzry6nd6d/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1364, \"height\": 352, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kgzry6nd6d/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1436, \"height\": 356, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kgzry6nd6d/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 764, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kgzry6nd6d/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1466, \"height\": 323, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kgzry6nd6d/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1464, \"height\": 328, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kgzry6nd6d/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1459, \"height\": 327, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kgzry6nd6d/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1459, \"height\": 324, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kgzry6nd6d/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1460, \"height\": 327, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1443, \"height\": 770, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1442, \"height\": 425, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1441, \"height\": 343, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1440, \"height\": 352, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1457, \"height\": 427, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1431, \"height\": 176, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1450, \"height\": 393, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 959, \"height\": 281, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1369, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1437, \"height\": 1813, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1438, \"height\": 1814, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1461, \"height\": 1076, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kgzry6nd6d/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1441, \"height\": 978, \"label\": \"Table\"}]"
motivation: 深度模型在时间序列噪声和异常值上易过拟合，现有统一优化所有时间步的方法导致性能不佳。
method: 提出选择性学习策略，仅对可泛化的时间步子集计算MSE损失进行优化。
result: 在多个基准数据集上验证了该方法能有效提升预测精度和鲁棒性。
conclusion: 选择性学习为深度学习时序预测训练提供了更鲁棒的新范式。
---

## Abstract
Benefiting from high capacity for capturing complex temporal patterns, deep learning (DL) has significantly advanced time series forecasting (TSF). However, deep models tend to suffer from severe overfitting due to the inherent vulnerability of time series to noise and anomalies. The prevailing DL paradigm uniformly optimizes all timesteps through the MSE loss and learns those uncertain and anomalous timesteps without difference, ultimately resulting in overfitting. To address this, we propose a novel selective learning strategy for deep TSF. Specifically, selective learning screens a subset of the whole timesteps to calculate the MSE loss in optimization, guiding the model to focus on generalizable timesteps while disregarding non-generalizable ones. Our framework introduces a dual-mask mechanism to target timesteps: (1) an uncertainty mask leveraging residual entropy to filter uncertain timesteps, and (2) an anomaly mask employing residual lower bound estimation to exclude anomalous timesteps. Extensive experiments across eight real-world datasets demonstrate that selective learning can significantly improve the predictive performance for typical state-of-the-art deep models, including 37.4% MSE reduction for Informer, 8.4% for TimesNet, and 6.5% for iTransformer.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
提出一种新颖的深度学习时间序列预测选择性学习策略来对抗过拟合。

### 2. 核心内容
针对深度时间序列模型因噪声和异常值易过拟合的问题，提出一种选择性学习策略，在优化时筛选泛化性好的时间步计算损失，引导模型忽略不可泛化的时间步。实验表明该方法能有效提升点预测的准确性和鲁棒性，为深度时序预测训练提供了新视角。

### 3. 对应检索需求
deep learning based neural forecasting techniques。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=kgzRy6nD6D](https://openreview.net/forum?id=kgzRy6nD6D)
