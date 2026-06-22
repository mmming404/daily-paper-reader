---
title: Conformal Prediction for Time-series Forecasting with Change Points
title_zh: 面向变化点的时间序列预测的共形预测
authors: "Sophia Huiwen Sun, Rose Yu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=HgLaVgCpCl"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 面向变化点时间序列的共形预测以提供不确定性量化
tldr: 针对传统共形预测难以处理非平稳时间序列中变化点的问题，本文提出CPTC算法，将潜在状态预测模型与在线共形预测集成，在最小假设下证明有效性和自适应性。在6个合成和真实数据集上，CPTC均提供更准确的自适应预测区间，对存在突变的流式数据具有实用意义，丰富了时间序列不确定性量化工具箱。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-hglavgcpcl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 405, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hglavgcpcl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1372, \"height\": 367, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hglavgcpcl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1427, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hglavgcpcl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 830, \"height\": 270, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hglavgcpcl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1229, \"height\": 1415, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hglavgcpcl/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1448, \"height\": 749, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hglavgcpcl/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1450, \"height\": 749, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-hglavgcpcl/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1447, \"height\": 748, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-hglavgcpcl/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1409, \"height\": 872, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hglavgcpcl/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1449, \"height\": 512, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hglavgcpcl/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 847, \"height\": 165, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hglavgcpcl/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 561, \"height\": 160, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hglavgcpcl/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1164, \"height\": 577, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hglavgcpcl/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1449, \"height\": 599, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hglavgcpcl/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1355, \"height\": 272, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-hglavgcpcl/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1285, \"height\": 189, \"label\": \"Table\"}]"
motivation: 现有共形预测无法很好适应时间序列中的突变点。
method: 提出CPTC，结合状态预测与在线共形预测处理变化点。
result: 在6个数据集上实现更优的有效性和自适应性。
conclusion: CPTC为非平稳时间序列提供了可靠的不确定性量化方法。
---

## Abstract
Conformal prediction has been explored as a general and efficient way to provide uncertainty quantification for time series. However, current methods struggle to handle time series data with change points — sudden shifts in the underlying data-generating process. In this paper, we propose a novel Conformal Prediction for Time-series with Change points (CPTC) algorithm, addressing this gap by integrating a model to predict the underlying state with online conformal prediction to model uncertainties in non-stationary time series. We prove CPTC's validity and improved adaptivity in the time series setting under minimum assumptions, and demonstrate CPTC's practical effectiveness on 6 synthetic and real-world datasets, showing improved validity and adaptivity compared to state-of-the-art baselines.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：共形预测（Conformal Prediction）作为一种为机器学习模型提供的不确定性量化方法，具有分布无关、有限样本覆盖保障等优势。然而，现有面向时间序列的在线共形预测方法（如ACI）在面对数据生成过程的**突变点**（change points）时，往往只能“反应式”地调整预测区间，导致突变时刻的覆盖不足，随后又因补偿而过度覆盖。
- **核心问题**：如何利用突变点可被预测的特性，设计一种能够主动适应分布突变的在线共形预测算法，使得预测区间在变化的动力学模式下依然保持有效且尖锐。
- **整体含义**：作者提出了一种面向“具有突变点的时间序列”的**共形预测算法CPTC**，通过融入切换动态系统（SDS）的**潜在状态预测**能力，将共形校准按状态分离，从而实现更快、更稳定的自适应不确定性量化，并在理论上证明了其有效性及对状态分类误差的鲁棒性。

## 2. 方法论：CPTC算法的核心思想与技术细节

- **核心思想**：将时间序列的不同动力学模式抽象为离散的潜在状态（开关状态），利用**切换动态系统**（如RED‑SDS）预测每个时刻的状态分布，针对每个状态独立维护一条在线共形推理链路，最后按预测概率聚合各状态的预测区间。
- **关键技术细节**：
    - **问题形式化**：在线流式场景下，给定序列 \((x_t, y_t)\)，要求在每一个时间步生成满足 \(P(y_t \in \Gamma_t(x_t)) \ge 1-\alpha\) 的预测区间。
    - **状态预测模块**：从一个已训练的 SDS 模型（或任何能输出状态概率的模型）中获得 \(\hat{p}(z_t | x_{0:t})\)，其中 \(z_t \in \{1,\dots,K\}\)。
    - **状态特定的共形校准**：
        - 为每个状态 \(z\) 维护一个非一致性分数集合 \(S_z\) 和一个自适应置信水平 \(\alpha_{z,t}\)。
        - 每个状态的预测区间为 \(\Gamma_{z,t}(x_t) = \{y : A(x_t, y) \le Q_{1-\alpha_{z,t}}(S_z \cup \{\infty\})\}\)。
    - **在线自适应调节**：采用 ACI 的在线更新策略 \(\alpha_{\hat{z}_t, t+1} \leftarrow \alpha_{\hat{z}_t, t} + \gamma \cdot (\alpha - \text{err}_t)\)，其中 \(\hat{z}_t\) 为采样的预测状态，\(\text{err}_t = \boldsymbol{1}_{\{y_t \notin \Gamma_t(x_t)\}}\)。
    - **区间聚合**：最终预测区间为各状态区间的加权水平集（理论形式），或实际使用的高效近似——取能使累积概率达到 \(1-\alpha\) 的最可能状态的区间的并集。
- **理论保证**：
    - **有限样本有效性**：在可交换数据下，满足 \(P(y_t \in \Gamma_t) \ge 1-\alpha\)。
    - **渐近有效性**：在非平稳环境下，全局误覆盖率收敛到目标水平 \(\alpha\)，速度为 \(O(1/T)\)，且对数据生成过程无假设。
    - **状态预测鲁棒性**：当状态预测错误率为 \(\epsilon\) 时，误覆盖率偏差被 \(\epsilon \cdot \max_z \delta_{z,T}\) 限制，其中 \(\delta_{z,T} \to 0\)。
    - **自适应加速**：当分布突变恰好与预测的状态转变一致时，CPTC 的收敛速度优于仅靠全局在线更新的方法。

## 3. 实验设计

- **数据集**：
    - **3个合成数据集**：
        - Bouncing Ball (观测噪声) —— 模拟恒定速度弹性碰撞，两种状态（上/下），不同状态加入不同水平的高斯观测噪声。
        - Bouncing Ball (动力学噪声) —— 噪声施加于动力学过程，导致相位不确定性。
        - 3‑mode switching system —— 3个离散状态的切换线性动力系统，状态持续时长从泊松分布采样。
    - **3个真实数据集**：
        - Electricity —— 370个客户的每小时电力消耗（UCI）。
        - Traffic —— 963个传感器的每小时道路占有率。
        - Dancing Bees —— 蜜蜂舞蹈轨迹（4维），包含“左转”“右转”“摇摆”三种行为模式。
- **评价指标**：
    - **有效性（校准度）**：经验覆盖率 \(\text{Coverage} = \frac{1}{T}\sum \boldsymbol{1}_{(y_t \in \Gamma_t)}\)，应尽量接近设定置信水平 \(1-\alpha\)（实验中设为0.9）。
    - **尖锐性**：平均预测区间宽度 \(\text{Width} = \frac{1}{T}\sum |\Gamma_t|\)，有效前提下越小越好。
- **基准方法**：
    - RED‑SDS：概率状态空间模型，直接输出预测分位数。
    - CP：在线分割共形预测（Online Sequential Split Conformal）。
    - ACI：自适应共形推理。
    - SPCI：利用分位数随机森林学习残差的自相关的顺序共形方法。
    - HopCPT：基于现代Hopfield网络的相似性条件共形预测。
    - 后续补充对比 DtACI、ECI、L‑ARC 等反应式方法。
- **实验设置**：主要实验中时序长度较短（合成200步，电力/交通300步，蜜蜂60步），以突出CPTC在数据有限时的优势；同时还给出了长时序（合成10k步，电力/交通4k步）的结果，讨论不同场景下的行为。

## 4. 资源与算力

- **硬件**：实验在配备**Nvidia A100 GPU** 的服务器上完成，部分数据处理在 Apple M1 笔记本电脑上进行。
- **训练开销**：
    - RED‑SDS 基础模型的单种子训练耗时约 **2–5 小时**。
    - 推理阶段：RED‑SDS 约需 15–20 分钟。
- **共形预测推理开销**：
    - SPCI 推理最耗时，约 8–10 小时（因需在线重新训练分位数回归模型）。
    - HopCPT 约需 1 小时。
    - CP、ACI、CPTC 等无需在线重训的方法，均可在 **5分钟内**完成所有推理。
- **本文未提供**更大规模分布式训练或具体 GPU 显存消耗的详细数据，但已有描述足以评估其计算实用性。

## 5. 实验数量与充分性

- **实验组数**：
    - 主表（Table 1 和 Table 4）覆盖 **6 个数据集**，每个数据集报告覆盖率和宽度，目标置信度为 0.9，所有结果均带有均值±标准差（基于多次测试样本）。
    - 增加了 DtACI、ECI、L‑ARC 的补充对比实验（Table 4）。
    - **长时序实验**（Table 5）：6 个场景（含变噪声的弹球）测试 T=10,000 或 4,000 时的表现。
    - **消融研究**：
        - 状态预测准确度对覆盖率与宽度的影响（Table 2, 3），模拟了 20% 和 50% 的标签噪声。
        - 聚合方法对比（Table 6）：理论加权水平集（grid-discretization）与近似并集的性能基本一致。
    - **定性可视化**：展示不同数据集上的预测区间随状态变化的自适应行为。
- **充分性与公平性**：
    - 数据集覆盖合成非线性动力系统、真实周期性能源、交通数据以及行为轨迹，维度从单变量到多变量，状态数从2到3，噪声来源多样，具有一定代表性。
    - 对比方法包含了纯粹的在线共形、学习残差结构的专门方法以及概率模型，较为全面。
    - 各实验均采用标准划分（70/10/20训练/验证/测试），错误栏和随机种子信息完善，保证了可重复性和统计稳健性。
    - 短时与长时性能的对比分析进一步说明了方法的适用范围，实验设计较为充分、客观。

## 6. 主要结论与发现

- **有效性显著提升**：在所有6个数据集（特别在短时序场景）上，CPTC 的覆盖率非常接近目标水平0.9，明显优于 RED‑SDS、CP、SPCI、HopCPT 等基线，尤其在突变点附近不易出现严重欠覆盖或过度补偿。
- **自适应能力强**：CPTC 能依据预测的状态主动扩大/缩小预测区间，白天/夜晚、工作日/周末等模式切换时区间宽度自适应变化，同时保持覆盖率平稳。
- **鲁棒性**：即使状态预测存在20%甚至50%的标签噪声，覆盖率变化极小，仅宽度略有增加，验证了理论中对错误分类的鲁棒性。
- **计算高效**：CPTC 无需在线重训练模型，推理时间与 ACI 相当，远低于需在线学习的 SPCI 和 HopCPT。
- **适用范围**：在状态可被离散建模且训练数据有限、要求快速部署的不确定性量化任务中，CPTC 具有独特的优势。

## 7. 优点

- **主动自适应机制**：将状态预测与共形预测深度融合，使预测区间能够“预判”突变，解决了纯反应式方法在突变点处的固有问题。
- **理论严谨**：在不设定数据生成分布的弱假设下，证明了渐近有效性和对状态分类误差的鲁棒性，给出了有限样本下的误覆盖率界。
- **模块化设计**：状态预测器、预测模型和在线共形程序彼此解耦，易于替换或升级其中任意组件。
- **计算轻量**：在线阶段仅需维护几个小规模分数集和比例更新，无需重新训练，适合实时应用。
- **实验充分**：在合成及多种真实场景下与众多先进方法对比，并通过消融实验验证关键模块的影响。

## 8. 不足与局限

- **离散状态假设**：方法依赖于预定义的离散状态，对于状态数未知或状态连续变化的任务扩展性有限。
- **状态转换频繁时收敛慢**：若切换过于频繁，每个状态观察量不足，导致各状态内的自适应参数收敛变缓，预测区间宽度可能变大。
- **极长时序的尖锐度劣势**：在 T≥10,000 的长序列上，CPTC 的区间宽度往往高于 SPCI、HopCPT 等专门通过在线学习残差结构的方法。
- **依赖状态空间模型**：需要额外训练一个能够预测状态的概率模型（如 SDS），对于不具备离散模式结构的普通时间序列，可能会增加模型复杂度。
- **风险边界仍需探索**：虽然展示了覆盖率要求，但对高风险场景下误覆盖的代价没有进行决策理论层面的分析。

（完）
