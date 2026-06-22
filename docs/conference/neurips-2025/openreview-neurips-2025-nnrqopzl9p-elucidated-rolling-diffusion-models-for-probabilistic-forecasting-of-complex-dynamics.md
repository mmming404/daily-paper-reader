---
title: Elucidated Rolling Diffusion Models for Probabilistic Forecasting of Complex Dynamics
title_zh: 阐明滚动扩散模型用于复杂动力学的概率预测
authors: "Salva Rühling Cachay, Miika Aittala, Karsten Kreis, Noah D Brenowitz, Arash Vahdat, Morteza Mardani, Rose Yu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=NnRQOPzL9P"
tags: ["query:ts-forecast"]
score: 10.0
evidence: 阐明滚动扩散模型用于概率预测，显式建模不确定性增长
tldr: 现有扩散模型在复杂系统概率预测中通常逐点预测，难以建模时序依赖和不确定性增长。本文提出阐明滚动扩散模型（ERDM），首次将滚动预测结构与先进的扩散技术统一，通过随时间增加噪声来显式处理不确定性。实验表明，ERDM在高维复杂动力学预测中显著优于现有方法，为概率预测提供了更精确的框架。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1439, \"height\": 702, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 608, \"height\": 405, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 500, \"height\": 720, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1402, \"height\": 517, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1435, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 580, \"height\": 758, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1440, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1431, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 623, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1459, \"height\": 752, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1446, \"height\": 1160, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1431, \"height\": 867, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1437, \"height\": 898, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1439, \"height\": 1582, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1444, \"height\": 1883, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nnrqopzl9p/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1450, \"height\": 1885, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-nnrqopzl9p/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1443, \"height\": 353, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nnrqopzl9p/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1096, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nnrqopzl9p/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1496, \"height\": 1665, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nnrqopzl9p/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1014, \"height\": 317, \"label\": \"Table\"}]"
motivation: 现有扩散预测忽略时序依赖和不确定性逐渐增长的内在特性。
method: 提出ERDM，将滚动扩散框架与高性能扩散技术结合，按时间递增加噪。
result: 在复杂动力学概率预测任务上显著优于现有方法，捕捉了不确定性演化。
conclusion: ERDM为复杂系统不确定性量化提供了强大新工具。
---

## Abstract
Diffusion models are a powerful tool for probabilistic forecasting, yet most applications in high-dimensional complex systems predict future states individually. This approach struggles to model complex temporal dependencies and fails to explicitly account for the progressive growth of uncertainty inherent to the systems. While rolling diffusion frameworks, which apply increasing noise to forecasts at longer lead times, have been proposed to address this, their integration with state-of-the-art, high-fidelity diffusion techniques remains a significant challenge. We tackle this problem by introducing Elucidated Rolling Diffusion Models (ERDM), the first framework to successfully unify a rolling forecast structure with the principled, performant design of Elucidated Diffusion Models (EDM). 
To do this, we adapt the core EDM components--its noise schedule, network preconditioning, and Heun sampler--to the rolling forecast setting. The success of this integration is driven by three key contributions: $(i)$ a novel loss weighting scheme that focuses model capacity on the mid-range forecast horizons where determinism gives way to stochasticity; $(ii)$ an efficient initialization strategy using a pre-trained EDM for the initial window; and $(iii)$ a bespoke hybrid sequence architecture for robust spatiotemporal feature extraction under progressive denoising. 
On 2D Navier–Stokes simulations and ERA5 global weather forecasting at $1.5^\circ$ resolution, ERDM consistently outperforms key diffusion-based baselines, including conditional autoregressive EDM.
ERDM offers a flexible and powerful general framework for tackling diffusion-based dynamics forecasting problems where modeling  uncertainty propagation is paramount.

---

## 论文详细总结（自动生成）

好的，以下是对该论文的结构化、深入、客观的总结。

### 1. 论文的核心问题与整体含义

本论文聚焦于复杂动力系统（如天气、流体力学）的概率预测。其核心问题是，当前主流的基于扩散模型的预测方法存在两个关键局限：

*   **忽略时序依赖性**：多数方法将未来每个时间点的状态视为独立预测，未能有效建模系统内在复杂的时序演变关系。
*   **未能显式建模不确定性增长**：混沌系统的一个固有特征是其预测不确定性随时间推移而逐渐增大，现有方法无法在模型中显式地体现这一物理规律。

因此，该研究的核心动机是设计一个扩散模型框架，能够**在生成长期预测序列时，显式地模拟随时间增长的不确定性，并更好地捕捉长程时序依赖**。

### 2. 论文提出的方法论

论文提出了**阐明滚动扩散模型（ERDM）**，其核心思想是将高性能的**阐明扩散模型（EDM）框架**与**滚动预测**机制相结合。关键技术细节如下：

*   **滚动噪声调度**：框架的核心是定义一个随预测步长递增的噪声标准差序列。对一个窗口大小为 $W$ 的序列，其噪声标准差满足 $\bar{\sigma}_1(t) < \bar{\sigma}_2(t) < \dots < \bar{\sigma}_W(t)$，其中 $t$ 是扩散时间。这直观地体现了“越远的未来越不确定”的先验。公式定义为：
    $\bar{\sigma}_w(t) = \left( \sigma_{max}^{1/\rho} + t_{w,t} (\sigma_{min}^{1/\rho} - \sigma_{max}^{1/\rho}) \right)^\rho$，其中 $t_{w,t}=1-\frac{w-t}{W}$，并通过调整曲率参数 $\rho$（默认 $\rho=-10$）来优化噪声分布。
*   **预条件处理与损失加权**：将 EDM 的预条件处理函数（$c_{skip}, c_{out}, c_{in}, c_{noise}$）向量化，独立应用于序列中的每一个快照。提出了一个**不确定性感知的损失重加权方案**，结合 EDM 的单位方差损失和基于对数正态分布的概率密度函数 $f(\sigma; P_{mean}, P_{std})$，将模型训练的重点放在噪声水平适中的“中间地带”，这里正是确定性走向随机性的关键区域。
*   **高效的初始化与采样策略**：
    *   **初始化**：利用一个预训练好的单步 EDM 模型生成第一个窗口的预测 $\hat{y}_{1:W}$，再加入匹配噪声水平的噪声，从而避免了从头开始训练初始化的复杂性。
    *   **采样**：基于设计好的噪声调度，运行一个特殊的概率流 ODE。当 ODE 积分完成时（$t=1$），窗口中的第一个快照被完全去噪（$\bar{\sigma}_1(1)=\sigma_{min}$）并输出作为预测结果。然后，窗口向前滑动一格，将一个纯噪声快照追加到末尾，循环往复，生成无限长的预测序列。采样器可选一阶欧拉法或二阶Heun法，并支持可控的随机性。
*   **混合时空架构**：设计了一个专用的 3D 去噪网络，将擅长空间特征提取的 2D U-Net 模块与擅长时序依赖建模的因果时序注意力模块交错布置，使模型能联合提取时空特征。

### 3. 实验设计

论文在两个截然不同的复杂动力学系统上进行了验证：

*   **数据集**：
    1.  **Navier-Stokes 流体仿真**：一个标准的湍流仿真数据集（$221 \times 42$ 网格），包含障碍物，要求模型根据初始状态预测未来 64 步。主要评估指标是**连续分级概率评分（CRPS）**和**离散度-技巧比（SSR，衡量校准度）**。
    2.  **ERA5 全球天气预报**：使用 $1.5^\circ$ 分辨率的再分析数据（$240 \times 121$ 网格），包含 69 个高空和地表变量。任务是根据初始条件进行长达 15 天的集合预报。
*   **对比基准**：实验对比了多种基线方法，包括：
    *   主流的条件自回归 **EDM**（单步/多步预测）。
    *   同类滚动扩散模型 **DYffusion** 和 **PDE-Refiner**。
    *   业界领先的物理模型 **IFS ENS**（ECMWF 业务集合预报系统）。
    *   物理-ML 混合模型 **NeuralGCM ENS**。
    *   其他先进概率预测模型 **Graph-EFM**。

### 4. 资源与算力

论文明确报告了训练和推理所需的算力资源：

*   **ERA5 模型训练**：最终的 ERDM 模型在 **4 块 NVIDIA H200 GPU** 上训练了约 **5 天**。这与竞品模型形成鲜明对比，例如 NeuralGCM ENS 需要 128 块 TPU v5 训练 10 天，凸显了其计算效率。
*   **Navier-Stokes 模型训练**：训练在 **2-8 块 L40S 或 A100 GPU** 上完成。
*   **推理效率**：尽管 ERDM 的 3D 架构单步计算更贵，但得益于其滚动窗口机制，生成完整 15 天预报所需的神经网络前传次数 (NFEs) 比自回归 EDM 少 5 倍，总推理时间与 EDM 相当或稍快。

### 5. 实验数量与充分性

实验设计相当充分和系统：

*   **多场景验证**：实验覆盖了流体力学和全球天气预报两个完全不同的高维复杂系统，证明了方法的普适性。
*   **多指标评估**：不仅关注预测技巧（CRPS、MSE），还深入评估了集合预报的校准度（SSR）和物理逼真度（功率谱），评估非常全面。
*   **广泛的对比基线**：对比了从纯粹 ML 方法到业务级物理模型的多种 SOTA 方法，基线选择强且有代表性。
*   **详尽的消融研究**：对关键设计选择进行了细致的消融实验（参见原文 Table 2），验证了噪声调度、损失加权策略、时空架构、采样器和初始化策略等每个组件的必要性和最优配置，结果极具说服力。
*   **公平性考虑**：对模型（如 DYffusion）进行了重新训练以确保公平比较，并探讨了评估年份对结果的影响。

### 6. 论文的主要结论与发现

论文的主要结论是，ERDM 在长期概率预测上显著优于现有扩散模型基线：

*   在 Navier-Stokes 任务中，ERDM 的长程预测 CRPS 比最佳基线（多步 EDM）**提升约 50%**。
*   在 ERA5 天气预报中，ERDM 的 CRPS 指标一致优于单步自回归 EDM 基线，**提升可达 10%**，并在中长期预报上展现出与 IFS ENS 等业务模型竞争的性能。
*   ERDM 生成预报的功率谱能量分布与真实分析场高度一致，甚至优于 IFS ENS，证明其具有**极高的物理逼真度**。
*   在集合预报校准度方面，ERDM 表现优异，优于易出现欠离散的 EDM 和 NeuralGCM 基线。

### 7. 优点

*   **理论优雅性**：成功将 EDM 的优良设计（预条件、损失权重、高阶采样器）系统性地移植到滚动扩散框架中，解决了该方向的一个关键难题。
*   **问题导向的设计**：滚动噪声调度和损失重加权策略直接针对“不确定性随时间增长”这一物理直觉，模型设计动机清晰。
*   **计算效率**：相比其性能所对标的业务模型（IFS ENS， NeuralGCM ENS），所需的训练算力显著降低（仅需 4 块 H200 GPU）。
*   **评估全面**：综合了技巧评分、校准度、物理一致性和计算成本，提供了多维度评价视角。
*   **模块化架构**：混合 U-Net 与时序注意力的设计，为扩散模型处理时空数据提供了一个有效的范式。

### 8. 不足与局限

*   **推理内存开销大**：时空混合架构模型参数量大，推理时需要约 49GB GPU 显存，是 2D EDM 的两倍多，对扩展到更高分辨率数据构成限制。
*   **短期预报未达最优**：在 ERA5 任务中，ERDM 在短预报时效（如 3 天内）的性能尚不如 IFS ENS，作者将此归因于初始化策略和 U-Net 架构在天气建模领域尚未完全特化。
*   **依赖外部初始化**：模型需要依赖一个预训练的外部预测器（如单步 EDM）来开始滚动过程，并非完全自包含。
*   **损失权重的超参数敏感**：虽然文中给出了默认值，但损失重加权方案中的 $P_{mean}$ 等参数对性能有显著影响，需针对特定任务进行调优。

（完）
