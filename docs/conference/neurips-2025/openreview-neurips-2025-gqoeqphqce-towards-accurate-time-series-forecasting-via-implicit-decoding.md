---
title: Towards Accurate Time Series Forecasting via Implicit Decoding
title_zh: 通过隐式解码实现准确的时间序列预测
authors: "Xinyu Li, Yuchen Luo, Hao Wang, Haoxuan Li, Liuhua Peng, Feng Liu, Yandong Guo, Kun Zhang, Mingming Gong"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=gqoeQPhQcE"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 提出新颖的隐式预测器（IF）解码模块以捕获全局模式
tldr: 现有时间序列模型多专注于历史建模，而预测阶段常采用逐点独立预测，忽略全局动态。本文从解码阶段创新，提出隐式预测器（IF），受分解预测启发，将预测视为整体，通过隐式解码捕获序列中的长短期模式。实验表明，IF能显著提升长期预测精度，为优化预测阶段提供了新方向。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-gqoeqphqce/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1383, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gqoeqphqce/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1294, \"height\": 635, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gqoeqphqce/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1443, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gqoeqphqce/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1178, \"height\": 485, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gqoeqphqce/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1446, \"height\": 1893, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gqoeqphqce/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1419, \"height\": 1872, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gqoeqphqce/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1453, \"height\": 772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-gqoeqphqce/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1448, \"height\": 778, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-gqoeqphqce/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1443, \"height\": 473, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gqoeqphqce/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 691, \"height\": 307, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gqoeqphqce/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 629, \"height\": 347, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gqoeqphqce/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 771, \"height\": 352, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gqoeqphqce/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1083, \"height\": 557, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gqoeqphqce/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1449, \"height\": 906, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gqoeqphqce/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1302, \"height\": 759, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gqoeqphqce/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1296, \"height\": 577, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-gqoeqphqce/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1442, \"height\": 1817, \"label\": \"Table\"}]"
motivation: 现有模型在预测阶段独立预测多个时间点，难以表达复杂的全局模式。
method: 提出隐式预测器（IF）作为额外解码模块，受分解预测启发，采用更精细的解码方式捕获全局动态。
result: IF显著提升了长期时间序列预测的准确性。
conclusion: 通过关注预测阶段解码方式，为时间序列预测提供了新的性能提升途径。
---

## Abstract
Recent booming time series models have demonstrated remarkable forecasting performance. However, these methods often place greater focus on more effectively modelling the historical series, largely neglecting the forecasting phase, which generates long-term forecasts by separately predicting multiple time points. Given that real-world time series typically consist of various long short-term dynamics, independent predictions over individual time points may fail to express complex underlying patterns and can lead to a lack of global views. To address these issues, this work explores new perspectives from the forecasting phase and proposes a novel Implicit Forecaster (IF) as an additional decoding module. Inspired by decomposition forecasting, IF adopts a more nuanced approach by implicitly predicting constituent waves represented by their frequency, amplitude, and phase, thereby accurately forming the time series. Extensive experimental results from multiple real-world datasets show that IF can consistently boost mainstream time series models, achieving state-of-the-art forecasting performance. Code is available at this repository: [https://github.com/rakuyorain/Implicit-Forecaster](https://github.com/rakuyorain/Implicit-Forecaster).

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究动机**：现有时间序列预测模型（TSF）普遍聚焦于优化“历史序列到隐藏表示”的编码阶段，但预测阶段（解码）常被忽视。绝大多数方法在解码时使用 MLP 对每个未来时间点进行**独立、逐点预测**，这种方式缺乏对序列整体波动趋势的全局视野，也难以表达现实序列中固有的**长短周期混合动态**。
- **核心问题**：独立预测多个时间点无法捕捉序列内部的复杂构成模式，导致预测缺乏整体一致性和可解释性。因此，需要从**预测阶段**出发，设计能够从全局视角推断序列组成的解码方式。

### 2. 论文提出的方法论
- **核心思想**：将未来时间序列视为多个不同频率的**周期性波动的叠加**。通过隐式预测这些组成波的**振幅、频率和相位**，再利用逆傅里叶变换（iDFT）合成完整的预测序列。该方法受分解预测启发，但更加精细化。
- **关键技术细节**：
  - **架构组成**：隐式预测器（IF）作为可直接替换现有模型输出层的解码模块，包含振幅预测头（AHead）、相位预测头（PHead）、DFT 模块和 iDFT 模块。
  - **输入特征**：接收编码器的隐藏表示 \(\mathbf{X}_{\text{enc}} \in \mathbb{R}^{N \times D}\)，并通过跳跃连接（skip-connection）利用原始输入序列的频谱振幅 \(|\mathbf{S}|\) 和相位 \(\arg(\mathbf{S})\)，其中 \(\mathbf{S} = \mathcal{F}(\mathbf{X}^\top)\)。
  - **振幅预测（AHead）**：使用一个两层 MLP，将拼接后的 \([\mathbf{X}_{\text{enc}}, |\mathbf{S}|]\) 映射为 \(P\) 个频率池中波的预测振幅 \(\hat{\mathbf{A}}\)，并取绝对值确保非负。
  - **相位预测（PHead）**：为解决相位的数值不连续问题（在 \(-\pi/\pi\) 边界跳变），改为预测相位的正弦和余弦分量，通过两个 MLP 输出 \(\hat{\alpha}\) 和 \(\hat{\beta}\)，再使用 \(\operatorname{atan2}(\hat{\alpha}, \hat{\beta})\) 恢复相位 \(\hat{\phi}\)。
  - **频率池扩展**：通常预测长度 \(L\) 对应 \(L\) 个频率分量。为更好地捕捉超低频趋势（周期长于 \(L\)），IF 将频率池大小扩展为 \(P \ge L\)，直接预测更低频分量，缓解频谱泄漏。
  - **序列合成**：利用 iDFT 将 \(\hat{\mathbf{A}} \cdot e^{j\hat{\phi}}\) 重建为完整序列，再截取前 \(L\) 个时间步作为最终预测输出。
  - **复杂度**：总时间复杂度为 \(O(P\log P)\)。

### 3. 实验设计
- **数据集**：涵盖 14 个常用真实数据集：ETTh1/ETTh2、ETTm1/ETTm2、ECL、Traffic、Weather、Exchange Rate、ILI、PEMS03/04/07/08 以及 Solar Energy，覆盖能源、交通、天气、经济、疾病等领域。
- **基准与对比方法**：选取 7 种不同架构的主流模型作为主干（baselines），包括 MLP 类（SOFTS）、Transformer 类（TimeXer、iTransformer、PatchTST、Crossformer）、RNN 类（SegRNN）和 CNN 类（TimesNet）。所有模型均采用官方实现，并在相同框架下与各自配备 IF 的版本进行对比。
- **评价指标**：使用均方误差（MSE）和平均绝对误差（MAE），并在多个标准化预测长度上进行评估（如 {96, 192, 336, 720} 等）。

### 4. 资源与算力
- 文中明确指出实验在 **单块 NVIDIA RTX 4090 GPU** 和 16 核 AMD EPYC 9654 CPU 上完成。训练采用 Adam 优化器和 L2 损失，训练轮数由早停策略自动决定。未提及具体总训练时长，但给出了不同解码器下每个训练迭代的耗时与显存占用，IF 效率较高，优于传统的 Transformer 解码器。

### 5. 实验数量与充分性
- **实验规模充足**：在 14 个数据集、多个预测长度下，对 7 种模型进行了全面对比，实验组数超过 70 组核心对比。
- **消融与分析充分**：包含解码器类型消融（替换为 Linear、MLP、Transformer 解码器）、跳跃连接消融（禁用/仅跳跃连接）、不同时长输入窗口下的性能对比、计算效率对比，以及权重与预测能量的可视化分析。
- **公平性保障**：所有对比方法均沿用原论文的超参数，未做额外调参；全部实验基于相同的标准化代码库（Time-Series-Library），确保了客观与公平。
- 此外，还提供了 5 次随机运行下的误差棒和配对 t 检验，进一步验证了提升的统计显著性（在 13/14 数据集上显著）。

### 6. 论文的主要结论与发现
- IF 能够**一致且显著地提升**各类主流预测模型的性能，尤其在 PEMS 等具有复杂、快速波动的交通数据集上，MSE 平均降低可达 30.4%。
- **MSE 的提升普遍比 MAE 更显著**，表明 IF 通过预测全局频率成分，有效增强了对序列整体趋势和长期模式的把握。
- 证明了**编码器已经能够提取到有用信息**，但原有的逐点解码方式不足以充分释放其潜力，优化预测阶段对于高精度 TSF 至关重要。
- 通过频率权重和能量分布的可视化，展现出 IF 能**隐式识别主导周期成分**，提供了更高的可解释性。

### 7. 优点
- **即插即用**：与模型架构解耦，可作为通用解码模块直接替换 MLP 输出层，无需修改编码器。
- **全局视角建模**：利用频域内波的振幅和相位进行整体预测，从根本上解决了逐点预测缺乏全局信息的问题。
- **创新的相位预测方式**：通过预测 sin/cos 连续分量来规避相位边界的不连续性，提升了训练稳定性。
- **实验设计扎实**：覆盖 14 个数据集、7 种基线模型，消融与统计检验全面，说服力强。
- **计算效率可控**：在取得显著性能提升的同时，计算开销仅略高于简单 MLP 解码器，远低于传统 Transformer 解码器。

### 8. 不足与局限
- **预测效率仍可优化**：当前方法预测了频率池中的所有频谱分量，未来可研究自适应选择最关键频率以进一步降低计算量。
- **固定频率池的次优性**：人为预定义的频谱尺寸 \(P\) 可能不完全匹配数据集的最优频率分布，存在改进空间。
- **应用场景限制**：目前设计主要针对确定性的长期预测任务，其在概率预测或分类等不同场景下的适配性尚待探索。
- **个别数据集增益不显著**：尽管整体提升明显，但在如 Solar 数据集上，对特定主干（如标准 Transformer）的提升未通过统计显著性检验，方法在极强规律性数据上的边际收益可能有限。

（完）
