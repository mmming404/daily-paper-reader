---
title: Learning Pattern-Specific Experts for Time Series Forecasting Under Patch-level Distribution Shift
title_zh: 学习模式特定专家以应对时间序列预测中的块级分布偏移
authors: "Yanru Sun, Zongxia Xie, Emadeldeen Eldele, Dongyue Chen, Qinghua Hu, Min Wu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=CtoIG9Iwas"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 用于分布变化下时间序列预测的模式特定专家
tldr: 现有时间序列预测模型通常使用单一架构，难以捕捉数据中多种演化模式，导致泛化能力不足。本文提出TFPS，通过模式特定专家动态匹配不同时序模式，有效缓解分布漂移问题。在多个基准数据集上的实验表明，该方法显著提升了预测精度和鲁棒性，为复杂时序预测任务提供了更灵活高效的解决方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1306, \"height\": 503, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1446, \"height\": 640, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1238, \"height\": 359, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 635, \"height\": 391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 687, \"height\": 383, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1074, \"height\": 565, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1008, \"height\": 288, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 800, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 795, \"height\": 351, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ctoig9iwas/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 800, \"height\": 379, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1450, \"height\": 1127, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1448, \"height\": 367, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 738, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 682, \"height\": 247, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1377, \"height\": 387, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1423, \"height\": 782, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1021, \"height\": 1000, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1092, \"height\": 893, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1093, \"height\": 833, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 948, \"height\": 693, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 950, \"height\": 693, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1375, \"height\": 157, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1019, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1164, \"height\": 295, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1020, \"height\": 309, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ctoig9iwas/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1019, \"height\": 220, \"label\": \"Table\"}]"
motivation: 真实世界时间序列存在多种演化模式，单一模型难以捕捉，导致泛化差。
method: 提出TFPS架构，利用模式特定专家网络动态处理不同时序片段。
result: 在多个数据集上显著提升预测准确性和对分布偏移的鲁棒性。
conclusion: TFPS通过多专家机制有效缓解模式漂移，为时序预测提供新范式。
---

## Abstract
Time series forecasting, which aims to predict future values based on historical data, has garnered significant attention due to its broad range of applications. However, real-world time series often exhibit heterogeneous pattern evolution across segments, such as seasonal variations, regime changes, or contextual shifts, making accurate forecasting challenging. Existing approaches, which typically train a single model to capture all these diverse patterns, often struggle with the pattern drifts between patches and may lead to poor generalization. To address these challenges, we propose TFPS, a novel architecture that leverages pattern-specific experts for more accurate and adaptable time series forecasting. TFPS employs a dual-domain encoder to capture both time-domain and frequency-domain features, enabling a more comprehensive understanding of temporal dynamics. It then performs subspace clustering to dynamically identify distinct patterns across data segments. Finally, these patterns are modeled by specialized experts, allowing the model to learn multiple predictive functions. Extensive experiments on real-world datasets demonstrate that TFPS outperforms state-of-the-art methods, particularly on datasets exhibiting significant distribution shifts. The data and code are available: https://github.com/syrGitHub/TFPS.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **核心问题**：真实世界的时间序列数据在不同片段（patch）上往往呈现出异质的模式演化（如季节性波动、状态切换、上下文变化），存在明显的**块级分布偏移**。而现有主流方法通常采用**统一分布建模（UDM）**策略，即用一个共享模型去拟合所有片段，忽略了结构异质性和时序变化，导致模型泛化能力差，预测性能下降。
- **整体含义**：论文旨在打破统一建模的局限，提出一种**模式感知的时间序列预测框架**，通过学习多个模式特定的专家，动态地为不同分布特性的片段匹配合适的预测函数，从而更好地应对概念漂移和非平稳时序中的分布偏移。

### 2. 论文提出的方法论
- **整体架构**：提出 **TFPS（Time-Frequency Pattern-Specific）** 架构，包含三大核心组件：双域编码器（DDE）、模式识别器（PI）和模式专家混合（MoPE）。
- **嵌入层**：将输入序列分割成长度为 \(P\) 的补丁（patch），经线性投影后加入可学习的位置嵌入，以保留时间顺序信息。
- **双域编码器（DDE）**：
  - **时间域分支**：使用基于补丁的 Transformer 编码器（类似 PatchTST），通过多头自注意力提取全局趋势和时序依赖，得到时间特征 \(z_t\)。
  - **频率域分支**：将自注意力子层替换为 **2D 快速傅里叶变换（FFT）**，对补丁表示在时间和隐藏维度上进行傅里叶变换，仅保留实部，捕捉周期性结构和频谱特征，得到频率特征 \(z_f\)。
- **模式识别器（PI）**：
  - 基于**子空间聚类**思想，维护一组可学习的子空间基 \(D\)，通过正则项 \(R_1\)（正交约束）和 \(R_2\)（子空间互异性约束）保证基的稳定性和区分度。
  - 计算嵌入 \(z\) 与各子空间的亲和度 \(s_{ij}\)，并通过非线性锐化得到细化亲和度 \(\hat{s}_{ij}\)。
  - 利用 KL 散度最小化 \(\hat{S}\) 与 \(S\) 的差异，形成自监督聚类损失 \(L_{sub}\)，总损失 \(L_{PI} = \alpha(R_1+R_2) + \beta L_{sub}\)，从而动态识别出不同模式的补丁。
- **模式专家混合（MoPE）**：
  - **门控网络**：根据 PI 输出的聚类分配 \(s\)，通过 Softmax(TopK(s)) 生成专家权重，只激活相关性最高的前 \(k\) 个专家。
  - **专家网络**：每个空间（时间/频率）包含 \(K\) 个专家，每个专家是一个两层的 MLP（ReLU 激活），对输入特征进行变换。
  - **输出聚合**：加权求和各专家输出，得到 \(h_t\) 和 \(h_f\)，拼接后经线性层映射到预测序列。
- **损失函数**：总损失 \(L = L_{MSE} + L_{PI}^t + L_{PI}^f\)，即在 MSE 预测损失的基础上，同时优化时间和频率分支的聚类正则化损失。
- **算法流程**：输入时序→补丁嵌入→分别进入时/频编码器→PI 识别模式→MoPE 专家预测→拼接融合→输出预测。

### 3. 实验设计
- **数据集**：9 个公开的多变量时间序列数据集，覆盖能源、天气、交通、金融、医疗等领域：
  - ETT 系列（ETTh1, ETTh2, ETTm1, ETTm2）
  - Exchange-Rate（汇率）
  - Weather（气象）
  - Electricity（电力）
  - Traffic（交通）
  - ILI（流感样病例）
- **预测设置**：输入长度 \(L=96\)（ILI 为 104），预测长度 \(H \in \{96,192,336,720\}\)（ILI 为 \(\{24,36,48,60\}\)）。
- **对比方法**：共对比了十余种最新的强基线，包括：
  - **时间域方法**：PatchTST, DLinear, TimesNet, iTransformer
  - **频率域方法**：FEDformer, FITS
  - **时频混合方法**：TFDNet-IK, TSLANet
  - **基础模型**：AutoTimes, Moment, Timer
  - **归一化方法**：SIN, SAN, Dish-TS, RevIN
  - **MoE 与分布偏移方法**：MoLE, MoU, KAN4TSF, Koopa, SOLID, OneNet
- **评估指标**：均方误差（MSE）和平均绝对误差（MAE），所有基线均使用官方代码或严格按原设定复现，以保证公平性。

### 4. 资源与算力
- **硬件**：所有实验在**单张 NVIDIA RTX 3090（24GB 显存）**上完成。
- **软件**：基于 PyTorch 实现。
- **训练时长**：论文未明确给出完整的训练时间，但在附录 I 的效率分析中提供了推理时间（如 ETTh1-192 设定下平均推理时间 6.114 ms）和 GPU 显存占用（9.643 MB），与其他模型进行了效率对比。

### 5. 实验数量与充分性
- **主实验**：9 个数据集 × 4 个预测长度 = 36 种配置（ILI 为 4 个长度），总计 72 个实验设置（其中部分数据集与基线合计）。
- **消融实验**：系统移除 PI、用线性层替代 PI、仅保留编码器等，验证各组件贡献；还针对 PI 的具体约束（\(R_1\), \(R_2\)）、真实/虚部取舍、MoPE 替换为多输出预测器或堆叠注意力等进行了额外消融。
- **超参数分析**：对专家数量（时间/频率分支各 1/2/4/8 组合）、正则化系数 \(\alpha\) 和 \(\beta\) 进行了网格搜索和敏感性分析。
- **对比实验扩展**：不仅对比了常规时间序列模型，还专门对比了基础模型、多种归一化方法、MoE 方法及分布偏移应对方法，实验非常全面、客观，且统一了超参数搜索空间，确保了对比的公平性。
- **可视化分析**：包括预测曲线对比、专家专门化模式展示、t-SNE 嵌入可视化、Wasserstein 距离热力图等，定性验证了方法的有效性。
- 整体上，实验设计充分、覆盖广泛，能够有力支撑论文结论。

### 6. 论文的主要结论与发现
- TFPS 在 **72 个实验设定中的 57 个**取得了最优性能，尤其在分布偏移严重的 ETTh2、Weather、ILI 等数据集上提升显著，相对时间域方法 MSE 平均降低 9.5%，相对频率域方法降低 16.9%。
- **双域编码**能同时捕捉趋势和周期性模式，对概念漂移的辨识更为全面。
- **模式识别器 + 专家混合**能有效将不同模式的补丁动态分配给对应专家，避免了统一建模的过平滑问题，且具有一定的可解释性（专家自发分化出下降趋势、抛物线趋势等）。
- 与归一化方法相比，TFPS 保留了序列内在的非平稳性，增强了模型对真实分布的适应能力；与基础模型相比，在多数数据集上表现出更高精度，验证了模式特定建模的优势。
- 专家数量需要根据数据集的分布偏移程度调整：偏移越严重，通常需要更多的专家。

### 7. 优点
- **范式创新**：提出从“统一建模”到“模式特定专家建模”的转变，为时间序列预测提供了新思路。
- **双域融合设计**：时域与频域信息互补，强化了模型对不同时间尺度和周期特征的捕获能力。
- **端到端可学习聚类**：将子空间聚类嵌入神经网络，通过 KL 散度实现无监督模式识别，避免了显式标注。
- **动态稀疏专家路由**：Top-K 门控机制在提升模型表达能力的同时控制了计算开销，实现了性能与效率的较好平衡。
- **实验严密且广泛**：与大量 SOTA 方法进行公平对比，并进行多维度的消融与敏感性分析，结论可靠。
- **开源代码**：提供了数据和代码，便于复现和后续研究。

### 8. 不足与局限
- **补丁长度选择**：补丁长度 \(P\) 目前是启发式选取，无法自动适应多周期特性或不可整除的序列长度，限制了在真实多样场景下的灵活性。
- **静态专家架构**：专家数量是固定的，无法应对随时间不断涌现的全新模式（如全新的疫情爆发模式），对于演化式分布偏移（evolving distribution shift）支持不足。
- **部分场景提升有限**：在分布偏移较小的 Traffic 数据集上，TFPS 相比基础模型 Timer 略有不如，说明其优势依赖于数据中存在明显的模式异质性，泛化边界需进一步明确。
- **计算存储成本**：虽然推理速度快，但模型需维护多个专家的参数，专家数量增多会带来参数量增长，在极大规模数据下的训练和存储效率仍需优化。
- **实验数据局限性**：主要基于公开基准数据集，对真实工业环境中的高噪声、多模态、不规则采样等复杂情况的验证尚不充分。

（完）
