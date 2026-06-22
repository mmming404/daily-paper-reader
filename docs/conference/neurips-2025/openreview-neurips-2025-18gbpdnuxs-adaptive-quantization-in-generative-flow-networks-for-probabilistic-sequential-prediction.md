---
title: Adaptive Quantization in Generative Flow Networks for Probabilistic Sequential Prediction
title_zh: 生成流网络中的自适应量化用于概率序列预测
authors: "Nadhir Hassen, Zhen Zhang, Johan W. Verjans"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=18GBPdnuXs"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 引入时间生成流网络实现校准的概率时间序列预测
tldr: 针对连续值时间序列概率预测中校准分布难以生成的问题，本文提出时间生成流网络（Temporal GFNs），通过自适应量化将生成流网络适配于顺序预测任务，逐步构建预测轨迹。实验证明该方法能产生校准良好的概率预测，为医疗、神经科学等领域的决策提供可靠的不确定性估计。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1352, \"height\": 648, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1438, \"height\": 881, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1440, \"height\": 720, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1448, \"height\": 1224, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1305, \"height\": 928, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1365, \"height\": 651, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 869, \"height\": 617, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1004, \"height\": 767, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1000, \"height\": 655, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1443, \"height\": 541, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1282, \"height\": 889, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1000, \"height\": 750, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1004, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1163, \"height\": 767, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1009, \"height\": 674, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1008, \"height\": 672, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1441, \"height\": 497, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 993, \"height\": 981, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1157, \"height\": 1155, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1412, \"height\": 942, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1435, \"height\": 733, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 955, \"height\": 901, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1441, \"height\": 917, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-18gbpdnuxs/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1288, \"height\": 986, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-18gbpdnuxs/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1449, \"height\": 262, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-18gbpdnuxs/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1454, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-18gbpdnuxs/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1479, \"height\": 333, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-18gbpdnuxs/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1699, \"height\": 2293, \"label\": \"Table\"}]"
motivation: 现有深度模型在生成未来连续值的校准概率分布方面仍有挑战。
method: 提出时间生成流网络（Temporal GFNs），结合自适应量化策略逐步生成预测轨迹。
result: 方法在校准度和不确定性量化方面优于基线。
conclusion: Temporal GFNs为概率时间序列预测提供了新的生成式方案。
---

## Abstract
Probabilistic time series forecasting, essential in domains like healthcare and neuroscience, requires models capable of capturing uncertainty and intricate temporal dependencies. While deep learning has advanced forecasting, generating calibrated probability distributions over continuous future values remains challenging. We introduce Temporal Generative Flow Networks (Temporal GFNs), adapting Generative Flow Networks (GFNs) – a powerful framework for generating compositional objects – to this sequential prediction task. GFNs learn policies to construct objects (eg. forecast trajectories) step-by-step, sampling final objects proportionally to a reward signal. However, applying GFNs directly to continuous time series necessitates addressing their inherently discrete action spaces and ensuring differentiability. Our framework tackles this by representing time series segments as states and sequentially generating future values via quantized actions chosen by a forward policy. We introduce two key innovations: (1) An adaptive, curriculum-based quantization strategy that dynamically adjusts the number of discretization bins based on reward improvement and policy entropy, balancing precision and exploration throughout training. (2) A straight-through estimator mechanism enabling the forward policy to output both discrete (hard) samples for trajectory construction and continuous (soft) samples for stable gradient propagation. Training utilizes a trajectory balance loss objective, ensuring flow consistency, augmented by an entropy regularizer. We provide rigorous theoretical bounds on the quantization error's impact and the adaptive factor's range. We demonstrate how Temporal GFNs offer a principled way to leverage the structured generation capabilities of GFNs for probabilistic forecasting in continuous domains.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
*   **研究背景与动机**：概率性时间序列预测（Probabilistic Time Series Forecasting）在医疗、神经科学等领域至关重要，因为它能提供预测值的不确定性（如预测区间或密度估计），用于风险评估。现有深度学习方法（如RNN、Transformer）要么对预测分布做限制性假设（如高斯分布），要么存在分位数交叉等问题。大型语言模型（LLM）虽然通过固定量化（discretization）将时间序列视为离散词元取得了成功，但量化方案往往是事先静态决定的。
*   **核心问题**：如何将生成流网络（GFlowNet，简称 GFN）这一擅长在离散动作空间中通过奖励驱动采样、生成组合对象的框架，适配到“连续值时间序列”的概率预测任务中？
*   **整体含义**：本文提出了一套新框架，将时间序列预测重构为在 GFN 状态空间中逐步构建预测轨迹的过程，旨在采样出与奖励（预测精度）成比例的高质量、多样化预测，从而提供更校准、更灵活的概率预测。

### 2. 论文提出的方法论
核心思想是将预测任务建模为**时间生成流网络（Temporal GFNs）** 的轨迹生成。具体技术细节如下：

*   **状态与动作定义**：
    *   **状态 (s)**：固定长度的滑动窗口，包含历史上下文和已生成的预测值。
    *   **动作 (a)**：从状态中通过“前向策略”选择一个离散的量化值，代表下一时间步的预测。这解决了传统 GFN 需要离散动作空间的问题。

*   **关键技术 1：自适应课程式量化**
    *   **动机**：固定量化分箱数 K 存在两难——K 太小精度低，K 太大导致动作空间稀疏、探索困难。
    *   **机制**：根据奖励提升幅度（\(\Delta R_e\)）和政策熵（\(H_e\)）动态调整 K。
    *   **公式**：更新因子 \(\eta_e = 1 + \lambda \left( \frac{\max(0, \epsilon - \Delta R_e)}{\epsilon} + (1 - H_e) \right)\)。
    *   **效果**：训练初期 K 较小（粗粒度），随着奖励停滞或熵降低，K 自适应增大（细粒度），实现从易到难的课程学习。当 K 增加时，通过保留旧权重、为新增加的 bin 初始化为近零值，防止灾难性遗忘。

*   **关键技术 2：直通估计器（STE）确保可微性**
    *   **问题**：从策略中采样离散动作的动作（argmax 或采样）导致梯度无法回传。
    *   **解决方案**：
        *   **前向传播**：使用硬采样（\(a_t^{hard}\)）进行状态转移，构建轨迹。
        *   **反向传播**：使用软采样（\(a_t^{soft} = \sum_k q_k P_F(a_t=q_k|s_t)\)）计算梯度，并将其“直通”给产生离散动作的参数，实现端到端训练。

*   **训练目标与网络**
    *   **策略网络**：使用 Transformer 编码器作为主干，输出 K 个 bin 上的分类分布。
    *   **损失函数**：采用轨迹平衡损失（Trajectory Balance, \(L_{TB}\)）保证流一致性。同时引入熵正则项（\(-\lambda_{entropy} H(P_F)\)）鼓励探索，防止策略过早陷入确定性。
    *   **奖励函数**：基于预测序列与真实未来序列的负归一化均方误差（MSE）的指数函数 \(R(\tau) = \exp(-\beta \cdot MSE)\)。
    *   **理论保证**：论文提供了量化误差对策略梯度影响的边界，以及自适应更新因子的范围（\(1 \le \eta_e \le 1+2\lambda\)），证明了算法的稳定性和可控性。

### 3. 实验设计
*   **数据集**：
    *   **大规模异构数据集**：覆盖能源、金融、交通、网络、医疗等多个领域的公开数据。
    *   **数据分割**：划分为“预训练集”、“域内评估集（Benchmark I）”和“零样本评估集（Benchmark II）”，评估域内预测及泛化能力。
*   **评估指标**：CRPS（连续分级概率评分）、WQL（加权分位数损失）、MASE（平均绝对标度误差），以及校准误差和多模态评分。
*   **对比方法**：
    *   **强化学习/MCMC基线**：PPO、SAC、MCMC。
    *   **最先进时间序列预测模型（SOTA）**：Lag-Llama、Chronos、MOREI、TimeFM。
*   **消融实验**：对比了固定 K 量化、自适应量化、学习型后向策略等配置，全面验证各组件贡献。

### 4. 资源与算力
*   文中提到在“多 GPU 硬件”上进行训练，典型训练步数为 10,000 步，但未明确说明具体的 GPU 型号、数量或总训练时长。

### 5. 实验数量与充分性
*   **实验数量**：非常充分。论文不仅进行了与 RL/MCMC、SOTA 预测模型的全面性能对比，设计了丰富的消融实验（固定与自适应 K、有无 STE、有无熵正则、后向策略选择），还从可视化（梯度流、量化误差、奖励与熵动态）、理论验证和计算资源开销等多个角度进行了深入分析。
*   **客观与公平性**：实验评估流程严谨，对模型进行了多随机种子下的指标平均，尽量确保了公平性和可复现性。

### 6. 论文的主要结论与发现
*   **框架有效性**：Temporal GFNs 成功地将 GFN 范式适配到连续时序预测，能够生成校准良好、多样化的预测。
*   **性能优越**：在域内和零样本设定下，Temporal GFNs 在 CRPS、WQL 等概率性指标上表现极具竞争力，显著优于 RL/MCMC 方法，在捕捉数据分布的多模态性（Multimodality）上相比 SOTA 模型（如 Chronos）有显著优势。
*   **机制验证**：自适应量化机制通过动态平衡精度与探索，提供了比固定量化更优的性能。STE 是保证模型有效学习的必要组件，而熵正则化对维持探索和防止模式坍塌至关重要。

### 7. 优点
*   **新颖的建模视角**：首次将 GFN 用于时间序列预测，为概率预测提供了基于奖励驱动采样的新范式。
*   **精巧的技术方案**：自适应量化机制解决了离散与连续的矛盾，提供了一种内在的课程学习方案；STE 的使用巧妙地处理了离散动作的不可微问题。
*   **坚实的理论支撑**：为关键机制提供了误差边界和稳定性证明，增强了方法的可信度。
*   **出色的分布建模能力**：方法在捕获复杂、多模态的预测分布方面表现出显著优势，校准性能好，优于许多主流方法。

### 8. 不足与局限
*   **计算开销**：相比单步生成预测的 Transformer 或 LLM，Temporal GFN 逐步生成轨迹的特性在训练时计算量更大。
*   **奖励设计依赖**：性能对奖励函数 \(R(\tau)\) 的设计敏感。虽然指数 MSE 有效，但在需要复杂目标（如惩罚不合理的生理轨迹）的领域，设计合适奖励可能是个挑战。
*   **应用限制**：
    *   **单变量**：当前验证仅限于单变量预测，扩展到多变量的主要挑战在于如何高效地对多变量动作空间进行联合分布建模。
    *   **规则采样**：当前框架基于固定大小的滑动窗口，假设了数据的规则采样，尚未适配医疗（EHR）等场景中常见的非规则采样数据。

（完）
