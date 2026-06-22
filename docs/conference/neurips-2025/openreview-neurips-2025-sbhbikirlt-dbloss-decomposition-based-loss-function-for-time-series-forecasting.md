---
title: "DBLoss: Decomposition-based Loss Function for Time Series Forecasting"
title_zh: DBLoss：面向时间序列预测的基于分解的损失函数
authors: "Xiangfei Qiu, Xingjian Wu, Hanyin Cheng, Xvyuan Liu, Chenjuan Guo, Jilin Hu, Bin Yang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=SbhBIkiRLT"
tags: ["query:ts-forecast"]
score: 8.0
evidence: 基于分解的损失函数，分别惩罚趋势和季节性误差
tldr: 传统MSE损失无法充分捕捉预测序列中的趋势和季节性，即使模型包含分解模块。本文提出DBLoss，利用指数移动平均将预测窗口分解为趋势和季节成分，并分别计算损失。该简单方法可与多种模型结合，实验表明它持续提升了预测精度，尤其在趋势和季节性显著的数据上，为损失函数设计提供了新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbhbikirlt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 367, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbhbikirlt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1441, \"height\": 380, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbhbikirlt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1440, \"height\": 767, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbhbikirlt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1449, \"height\": 239, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbhbikirlt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 865, \"height\": 374, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbhbikirlt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1467, \"height\": 1180, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbhbikirlt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1451, \"height\": 1359, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbhbikirlt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1457, \"height\": 416, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbhbikirlt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1451, \"height\": 559, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbhbikirlt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1452, \"height\": 444, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbhbikirlt/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1448, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbhbikirlt/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1027, \"height\": 460, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbhbikirlt/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1025, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbhbikirlt/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1025, \"height\": 460, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbhbikirlt/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1449, \"height\": 174, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbhbikirlt/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1450, \"height\": 1361, \"label\": \"Table\"}]"
motivation: 现有MSE损失即使配合分解模块，仍难以准确捕获预测窗口中的趋势和季节性模式。
method: 提出DBLoss，使用指数移动平均分解预测序列，分别计算趋势和季节性分量的损失。
result: DBLoss与多种模型结合均能持续提升预测性能，尤其在趋势季节性明显的数据上。
conclusion: 简单而有效的分解损失为增强时间序列模型训练提供了通用工具。
---

## Abstract
Time series forecasting holds significant value in various domains such as economics, traffic, energy, and AIOps, as accurate predictions facilitate informed decision-making. However, the existing Mean Squared Error (MSE) loss function sometimes fails to accurately capture the seasonality or trend within the forecasting horizon, even when decomposition modules are used in the forward propagation to model the trend and seasonality separately. To address these challenges, we propose a simple yet effective Decomposition-Based Loss function called DBLoss. This method uses exponential moving averages to decompose the time series into seasonal and trend components within the forecasting horizon, and then calculates the loss for each of these components separately, followed by weighting them. As a general loss function, DBLoss can be combined with any deep learning forecasting model. Extensive experiments demonstrate that DBLoss significantly improves the performance of state-of-the-art models across diverse real-world datasets and provides a new perspective on the design of time series loss functions.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
基于分解的损失函数，分别惩罚趋势和季节性误差。

### 2. 核心内容
传统MSE损失无法充分捕捉预测序列中的趋势和季节性，即使模型包含分解模块。本文提出DBLoss，利用指数移动平均将预测窗口分解为趋势和季节成分，并分别计算损失。该简单方法可与多种模型结合，实验表明它持续提升了预测精度，尤其在趋势和季节性显著的数据上，为损失函数设计提供了新思路。

### 3. 对应检索需求
deep learning based neural forecasting techniques。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=SbhBIkiRLT](https://openreview.net/forum?id=SbhBIkiRLT)
