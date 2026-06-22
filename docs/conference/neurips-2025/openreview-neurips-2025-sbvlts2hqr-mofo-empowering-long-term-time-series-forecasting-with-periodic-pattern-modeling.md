---
title: "MoFo: Empowering Long-term Time Series Forecasting with Periodic Pattern Modeling"
title_zh: MoFo：通过周期模式建模提升长期时间序列预测
authors: "Jiaming Ma, Binwu Wang, Qihe Huang, Guanjun Wang, Pengkun Wang, Zhengyang Zhou, Yang Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=sbvLts2HqR"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 周期结构化分块同时建模周期对齐相关性和周期偏移趋势
tldr: 针对现有模型难以有效捕获时间序列稳定周期模式的问题，本文提出MoFo，将周期性解释为周期对齐时间步的相关性与周期偏移时间步的趋势。通过设计周期结构化分块，将序列重组为二维张量，行表示周期对齐点，列表示周期内偏移点，从而直接建模这两种结构。实验证明，MoFo在长时预测任务中优于现有方法，为周期建模提供了新范式。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbvlts2hqr/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1447, \"height\": 629, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbvlts2hqr/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1436, \"height\": 478, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbvlts2hqr/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1461, \"height\": 400, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbvlts2hqr/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1447, \"height\": 433, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbvlts2hqr/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1443, \"height\": 257, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbvlts2hqr/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1423, \"height\": 299, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-sbvlts2hqr/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1433, \"height\": 2064, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1308, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1449, \"height\": 1059, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1444, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1448, \"height\": 1074, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 739, \"height\": 250, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 722, \"height\": 449, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1027, \"height\": 343, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 740, \"height\": 258, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1447, \"height\": 508, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 741, \"height\": 259, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-sbvlts2hqr/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1444, \"height\": 415, \"label\": \"Table\"}]"
motivation: 现有模型受限于连续混沌的输入划分和弱归纳偏置，难以捕获稳定周期结构。
method: 提出MoFo，设计周期结构化分块，将一维序列重组为二维张量，分别建模周期对齐和偏移依赖。
result: 在长时预测上取得显著提升，验证了显式周期建模的有效性。
conclusion: MoFo为时间序列的周期模式利用提供了一种简单而强大的架构设计。
---

## Abstract
The stable periodic patterns present in the time series data serve as the foundation for long-term forecasting. However, existing models suffer from limitations such as continuous and chaotic input partitioning, as well as weak inductive biases, which restrict their ability to capture such recurring structures. In this paper, we propose MoFo, which interprets periodicity as both the correlation of period-aligned time steps and the trend of period-offset time steps. We first design period-structured patches—2D tensors generated through discrete sampling—where each row contains only period-aligned time steps, enabling direct modeling of periodic correlations. Period-offset time steps within a period are aligned in columns. To capture trends across these offset time steps, we introduce a period-aware modulator. This modulator introduces an adaptive strong inductive bias through a regulated relaxation function, encouraging the model to generate attention coefficients that align with periodic trends. This function is end-to-end trainable, enabling the model to adaptively capture the distinct periodic patterns across diverse datasets. Extensive empirical results on widely used benchmark datasets demonstrate that MoFo achieves competitive performance while maintaining high memory efficiency and fast training speed.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有基于 Transformer 的长期时间序列预测方法在捕获数据中固有的稳定周期模式方面存在两个关键瓶颈：  
  ① **连续却混乱的输入划分**：传统连续分块（patch）策略会将周期内相位对齐（period-aligned）和偏移（period-offset）的时间步混合在同一块中，导致块内相关性强弱不一甚至包含噪声，阻碍周期关系的学习。  
  ② **对周期性的弱归纳偏置**：Transformer 的自注意力机制具有置换不变性，而常用的正弦位置编码或绝对时间戳编码难以反映真实的相对周期距离，致使模型难以关注周期相关的远距离时间步。
- **整体含义**：本文提出 **MoFo**（Modulator Forecaster），将周期模式建模拆解为两个维度——**同相位时间步的相关性** 与 **跨偏移时间步的趋势**，并设计相应的架构组件显式捕捉这两类周期依赖，从而在长期预测任务中取得更优的精度和效率。

### 2. 论文提出的方法论

#### 2.1 周期结构化分块
- 给定周期长度 $P$，将输入序列 $\mathbf{X} \in \mathbb{R}^T$ 填充至 $T' = P \cdot \lceil T/P \rceil$ (不足部分用相邻周期数据补全)。
- 以间隔 $P$ 离散采样将序列重整为二维张量 $\mathbf{X}_{in} \in \mathbb{R}^{P \times \lceil T/P \rceil}$。
  - **行**（即每个 patch）：只包含不同周期中相位对齐的时间步，便于直接建模长程周期相关性。
  - **列**（跨 patch）：对应一个完整周期内的所有偏移时间步，用以捕捉周期内趋势。
- 通过一个简单的单层 MLP 将每行（patch）映射为 $d$ 维表示 $\mathbf{Z} \in \mathbb{R}^{P \times d}$。

#### 2.2 周期感知调制器
- 计算**相对周期距离矩阵** $\mathbf{\Gamma} = \{\gamma_{ij}\}$，其中 $\gamma_{ij} = \min\{(i-j)\bmod P, (j-i)\bmod P\}$，使周期上相近的时间步获得小的距离值。
- 引入一个可学习的**调控松弛函数** $S(\gamma; \alpha, \beta)$ 作为 Heaviside 阶梯函数的平滑近似：  
  $$S(\gamma; \alpha, \beta) = \frac{1}{1+e^{\alpha(\gamma-\beta)}} + \frac{e^{-\gamma}}{1+e^{\alpha\beta}} \in [0,1]$$
  其中 $\alpha>0$ 控制衰减梯度，$\beta>0$ 为距离惩罚阈值，二者均通过反向传播自适应学习。
- 该函数生成调制项 $\log S(\mathbf{\Gamma}; \alpha, \beta)$，加入注意力计算：  
  $$\text{RRF}(\mathbf{Q},\mathbf{K},\mathbf{V}) = \text{Softmax}\!\left(\frac{\mathbf{Q}\mathbf{K}^\top}{\sqrt{d_h}} + \log S(\mathbf{\Gamma}; \alpha, \beta)\right)\mathbf{V}$$
  从而强制注意力系数随周期性距离平滑衰减，为模型注入利于周期趋势的强归纳偏置，并解决置换不变性问题。
- 整个 Transformer 层仅使用单层，结合 Gated Linear Units、RMSNorm 等优化，最终将输出展平后线性投影得到预测 $\hat{\mathbf{Y}}$。

#### 2.3 多变量处理与优化
- 多变量序列采用**通道独立**策略，各变量独立建模。
- 基于通道最大损失动态调整各通道的相对权重，提升训练稳定性。
- 使用 FreDF 策略的 L1 损失进行优化。

### 3. 实验设计

- **数据集**：8 个来自不同领域的真实世界周期时间序列数据集，包括 ETTh1, ETTh2, ETTm1, ETTm2, Weather, Solar Energy, Electricity, Traffic（频率涵盖 10 分钟、15 分钟、1 小时）。
- **评估指标**：均方误差（MSE）和平均绝对误差（MAE）。
- **预测设置**：遵循 TFB 平台标准，回看窗口 $T \in \{96,336,512\}$，预测长度 $L \in \{96,192,336,720\}$，取各模型最优 $T$ 下的最佳结果。
- **对比方法**：17 个先进基线，包括 DUET, PDF, iTransformer, Pathformer, CycleNet, TimeMixer, PatchTST, Crossformer, DLinear, NLinear, FITS, FiLM, MICN, FEDformer, Triformer, Non‑stationary Transformer, Informer，覆盖 MLP、TCN、RNN、Transformer 等多种架构。
- **其它实验**：效率对比（参数量、MACs、FLOPs、内存、训练时间）、超参数敏感性（层数、维度）、消融实验（各组件替换或移除）、回看窗口可扩展性（最长 10K 步）、注意力可视化等。

### 4. 资源与算力

- **硬件**：实验基于一张 NVIDIA A100 GPU（40 GB 显存）。
- **软件**：PyTorch，Python 3.11.5。
- **训练时长**：文中给出了 Traffic 数据集单个 epoch 的训练时间（47 s），并与其他方法作了对比；对于极长回看窗口（10K）的可扩展性实验，也报告了内存、时间等开销，但未给出所有实验的总训练时长或总 GPU 小时。

### 5. 实验数量与充分性

- 在 8 个主流数据集上，对 4 种预测长度分别评估了所有对比方法，总计核心预测表格包含 **8×4 = 32 项**，并进一步在附录中与更多基线比较。
- 进行了详细的**消融研究**（替换连续分块、不同位置编码、移除调制器、损失函数等），覆盖全部数据集，验证了各模块的必要性。
- 开展了**效率分析**（参数、计算量、内存、速度）和**可扩展性实验**（回看窗口至 10000 步），以及**超参数敏感性**、**周期长度鲁棒性**（单周期微调、多周期共存、动态变化周期）、**非周期数据集**（ILI）上的泛化实验。
- 对比严格遵循 TFB 平台的公平基准，禁用“Drop Last”等 tricks，选用回看窗口最优配置，并使用了独立的测试集。
- 总体实验设计非常全面，从精度、效率、消融、鲁棒性多个维度进行了验证，具有较好的充分性和客观公平性。

### 6. 论文的主要结论与发现

- MoFo 通过周期结构化分块和周期感知调制器，显式捕获周期内对齐点的相关性和跨偏移点的趋势，在多个基准数据集上取得了**最优或次优的预测精度**。
- 相较于其它 Transformer 模型，MoFo 在参数量、计算量、内存占用和训练速度上具有显著优势（例如 Traffic 数据集上比 DUET 节省 10× 以上 FLOPs 和近 10× 训练时间）。
- 只需单层 Transformer 即可达到高性能，计算复杂度仅与周期长度相关，与总序列长度无关，因此即使回看窗口扩大 100 倍，内存和训练时间也无明显增加，展现了优秀的可扩展性。
- 消融实验证实，周期结构化分块和调制器是模型性能的关键；周期距离的精确估计对性能有重要影响，但模型对微小的周期变化和多周期共存仍表现出较强的鲁棒性。

### 7. 优点

- **独特的周期视角**：将周期模式解耦为相位对齐相关性与偏移趋势，为长时预测提供了更精细的建模维度。
- **显式结构设计**：周期结构化分块将一维序列重组为二维张量，直接对齐周期性依赖，简单却有效。
- **自适应强偏置**：可学习的调控松弛函数使注意力机制自动适应不同数据集的周期特性，克服了传统位置编码的局限。
- **高精度 + 高效率**：在保持先进精度的同时，大幅降低了内存和计算开销，具备优秀的实际部署潜力。
- **全面的实验验证**：覆盖多领域、多周期类型的数据集，对比众多基线，并进行了深入的消融和鲁棒性分析，实验结论令人信服。

### 8. 不足与局限

- **周期先验依赖**：方法需要预先给定周期长度 $P$，文中虽讨论了多周期共存和周期估计的鲁棒性，但在没有明显周期或周期难以确定的场景下性能如何，仍需进一步研究（仅在 ILI 数据上试过）。
- **调制器限制于标准注意力**：当前设计的周期感知调制器仅适用于复杂度为 $O(P^2)$ 的原始自注意力，无法直接扩展至线性复杂度的注意力变体，限制了其在超长周期（$P$ 很大）下的应用。
- **多变量交互简单**：采用通道独立策略，未显式建模变量间的相互关系，在多变量强耦合场景下可能不够充分。
- **可能对复杂周期混合场景的泛化未知**：虽然通过综合数据集测试了动态周期，但未在更复杂的真实场景（如不规律周期、多种周期同时存在且强度不一）中系统评估，可能存在性能下降的风险。

（完）
