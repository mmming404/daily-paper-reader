---
title: "This Time is Different: An Observability Perspective on Time Series Foundation Models"
title_zh: 这次不同：从可观测性视角审视时间序列基础模型
authors: "Ben Cohen, Emaad Khwaja, Youssef Doubli, Salahidine Lemaachi, Chris Lettieri, Charles Masson, Hugo Miccinilli, Elise Ramé, Qiqi Ren, Afshin Rostamizadeh, Jean Ogier du Terrail, Anna-Monica Toon, Kan Wang, Stephan Xie, Zongzhe Xu, Viktoriya Zhukova, David Asker, Ameet Talwalkar, Othmane Abou-Amal"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=1jDAYXfcS2"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 时间序列基础模型Toto，采用仅解码器架构及创新设计用于预测
tldr: Toto是一个具有1.51亿参数的时间序列预测基础模型，采用现代仅解码器架构，针对多元可观测数据设计创新组件，在混合大数据上预训练。在包含3.5亿观测值的BOOM基准上，Toto表现最优，证明了大尺度预训练和架构创新对预测任务的有效性，推动了时序基础模型的发展。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1450, \"height\": 977, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1453, \"height\": 580, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1447, \"height\": 290, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1446, \"height\": 323, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1456, \"height\": 262, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1458, \"height\": 525, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 753, \"height\": 583, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1240, \"height\": 477, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1436, \"height\": 428, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1421, \"height\": 886, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 714, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1jdayxfcs2/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1439, \"height\": 1819, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1450, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1447, \"height\": 216, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1450, \"height\": 174, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1444, \"height\": 607, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 833, \"height\": 965, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1552, \"height\": 650, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1451, \"height\": 226, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1445, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1435, \"height\": 117, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1446, \"height\": 124, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1450, \"height\": 162, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1446, \"height\": 187, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1446, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1444, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 446, \"height\": 2233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1447, \"height\": 1276, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1065, \"height\": 2294, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1444, \"height\": 1535, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1jdayxfcs2/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 944, \"height\": 292, \"label\": \"Table\"}]"
motivation: 现有时间序列基础模型未充分考虑可观测性数据特点和规模。
method: 设计仅解码器架构Toto，融合特定创新并在大规模数据上预训练。
result: 在自建的BOOM基准上显著超越领先模型。
conclusion: Toto展示了面向可观测性场景的基础模型潜力。
---

## Abstract
We introduce Toto, a time series forecasting foundation model with 151 million parameters. Toto uses a modern decoder-only architecture coupled with architectural innovations designed to account for specific challenges found in multivariate observability time series data. Toto's pre-training corpus is a mixture of observability data, open datasets, and synthetic data, and is 4-10$\times$ larger than those of leading time series foundation models. Additionally, we introduce BOOM, a large-scale  benchmark consisting of 350 million observations across 2,807 real-world time series.  For both Toto and BOOM, we source observability data exclusively from our own telemetry and internal observability metrics. Extensive evaluations demonstrate that Toto achieves state-of-the-art performance on both BOOM and on established general  purpose time series forecasting benchmarks. Toto's model weights, inference code, and evaluation scripts, as well as BOOM's data and evaluation code, are all available as open source under the Apache 2.0 License.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有的通用时间序列基础模型（TSFMs）主要针对一般领域设计，在面对**可观测性（Observability）数据**（例如分布式系统中的 CPU 负载、内存占用、网络吞吐、错误率、延迟等海量、高维、异构指标）时，其零样本（zero‑shot）预测能力严重不足。这些数据具有高度非平稳性、重尾分布、极端动态范围、多变量高基数以及稀疏/突发特性，传统监督学习或经典统计方法难以规模化应用。
- **整体含义**：本研究旨在通过**专门针对可观测性场景**设计一个时间序列基础模型 Toto，并同时推出一个全新的、大规模的可观测性时间序列基准 BOOM，以此填补该领域的评估空白，并验证领域特化预训练在该场景下的显著优势。论文题目“This Time is Different”暗指可观测性数据的分布和特性与通用时间序列有本质区别，需要不同的建模策略。

### 2. 论文提出的方法论：核心思想、关键技术细节

Toto 是一个**1.51 亿参数**的 decoder‑only Transformer 基础模型，其设计核心在于**四项专门针对可观测性数据挑战的架构创新**：

1. **基于块（Patch-based）的因果实例归一化（Causal Instance Normalization）**
   - **动机**：传统实例归一化或全局归一化在 next‑patch 预测任务中会泄露未来信息；而仅用第一个块的统计量对整个序列归一化对高度非平稳数据无效。
   - **方法**：采用**逐块因果缩放**。对每个时间步 $t$，利用 Welford 在线算法高效计算仅基于当前及过去数据的因果均值 $\hat{\mu}_t$ 和因果标准差 $\hat{s}_t$，并引入变体级别统计量进行裁剪（约束范围），在保留因果性的同时抑制极端非平稳带来的训练不稳定。最终归一化应用于每个块，块内时间步共享同一个归一化参数。

2. **比例分解注意力（Proportional Factorized Attention）**
   - **动机**：可观测性数据通常包含大量相关变量（高基数），全自注意力（同时处理时间和变量维度）计算昂贵；完全忽略变量交互会损失信息。
   - **方法**：将 Transformer 块分为两种类型：**时间维注意力块**（捕获单变量的时序依赖）和**变量维注意力块**（捕获同一时间点不同变量间的交互）。两者按固定比例交替排列，**不作逐层混合**，而是让时间维块占多数（最终采用 11:1 的时间‑变量块比例）。这种设计在计算复杂度上显著优于全自注意力，同时保留了必要的变量交互。

3. **学生 T 混合模型（Student‑T Mixture Model, SMM）预测头**
   - **动机**：可观测性数据分布复杂，常见高斯混合模型在面对极端离群值和高峰度时数值不稳定。
   - **方法**：用一个 $K$ 组分的学生 T 分布混合模型作为输出，每个组分由其均值 $\mu_k$、尺度 $\tau_k$、自由度 $\nu_k$ 和混合系数 $\pi_k$ 参数化。模型通过线性投影从解码器隐藏状态中预测这些参数。SMM 具有更厚的尾部，能更好地拟合重尾、偏斜的观测值。

4. **复合鲁棒损失（Composite Robust Loss）**
   - **动机**：仅最大化似然（NLL）会导致混合模型退化或崩溃，并且对异常值敏感。
   - **方法**：联合优化标准的负对数似然损失 $L_{\text{NLL}}$（衡量分布拟合）与一个基于 Cauchy 损失的鲁棒点预测损失 $L_{\text{Cauchy}}$（衡量预测均值与真值的误差）。最终损失为   $L = \lambda_{\text{NLL}} L_{\text{NLL}} + (1-\lambda_{\text{NLL}}) L_{\text{Robust}}$，其中超参数 $\lambda_{\text{NLL}}=0.57$，鲁棒参数 $\alpha=0$（Cauchy 形式）、$\delta=0.1$。该复合损失稳定了训练，避免退化。

另外，Toto 的预训练语料库十分庞大：包含约 **2.36 万亿**时间序列点（去重去合成后约 1.59 万亿），混合了**内部匿名可观测性指标**（约占 43%）、**公开数据集**（如 GIFT‑Eval Pretrain、Chronos 集合）以及**合成数据**。其规模是其它 TSFM 的 4‑10 倍。

### 3. 实验设计：数据集 / 场景、基准、对比方法

- **基准数据集**：
  - **BOOM**：全新构建的**大规模可观测性时间序列基准**，包含 2,807 个多变量序列、约 3.5 亿个观测点，涵盖应用、基础设施、数据库、网络、安全五个子域。同时提供一个较小的子集 BOOMLET (32 个序列，约 2,300 万点) 用于轻量评估。
  - **GIFT‑Eval**：通用多域时间序列基准，用于评估零样本泛化能力。
  - **LSF (Long Sequence Forecasting)**：传统的长序列预测基准（ETT、Electricity、Weather 等）。

- **对比方法**：
  - **零样本基础模型**：Moirai, TimesFM 2.0, Chronos (包括 Chronos‑Bolt), Timer, Time‑MoE, VisionTS, TabPFN‑TS（仅在 GIFT‑Eval 中）。
  - **全监督模型 / 基线**：Auto‑ARIMA, Auto‑ETS, Auto‑Theta, DLinear, DeepAR (在 BOOM/BOOMLET 上)，并在 LSF 上有大量全监督对手如 PatchTST, iTransformer, TiDE, TimeLLM, GPT4TS, xLSTMTime 等。

- **评估指标与协议**：
  - 主要使用与季节性朴素预测归一化后的 **MASE**（点预测）和 **CRPS**（概率预测），并报告平均 rank（基于 CRPS）。对包含近乎恒定子序列的情况，采用了 shifted geometric mean 聚合，并将极端退化序列单独用 MAE 和未归一化 CRPS 评估。
  - 预测长度根据序列频率设定（短、中、长），采用非重叠滚动窗口。

### 4. 资源与算力

论文明确说明了使用的算力资源，但**未给出具体 GPU 数量或总训练时长**，仅指出：
- 所有实验（超参搜索、最终模型训练、基准评估）在**配备 A100 和 H100 的 GPU 集群**上进行。
- 超参优化采用 Optuna（133 次迭代，每次训练 5 万步），最终 Toto 模型共训练 **135,001 步**（WSD 学习率调度）。
- 推理效率评估：在一张 NVIDIA A100 (40 GB) 上测试，Toto 在变量数增多时表现出最低的 FLOPs 和优秀的 wall‑time。

### 5. 实验数量与充分性

- **实验数量充足，覆盖多个维度**：
  - 分别在 **BOOM（全量）、BOOMLET、GIFT‑Eval、LSF** 四个基准上进行零样本评估，并在 LSF 上补充了全监督微调实验。
  - 在 BOOM 上按预测期、指标类型、应用域进行了分层分析（共 4 张详细表格）。
  - 进行了关键架构组件的**消融实验**（移除变体注意力、鲁棒损失、学生 T 混合、因果缩放），并分别报告 NLL 变化。
  - 提供了**计算效率基准测试**（不同变量数下的 FLOPs、CUDA 时间、内存等）。
  - **公平性**：所有模型统一使用 2048 步上下文窗口，建模预测长度一致，严格遵循 GIFT‑Eval 协议。数据划分上，BOOM 的训练数据来自生产环境，评估数据来自分离的预发环境，完全避免了数据泄露。

### 6. 论文的主要结论与发现

- Toto 在**专门的可观测性基准 BOOM 上大幅度领先**，相对次优模型（Moirai Base），CRPS 降低 **12.4%**，MASE 降低 **13.1%**，平均 rank 显著更低。
- 在**通用基准 GIFT‑Eval 上也取得了第一名**（平均 rank 5.495，MASE 0.673），证明可观测性特化设计对通用时序预测同样有益。
- 在**传统 LSF 基准上零样本**取得 8/12 指标的最优，**微调后同样成为全监督 SOTA**（平均 MAE 0.314, MSE 0.284），进一步证实模型的强大迁移能力。
- 统计分析表明，BOOM 的可观测性序列在自相关、异方差、非平稳性、平坦区域长度、偏度等方面**分布明显异于通用基准**，解释了通用 TSFM 失效的原因。
- 消融实验确认了四项架构创新均**贡献显著**，尤其是因果缩放和学生 T 混合，移除后 NLL 分别上升 27.3% 和 27.2%。

### 7. 优点：方法或实验设计上的亮点

- **领域特化的系统设计**：从数据（大规模预训练集 + 专有基准）到模型架构（四项创新）均紧贴可观测性数据的真实挑战，目标清晰。
- **创新的因果归一化**：利用 Welford 在线算法和 patch‑wise 方式，在保留因果性的同时高效处理非平稳性，对后续研究有参考价值。
- **灵活的比例分解注意力**：允许动态调节时间‑变量交互比例，平衡性能与效率，并在高变量场景下展现出优秀的扩展性。
- **复合鲁棒损失与 Student‑T 混合模型**的组合，有效解决了可观测性数据中重尾和异常值导致的训练不稳定问题，且消融证明其不可或缺。
- **基准构建严谨**：BOOM 不仅在规模上超越 GIFT‑Eval（总点数约 2 倍），还具有严格的生产/预发隔离保证无泄漏，附带领域标签便于细致分析。
- **全面且开放的对比**：在多个主流基准上与大量模型公平对比，并开源模型权重、代码、基准数据，极大促进可复现性。

### 8. 不足与局限：包括实验覆盖、偏差风险、应用限制等

- **固定间隔假设**：Toto 和大多数 TSFM 一样假定均匀采样，论文中采用启发式填充缺失值，但对于可观测性中常见的非规则采样未做原生支持。
- **未融入日历特征**：模型未利用时间戳信息（如星期、节假日），可能限制了在具有强周期模式数据上的性能。
- **对恒定序列的过度保守**：在 BOOM 平坦序列子集上，Toto 的 CRPS 略高（预测区间过宽），这可能源自预训练数据中大量异常的存在，或会导致下游异常检测中的误报增加。
- **算力与训练开销未详细披露**：虽提及 A100/H100 集群，但未公布训练 GPU‑小时数，使得其他团队难以准确估计复现成本。
- **微调仅在 LSF 上进行**：尽管在 LSF 上证明了微调能力，但在 BOOM 或其它真实可观测性下游任务上的微调或 adapter‑based 迁移尚未探索。
- **可观测性数据的广度和代表性**：预训练和基准数据全部来自同一公司的内部遥测，尽管规模巨大，但其分布可能存在**组织偏差**，不一定完全涵盖所有生产系统的特性。

（完）
