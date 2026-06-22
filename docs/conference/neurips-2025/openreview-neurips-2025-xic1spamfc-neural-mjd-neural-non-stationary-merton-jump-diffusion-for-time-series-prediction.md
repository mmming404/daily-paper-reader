---
title: "Neural MJD: Neural Non-Stationary Merton Jump Diffusion for Time Series Prediction"
title_zh: 神经MJD：用于时间序列预测的神经非平稳默顿跳扩散
authors: "Yuanpei Gao, Qi Yan, Yan Leng, Renjie Liao"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=Xic1sPAmfC"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 神经默顿跳扩散模型用于带跳跃的概率时间序列预测
tldr: 深度学习方法难以显式建模潜在随机过程和突发变化，限制了在非平稳时序上的鲁棒性。本文提出神经MJD，将预测建模为随机微分方程仿真，结合时变伊藤扩散与复合泊松过程，同时捕获非平稳连续动态和跳跃。通过似然截断实现可行学习，实验表明该模型在含突变时间序列概率预测上具有优越表现，提升了可解释性和鲁棒性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-xic1spamfc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1361, \"height\": 407, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xic1spamfc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1434, \"height\": 498, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xic1spamfc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 676, \"height\": 252, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xic1spamfc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1080, \"height\": 647, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xic1spamfc/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1303, \"height\": 587, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-xic1spamfc/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 761, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xic1spamfc/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1438, \"height\": 588, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xic1spamfc/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1429, \"height\": 611, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xic1spamfc/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 816, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xic1spamfc/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 620, \"height\": 214, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xic1spamfc/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 625, \"height\": 208, \"label\": \"Table\"}]"
motivation: 黑箱神经网络难以处理非平稳性和突发跳变，缺乏随机过程解释性。
method: 提出Neural MJD，显式将预测构建为时变扩散与跳跃过程的SDE仿真。
result: 在非平稳和跳跃时间序列上实现了鲁棒且可解释的概率预测。
conclusion: 为时间序列概率预测提供了一种结合物理可解释性和数据驱动灵活性的新框架。
---

## Abstract
While deep learning methods have achieved strong performance in time series prediction, their black-box nature and inability to explicitly model underlying stochastic processes often limit their robustness handling non-stationary data, especially in the presence of abrupt changes. In this work, we introduce Neural MJD, a neural network based non-stationary Merton jump diffusion (MJD) model. Our model explicitly formulates forecasting as a stochastic differential equation (SDE) simulation problem, combining a time-inhomogeneous Itô diffusion to capture non-stationary stochastic dynamics with a time-inhomogeneous compound Poisson process to model abrupt jumps. To enable tractable learning, we introduce a likelihood truncation mechanism that caps the number of jumps within small time intervals and provide a theoretical error bound for this approximation. Additionally, we propose an Euler-Maruyama with restart solver, which achieves a provably lower error bound in estimating expected states and reduced variance compared to the standard solver. Experiments on both synthetic and real-world datasets demonstrate that Neural MJD consistently outperforms state-of-the-art deep learning and statistical learning methods. Our code is available at https://github.com/DSL-Lab/neural-MJD.

---

## 论文详细总结（自动生成）

# 论文总结：Neural MJD —— 用于时间序列预测的神经非平稳默顿跳扩散模型

## 1. 研究动机与核心问题
- **背景与痛点**：真实世界的时间序列（如股价、零售收入）常同时包含连续趋势和因突发事件引起的**跳跃（abrupt jumps）**。传统统计模型（如ARIMA、BS、MJD）虽能显式建模跳跃，但依赖平稳性假设，难以捕捉时变动态；深度学习方法性能强大但多为黑箱，无法显式建模底层随机过程，在非平稳和跳跃数据上鲁棒性差、可解释性弱。
- **核心目标**：将**可解释的随机过程建模**与**数据驱动的深度学习**相结合，构建一个能够同时处理非平稳连续动态与离散跳跃的时序预测框架，提升概率预测的准确性和鲁棒性。

## 2. 方法论
- **整体框架（Neural MJD）**：
  - 将预测问题形式化为**非平稳默顿跳扩散（MJD）过程**的仿真。MJD由**时变伊藤扩散（Itô diffusion）**和**时变复合泊松过程（compound Poisson process）**组成，分别刻画非平稳连续动态和突发跳跃。
  - 使用**神经网络**根据历史序列和上下文信息，直接预测未来每个时间步的SDE参数（漂移μₜ、扩散σₜ、跳强度λₜ、跳均值νₜ、跳方差γₜ），实现“非平稳”建模。
- **可处理的学习目标**：
  - **分段常数近似**：将连续时间离散化，在每个小时间区间内假设参数恒定，避免积分计算。
  - **似然截断**：完整似然函数包含无限个可能跳数的求和，实际计算时**截断跳数上限为κ**。理论证明截断误差以超指数速率（O(κ⁻ᵏ)）收敛，保证了近似精度。
  - **自预测训练**：训练时不使用真实值的教师强制（teacher forcing），而是用模型自身的条件均值预测作为下一步的输入，并加入正则项，缩小训练-推理分布差距。
- **高效推理求解器（Euler-Maruyama with Restart）**：
  - 在标准欧拉-丸山（EM）离散化仿真的基础上，每隔整数时间步（目标预测点）**将状态重置为解析条件均值**。
  - 理论证明该重启策略可获得**更紧的弱收敛误差界**，有效降低均值估计误差和方差，比标准EM更稳定。
- **关键公式与算法概览**：
  - SDE 形式：dSₜ = Sₜ[(μₜ − λₜkₜ)dt + σₜdWₜ + ∫(y-1)N(dt,dy)]
  - 似然函数（截断后）：P(ln Sₜ₊δ|Sₜ) ≈ Σₙ₌₀ᵏ exp(-λδ)(λδ)ⁿ/n! · 𝒩(an, bn²)
  - 训练（Alg1）：逐时间步计算截断似然损失与正则项，并行执行以加速。
  - 推理（Alg2）：细粒度仿真，在整数时刻重启为条件期望 E[S|C]。

## 3. 实验设计
- **数据集**：
  - **合成数据**：由标量MJD生成，含跳跃和突变，10,000条路径，每条100步，滑窗预测（用前10帧预测后10帧）。
  - **SafeGraph&Advan商业分析数据**：包含德州POI的每日消费金额及空间图结构，滑窗（14天历史→7天未来），训练/验证/测试按时间切分。
  - **S&P 500股票数据**：500只美股每日价格，构造完全连通图，同样采用滑窗（14→7）预测。
- **对比方法**：
  - 统计模型：ARIMA、BS、MJD。
  - 监督学习：XGBoost、MLP、GCN。
  - 神经微分方程：NeuralCDE、LatentSDE、NJ-ODE（仅S&P 500）。
  - 生成模型：DDPM、EDM、Flow Matching (FM)。
  - 消融模型：Neural BS（无跳跃部件）。
- **评估指标**：MAE、MSE、R²，并细分为**均值指标**、**胜者全拿（Winner-takes-all）指标**（10次采样取最优）、**概率指标**（选最可能结果），全面衡量确定性和概率预测能力。

## 4. 资源与算力
- 论文提到所有实验在 **NVIDIA A40（48 GB）** 和 **A100（80 GB）** GPU上运行，但**未明确说明使用的GPU数量及具体训练时长**（仅给出了单个序列的训练/推理耗时对比，如表5）。

## 5. 实验数量与充分性
- **实验丰富度较高**：覆盖3个不同类型数据集（合成、商业、金融），每个数据集约与10+种基线对比，且包含**消融研究**（教师强制 vs 自预测训练、标准EM vs 重启EM）及**运行效率对比**，评估维度多样。
- **公平性与客观性**：对生成模型和本模型使用相同Transformer主干网络；统计模型通过标准MLE估计参数；所有方法均按相同的数据划分和预处理。实验设计系统，对比相对公平。

## 6. 主要结论与发现
- Neural MJD在所有数据集及几乎所有评估指标上均**一致优于**各类深度学习和统计基线，特别是在“胜者全拿”指标上优势明显，表明其能生成更准确且多样化的预测轨迹。
- 跳跃建模的引入（与Neural BS对比）显著提升了对突变数据的拟合能力。
- 自预测训练和重启EM求解器有效提升了训练稳定性和推理精度，可在不增加神经网络前传次数的情况下实现多步随机仿真。

## 7. 优点与亮点
- **物理可解释性与数据驱动灵活性的结合**：显式建模非平稳扩散和跳跃过程，参数由数据驱动学习。
- **坚实的理论支撑**：提供了似然截断误差的收敛性分析、重启EM方法的弱收敛误差界，增强了方法的可信度。
- **高效的概率预测**：推理时仅需一次神经网络前向传播即可获得全时域SDE参数，后续仿真在CPU上轻量完成，支持快速多采样。
- **鲁棒的不确定性量化**：通过重启机制和显式分布假设，在复杂跳跃场景下仍能保持低误差和低方差。

## 8. 不足与局限
- **跳跃缺失场景的潜在不适**：若数据极度平滑无跳跃，跳跃部件可能被错误估计或成为冗余，模型性能可能下降。
- **截断超参依赖**：似然截断数κ固定为5，虽理论保证误差衰减快，但极端跳跃频率下需进一步验证。
- **图建模简单**：对于S&P 500数据，仅使用全连接图，未利用行业等真实关联信息，可能影响空间依赖的刻画。
- **实验覆盖领域有限**：集中在金融和商业数据，未在需跳跃建模的其它领域（如气候事件、网络流量突变等）验证。
- **训练资源信息不全**：未提供具体的GPU使用数量和总训练时间，不利于精确复现。

（完）
