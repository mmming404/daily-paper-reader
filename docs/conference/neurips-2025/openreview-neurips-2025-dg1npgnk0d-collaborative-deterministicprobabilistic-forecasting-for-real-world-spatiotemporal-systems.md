---
title: Collaborative Deterministic–Probabilistic Forecasting for Real-World Spatiotemporal Systems
title_zh: 面向真实世界时空系统的协同确定性-概率性预测
authors: "Zhi Sheng, Yuan Yuan, Yudi Zhang, Yong Li"
date: 2025-05-06
pdf: "https://openreview.net/pdf?id=dg1npGNK0d"
tags: ["query:ts-forecast"]
score: 10.0
evidence: 协同框架结合确定性模型和扩散模型，用于概率时空预测并量化不确定性。
tldr: 针对扩散模型用于时空概率预测时计算量大、动力学复杂的问题，提出CoST框架，通过均值-残差分解，用强大的确定性模型捕捉条件均值，轻量扩散模型学习残差分布。该方法在多个真实系统上实现了高效且准确的不确定性量化概率预测。
source: NeurIPS-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-dg1npgnk0d/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 712, \"height\": 391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dg1npgnk0d/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1394, \"height\": 616, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dg1npgnk0d/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 864, \"height\": 564, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dg1npgnk0d/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1429, \"height\": 285, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dg1npgnk0d/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 737, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dg1npgnk0d/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1115, \"height\": 560, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dg1npgnk0d/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1147, \"height\": 489, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dg1npgnk0d/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1195, \"height\": 422, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-dg1npgnk0d/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1091, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dg1npgnk0d/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1449, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dg1npgnk0d/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1453, \"height\": 297, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dg1npgnk0d/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1448, \"height\": 868, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dg1npgnk0d/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1443, \"height\": 420, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dg1npgnk0d/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1165, \"height\": 303, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dg1npgnk0d/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 871, \"height\": 295, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dg1npgnk0d/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1451, \"height\": 309, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dg1npgnk0d/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 730, \"height\": 350, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dg1npgnk0d/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1020, \"height\": 299, \"label\": \"Table\"}]"
motivation: 扩散模型时空预测面临高计算负担和动态复杂性，需要高效量化不确定性。
method: 提出CoST框架，确定性模型预测均值，轻量扩散模型建模残差分布。
result: 在气候、能源等系统中，CoST提供精确概率预测和可靠不确定性区间。
conclusion: 协同设计大幅提升了扩散模型在时空概率预测中的实用性和效率。
---

## Abstract
Probabilistic forecasting is crucial for real-world spatiotemporal systems, such as climate, energy, and urban environments, where quantifying uncertainty is essential for informed, risk-aware decision-making. While diffusion models have shown promise in capturing complex data distributions, their application to spatiotemporal forecasting remains limited due to complex spatiotemporal dynamics and high computational demands. In this work, we propose CoST, a novel framework that collaborates deterministic and diffusion models for spatiotemporal forecasting. 
CoST formulates a mean-residual decomposition strategy: it leverages a powerful deterministic model to capture the conditional mean and a lightweight diffusion model to learn residual uncertainties
This collaborative formulation simplifies learning objectives, enhances forecasting accuracy, enables uncertainty quantification, and significantly improves computational efficiency. To address spatial heterogeneity, we further design a scale-aware diffusion mechanism to guide the diffusion process. Extensive experiments across ten real-world datasets from climate, energy, communication, and urban systems show that CoST achieves 25% performance gains over state-of-the-art baselines, while significantly reducing computational cost. Code and datasets are available at: https://anonymous.4open.science/r/CoST_8069.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

*   **核心问题**：在气候、能源、城市等真实世界的时空系统中，概率性预测对于风险感知决策至关重要，因为它能够量化预测结果的不确定性。扩散模型在捕捉复杂数据分布方面表现出色，但将其直接应用于时空预测面临两大挑战：1) 时空系统固有的复杂动态（如周期性、季节性趋势和随机波动）难以被扩散模型有效学习；2) 扩散模型的多步采样过程计算开销巨大，限制了其在现实场景中的实用性。
*   **研究动机**：现有方法大多试图通过向扩散过程中注入时间条件或先验来弥补其在时序建模上的不足，但效果有限。本文提出一个新视角：不应让扩散模型独立承担学习完整数据分布的全部负担，而应采用一种协同方式，结合确定性模型在捕捉规则模式上的效率和扩散模型在不确定性量化上的优势。
*   **整体含义**：该研究旨在通过一种“均值-残差分解”的协同框架，简化学习目标、提升预测精度、实现不确定性量化，并显著降低计算成本，从而推动概率性时空预测在实际系统中的应用。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

**核心思想：均值-残差分解（Mean-Residual Decomposition）**

*   **核心策略**：将时空数据的预测任务解耦为两部分。首先，用一个强大的确定性模型预测未来数据的**条件均值 \(\mathbb{E}[\mathbf{y}|\mathbf{x}]\)**（即数据中的规则模式）。然后，用一个轻量级的扩散模型专门学习**残差分布 \(p(\mathbf{r}|\mathbf{x})\)**（即数据中的随机波动和不确定性）。
*   **理论依据**：
    *   数据分解为：\( \mathbf{x}^{\text{ta}} = \underbrace{\mathbb{E}[\mathbf{x}^{\text{ta}}|\mathbf{x}^{\text{co}}]}_{\text{:= }\mu (\text{Deterministic})} + \underbrace{(\mathbf{x}^{\text{ta}} - \mathbb{E}[\mathbf{x}^{\text{ta}}|\mathbf{x}^{\text{co}}])}_{\text{:= }\mathbf{r} (\text{Diffusion})} \)
    *   若确定性模型准确预测了均值，则残差 \(\mathbf{r}\) 的方差将小于原始数据 \(\mathbf{x}^{\text{ta}}\) 的方差，且期望为0。这使得扩散模型只需要学习一个更简单、方差更小的分布，极大降低了其建模负担。

**关键技术细节与流程**

*   **第一阶段：均值预测（确定性模型）**
    *   采用一个已有的高性能时空预测架构（如 STID、ConvLSTM、iTransformer 等）作为骨干网络。
    *   使用历史数据 \( \mathbf{x}^{\text{co}} \) 作为输入，以 L2 损失函数（\( \mathcal{L}_2 = ||\mathbb{E}_\theta[\mathbf{x}^{\text{ta}}|\mathbf{x}^{\text{co}}] - \mathbf{x}^{\text{ta}}_0||^2_2 \)）进行预训练，使其输出对条件均值的估计。

*   **第二阶段：残差学习（尺度感知扩散模型）**
    *   **残差目标**：扩散模型的建模目标从原始数据 \( \mathbf{x}^{\text{ta}} \) 替换为残差 \( \mathbf{r}^{\text{ta}} = \mathbf{x}^{\text{ta}} - \mathbb{E}_\theta[\mathbf{x}^{\text{ta}}|\mathbf{x}^{\text{co}}] \)。
    *   **自定义波动尺度 \( \mathbf{Q} \)**：为解决空间异质性，首先使用快速傅里叶变换（FFT）从训练集中提取每个空间单元的波动成分，并计算其方差 \( \sigma^2_v \)，得到一个方差张量 \( \mathbf{M} \)。然后，结合一个随机符号张量，生成最终的波动尺度 \( \mathbf{Q} \)，作为扩散模型的先验输入。
    *   **尺度感知扩散过程**：修改标准扩散过程，使噪声的终点分布不再是标准高斯 \(\mathcal{N}(0, \mathbf{I})\)，而是以空间异质性先验为中心的分布 \(\mathcal{N}(\mathbf{Q}, \mathbf{I})\)。
        *   **调整后的前向过程**：\( \mathbf{r}^{\text{ta}}_n = \sqrt{\bar{\alpha}_n}\mathbf{r}^{\text{ta}}_0 + (1 - \sqrt{\bar{\alpha}_n})\mathbf{Q} + \sqrt{1 - \bar{\alpha}_n}\boldsymbol{\epsilon} \)
        *   **调整后的反向过程**：均值 \( \boldsymbol{\mu}_\theta \) 的计算公式相应修改，以结合 \( \mathbf{Q} \) 的先验信息。
    *   **训练与推理**：训练采用两阶段流程。推理时，确定性模型输出均值预测，扩散模型估计残差，二者相加得到最终的概率性预测结果。

### 3. 实验设计：使用了哪些数据集/场景，它的benchmark是什么，对比了哪些方法

*   **数据集与场景**：覆盖四大领域的**十个真实世界数据集**，涵盖网格与图结构。
    *   **气候**：SST-CESM2（训练）、SST-ERA5（验证/测试），用于海面温度预测。
    *   **能源**：SolarPower，用于太阳辐照度（GHI）预测。
    *   **通信**：MobileSH（上海）、MobileNJ（南京），用于移动通信流量预测。
    *   **城市**：CrowdBJ、CrowdBM（人流）、TaxiBJ（出租车流量）、BikeDC（共享单车需求）、Los-Speed（交通速度）。
*   **基准方法（Baselines）**：与 6 种先进方法对比，包括：
    *   **D3VAE**：结合VAE和扩散的模型。
    *   **DiffSTG**：用于时空图预测的扩散模型。
    *   **TimeGrad**：自回归扩散模型。
    *   **CSDI**：基于分数的条件扩散模型。
    *   **DYffusion**：动态感知的扩散模型（仅限网格数据）。
    *   **NPDiff**：带噪声先验的扩散模型。
*   **评估指标**：论文引入了一套更全面的评估协议。
    *   **确定性指标**：MAE, RMSE。
    *   **概率性指标**：CRPS, QICE, IS。作者认为传统指标（如CRPS）不足以评估分位数覆盖的准确性和区间宽度的合理性，因此加入QICE和IS。

### 4. 资源与算力：如果文中有提到，请总结使用了多少算力

*   **GPU 资源**：
    *   论文明确指出大部分模型的实验运行在 **NVIDIA TITAN Xp (12GB)** 和 **NVIDIA GeForce RTX 4090 (24GB)** 上。
    *   对于计算资源需求更高的基线模型**DYffusion**，则使用了 **NVIDIA A100 (80GB)** 和 **A800 (40GB)** 进行训练。
*   **训练细节**：
    *   CoST 的训练分为两个阶段，每个阶段最多 **50 个 epoch**。
    *   扩散模型使用 **50 步**扩散步数。
    *   论文在计算成本分析部分提供了具体对比，例如在 MobileSH 数据集上，CoST 的总训练时间仅为 **2分50秒**，而 CSDI 为 48分40秒，DYffusion 长达 33小时，体现了其显著的效率优势。但未提及具体 GPU 数量。

### 5. 实验数量与充分性：大概做了多少组实验

*   **实验类型与数量**：
    *   **主实验（短期预测）**：在 10 个数据集上与 6 个基线模型对比，报告了 5 项指标，结果详实。
    *   **长期预测**：在 5 个数据集上与所有基线对比，验证了框架在长序列预测任务上的有效性。
    *   **泛化性实验**：将 CoST 框架中的确定性骨干网络替换为 4 种不同架构（STID, STNorm, ConvLSTM, iTransformer），并在 3 个数据集上进行测试，充分证明了方法的通用性。
    *   **消融实验**：通过逐步移除“尺度感知扩散过程”（w/o s）、“自定义波动尺度”（w/o q）和“确定性均值预测器”（w/o m）三个关键模块，验证了各组件的贡献。
    *   **定性分析**：包括对预测分布的可视化（KDE图、PIT图）、预测区间校准性分析（PICP曲线）、以及对气候预测的案例研究（SST不确定性空间分布）。
*   **充分性与公平性评估**：实验设计非常充分和客观。实验覆盖了多个领域、多种数据格式（网格、图）、进行了短期/长期预测、对比了多种前沿基线、验证了框架泛化能力，并通过消融实验量化了内部模块的贡献。所有实验均固定随机种子，采用相同的标准化和数据划分方式，确保了对比的公平性。

### 6. 论文的主要结论与发现

*   **性能显著提升**：CoST 在 10 个真实数据集上，在概率性指标（CRPS, QICE, IS）和确定性指标（MAE, RMSE）上，均一致性地优于所有对比的基线模型，平均性能提升达 **25%**。
*   **高效的不确定性量化**：验证了“均值-残差分解”新范式的有效性。通过与强大的确定性模型协同，扩散模型能更精准地捕捉残差中的不确定性，生成更校准的预测区间和更接近真实数据的分布。
*   **计算效率优势**：通过让扩散模型专注于学习简化的残差分布，允许使用更轻量级的去噪网络，显著降低了训练和推理的计算成本，使其更具实际应用价值。
*   **框架的通用性**：CoST 作为一个框架，可以与多种现有的确定性时空预测架构结合，并稳定提升它们的概率预测性能。

### 7. 优点：方法或实验设计上有哪些亮点

*   **新颖的协同范式**：不局限于改进扩散模型本身，而是提出将确定性模型与概率模型优势互补的“均值-残差分解”思想，构思巧妙，逻辑清晰且有理论支撑。
*   **解决实际痛点**：直面扩散模型在时空预测中的高计算成本问题，通过框架设计使其显著降低，极具现实意义。
*   **全面的评估体系**：指出传统评估指标的不足，引入 QICE 和 IS 等更精细的指标，从数据分布匹配和预测可用性两个角度进行更严格的评估，提升了研究的严谨性。
*   **处理空间异质性**：提出的“尺度感知扩散”机制，通过 FFT 提取的空间波动特征作为先验，智能化地建模不同空间位置的不确定性差异，是方法上的一个精细创新。
*   **实验极其扎实**：在10个数据集、多种骨干网络上进行了全面的实验，无论是横向对比、纵向深度、消融实验还是可视化分析都非常充分，结论令人信服。

### 8. 不足与局限：包括实验覆盖、偏差风险、应用限制等

*   **对骨干模型的依赖**：框架的性能上限受限于其所采用的确定性骨干模型。在缺乏成熟确定性预测模型的领域，CoST 的优势可能无法充分发挥。
*   **未在复杂物理系统上验证**：论文明确指出，尚未在如偏微分方程（PDE）描述或耦合动力学系统等更复杂的物理系统中进行验证，其在该类环境下的适用性尚待探讨。
*   **潜在的偏差风险**：实验所使用的 SST-ERA5 和 CESM2 气候数据均经过重新网格化处理，可能会引入或平滑掉一些原始信息，存在一定的预处理偏差。
*   **残差分布假设**：方法假设由确定性模型产生的残差是随机的。如果确定性模型存在系统性偏差，则该偏差会进入残差并由扩散模型学习，可能影响不确定性估计的准确性。论文的理论分析也基于“条件均值预测准确”这一前提。

（完）
