---
title: How Different from the Past? Spatio-Temporal Time Series Forecasting with Self-Supervised Deviation Learning
title_zh: 与过去有何不同？基于自监督偏差学习的时空时间序列预测
authors: "Haotian Gao, Zheng Dong, Jiawei Yong, Shintaro Fukushima, Kenjiro Taura, Renhe Jiang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=TgGH1bY6kl"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 基于自监督偏差学习的时空预测
tldr: 现有时空预测方法忽视当前输入与历史模式之间的动态偏差，这些偏差蕴含关键信号。本文提出ST-SSDL框架，通过自监督学习量化并利用这种偏差，将输入锚定历史平均值并离散化后期偏差。实验表明，该方法在城市交通等时空预测任务上显著超越现有模型，为动态模式感知预测提供了新机制。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-tggh1by6kl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 687, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tggh1by6kl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1434, \"height\": 409, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tggh1by6kl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1289, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tggh1by6kl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1441, \"height\": 790, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tggh1by6kl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 662, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tggh1by6kl/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1444, \"height\": 890, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tggh1by6kl/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1442, \"height\": 717, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tggh1by6kl/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1443, \"height\": 721, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tggh1by6kl/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1443, \"height\": 716, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tggh1by6kl/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1444, \"height\": 721, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-tggh1by6kl/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 941, \"height\": 321, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tggh1by6kl/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1453, \"height\": 1017, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tggh1by6kl/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1455, \"height\": 358, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tggh1by6kl/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1414, \"height\": 323, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tggh1by6kl/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1263, \"height\": 1076, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tggh1by6kl/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1351, \"height\": 313, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tggh1by6kl/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1461, \"height\": 1144, \"label\": \"Table\"}]"
motivation: 时空预测中，动态偏差信息未被充分利用。
method: 设计ST-SSDL，利用自监督偏差学习捕捉模式变化。
result: 在交通等时空预测基准上取得了最优性能。
conclusion: 偏差感知机制有效提升了时空预测的准确性和鲁棒性。
---

## Abstract
Spatio-temporal forecasting is essential for real-world applications such as traffic management and urban computing. Although recent methods have shown improved accuracy, they often fail to account for dynamic deviations between current inputs and historical patterns. These deviations contain critical signals that can significantly affect model performance. To fill this gap, we propose $\textbf{ST-SSDL}$, a $\underline{S}$patio-$\underline{T}$emporal time series forecasting framework that incorporates a $\underline{S}$elf-$\underline{S}$upervised $\underline{D}$eviation $\underline{L}$earning scheme to capture and utilize such deviations. ST-SSDL anchors each input to its historical average and discretizes the latent space using learnable prototypes that represent typical spatio-temporal patterns. Two auxiliary objectives are proposed to refine this structure: a contrastive loss that enhances inter-prototype discriminability and a deviation loss that regularizes the distance consistency between input representations and corresponding prototypes to quantify deviation. Optimized jointly with the forecasting objective, these components guide the model to organize its hidden space and improve generalization across diverse input conditions. Experiments on six benchmark datasets show that ST-SSDL consistently outperforms state-of-the-art baselines across multiple metrics. Visualizations further demonstrate its ability to adaptively respond to varying levels of deviation in complex spatio-temporal scenarios. Our code and datasets are available at https://github.com/Jimmy-7664/ST-SSDL.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：在交通流预测等时空预测任务中，现有方法大多聚焦于建模时空依赖关系，却普遍忽略了**当前观测序列与其历史典型模式之间的动态偏差**。这类偏差（如突发事件、政策干预、事故等所引发的模式突变）蕴含对未来状态的重要信号，但传统方法难以对其进行连续、可量化的建模。
- **整体含义**：论文提出，通过**自监督的方式显式学习并量化这种偏差**，能够增强时空预测模型在不同偏差水平下的适应能力，从而提升预测精度与鲁棒性。研究背景是城市计算与交通管理对精准预测的迫切需求，以及现有模型在面对输入分布漂移时泛化能力不足。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：利用**历史平均作为自监督锚点**，通过一组**可学习原型（prototypes）离散化连续潜在空间**，并设计**对比损失**与**偏差损失**使该空间内保持“相对距离一致性”（即物理空间中输入与锚点之间的距离关系应在潜在空间中得到保持），从而让模型自发地学会量化偏差并利用其辅助预测。

- **关键组件与流程**：
  - **历史锚点构建**：将训练序列按周分割，计算每周同时刻的平均值得到历史锚点序列 \(X_a\)，与当前输入 \(X_c\) 一并送入共享编码器（GCRU），得到隐藏表示 \(H_c, H_a\)。
  - **原型离散化**：设置一组可学习原型 \(\{P_1,\dots,P_M\}\)，通过查询-原型注意力（公式3）计算每个样本的归属分数，选取最高与次高评分原型作为正样本 \(P_c\) 及负样本 \(N_c\)。
  - **对比损失**（公式4）：\(L_{Con} = \max(\| \text{sg}(Q_c) - P_c\|_2^2 - \| \text{sg}(Q_c) - N_c\|_2^2 + \delta, 0)\)，增强原型之间的可分性，并防止模型坍缩到单一原型。
  - **偏差损失**（公式5）：\(L_{Dev} = \| \text{sg}(\|Q_c - Q_a\|_1) - \|P_c - P_a\|_1\|_1\)，强制“物理空间距离 ≈ 潜在原型间距离”，实现相对距离一致性。
  - **预测主干**：编码器-解码器结构，采用 GCRU（图卷积循环单元）作为序列编码器。将增强后的隐藏状态拼接并生成自适应邻接矩阵，用于解码器完成未来多步预测。
  - **总损失**：\(L = L_{MAE} + \lambda_{Con} L_{Con} + \lambda_{Dev} L_{Dev}\)。

### 3. 实验设计：使用了哪些数据集 / 场景，它的 benchmark 是什么，对比了哪些方法

- **数据集**：6 个广泛使用的时空预测基准：
  - 交通速度：METRLA (207 传感器)、PEMSBAY (325 传感器)、PEMSD7(M) (228 传感器)。
  - 交通流量：PEMS04 (307 传感器)、PEMS07 (883 传感器)、PEMS08 (170 传感器)。
  - 时间粒度均为 5 分钟，输入和预测窗口均为 12 步（1 小时）。

- **评价指标**：MAE、RMSE、MAPE（不同预测步长或所有步长平均）。

- **对比基线**：涵盖统计方法 HI、单变量模型 GRU，以及多种时空预测模型 STGCN、DCRNN、Graph WaveNet、MTGNN、AGCRN、GTS、STNorm、STID、ST-WA、MegaCRN、STDN 等。

### 4. 资源与算力：如果文中有提到，请总结使用了多少算力（GPU 型号、数量、训练时长等）。若未明确说明，也请指出这一点

- 论文提到实验在 **NVIDIA RTX 5000 Ada Generation** GPU 上进行。
- **未明确说明** GPU 的具体数量（推测为单卡或少量）。
- 效率对比表中提供了不同模型在 METRLA 等数据集上每 epoch 训练时间及推理时间（如 ST-SSDL 在 METRLA 上训练 71.84 秒/epoch，推理 8.65 秒），但未给出完整训练轮数或总时间。
- 从参数数量看，ST-SSDL 在多数数据集上参数规模与轻量模型相当（例如 PEMS08 上仅 100K），但推理时间因循环结构而稍长。

### 5. 实验数量与充分性：大概做了多少组实验（如不同数据集、消融实验等），这些实验是否充分、是否客观、公平

- **总体实验组数**：
  - 主表在 6 个数据集上，针对不同预测步长/平均指标，共约 18 组对比。
  - 消融实验（6 个变体 × 6 数据集）总计 36 组。
  - 效率对比（6 数据集 × 13 左右模型）较多组。
  - 超参数敏感性（2 数据集 × 多种 M 与 d 组合）约 50+ 组。
  - 案例可视化（多场景：低/中/高偏差、缺失值）以及潜在空间可视化、原型物理模式展示。
- **充分性与公平性**：
  - 数据集选择广泛，涵盖交通速度与流量两种类型，规模不一。
  - 对比基线全面，包含 GCN、注意力、Transformer、MLP 等不同范式。
  - 使用统一的数据划分、指标，代码开源，保证了可复现性与公平性。
  - 消融和超参数研究详细验证了所提出的组件有效性。

### 6. 论文的主要结论与发现

- ST-SSDL 在所有 6 个基准上均取得**最优性能**，显著优于前沿基线。
- **自监督偏差学习**的每个组件（对比损失、偏差损失）均是必要的，去除任一都会导致性能下降；完全移除 SSDL 模块（退化为普通 GCRU）表现最差。
- 模型能根据输入与历史锚点的偏差程度，动态调整查询与原型之间的映射关系：低偏差时查向同一原型，高偏差时映射到相距较远的原型，体现了**自适应偏差建模能力**。
- 在部分缺失值场景下仍保持鲁棒预测，说明偏差建模有助于处理数据异常。

### 7. 优点：方法或实验设计上有哪些亮点

- **问题新颖性**：首次以自监督方式显式建模时空序列中的连续动态偏差，不同于简单的二值异常检测。
- **方法论创新**：
  - 将历史平均作为自然锚点，无需额外标注。
  - 用可学习原型离散化潜在空间，并构建相对距离一致性损失，巧妙地将物理距离转化为潜在空间距离正则。
  - 通过 stop-gradient 防止模型坍缩至平凡解。
- **实验扎实**：在多种速度与流量数据集上一致最优；消融、超参数、效率、可视化分析全面，增强了说服力。
- **架构简洁**：仅基于轻量 GCRU 编码器，未引入复杂注意力或 Mamba 等模块，参数效率高，效果却超越许多重型模型。

### 8. 不足与局限：包括实验覆盖、偏差风险、应用限制等

- **计算效率受限**：使用循环 GCRU 作为骨干，导致推理时间相对较长，尤其在节点数较多的数据集（如 PEMS07）上，实时性可能受限。
- **偏差建模依赖周期锚点**：历史锚点基于每周平均，适用于具有固定周期性的交通数据，对于无明显周期或周期变化大的场景（如突发事件、长期依赖）、或者跨度较短的数据可能不够有效。
- **原型设计与超参数**：原型数量 M 和维度 d 需手工设定，虽实验显示一定鲁棒性，但迁移到新领域时仍需调参。
- **实验局限性**：
  - 仅测试了交通速度和流量两种类型，未涉及其他时空数据（如气象、能源、流行病等）。
  - 缺乏极端长序列预测（如 2 小时以上）实验。
  - 未讨论模型在不同季节、异常事件（如节假日）下的专门评估。
- **偏差与社会风险**：论文未深入讨论传感器分布不均可能带来的预测偏差，以及该偏差对交通资源分配公平性的潜在影响。
- **模型复杂度**：添加了原型注意力与自适应图生成，虽然参数增多不多，但计算图相对复杂，可能对分布式训练或端侧部署不太友好。

（完）
