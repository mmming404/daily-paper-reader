---
title: "MVG-CRPS: A Robust Loss Function for Multivariate Probabilistic Forecasting"
title_zh: MVG-CRPS：用于多元概率预测的鲁棒损失函数
authors: "Vincent Zhihao Zheng, Lijun Sun"
date: 2025-05-02
pdf: "https://openreview.net/pdf?id=mZuFaBAVs6"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 新型鲁棒闭式损失函数用于多元概率预测
tldr: 针对多元概率预测中负对数似然对异常值敏感而能量分数计算昂贵的问题，本文提出MVG-CRPS，一种适用于多元高斯分布的严格合适评分规则，具有异常值鲁棒性和闭式解。该损失函数可高效训练神经网络模型，显著提升概率预测的准确性和稳定性，对实际电力、气候等预测应用具有重要价值。
source: NeurIPS-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 513, \"height\": 391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 573, \"height\": 206, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 572, \"height\": 206, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1017, \"height\": 383, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 877, \"height\": 534, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 950, \"height\": 527, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1311, \"height\": 412, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1169, \"height\": 481, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 948, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 877, \"height\": 527, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mzufabavs6/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1089, \"height\": 632, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 572, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 567, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 738, \"height\": 514, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1317, \"height\": 816, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 775, \"height\": 390, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1456, \"height\": 569, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1490, \"height\": 589, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 737, \"height\": 537, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 737, \"height\": 541, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 800, \"height\": 552, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1456, \"height\": 569, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mzufabavs6/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1478, \"height\": 593, \"label\": \"Table\"}]"
motivation: 常用概率预测损失对流式数据异常值敏感或计算开销大。
method: 提出MVG-CRPS，一个针对多元高斯的鲁棒闭式评分规则。
result: 在多个数据集上取得比现有损失更优的预测性能。
conclusion: MVG-CRPS平衡了鲁棒性与计算效率，适合神经网络训练。
---

## Abstract
Multivariate probabilistic forecasting typically leverages neural network-based distributional regression, often employing Gaussian assumptions to simplify computation. While the standard negative log-likelihood provides analytical convenience, its sensitivity to outliers can severely degrade forecasting accuracy. Conversely, robust alternatives like the Energy Score, although less sensitive to extreme values, rely heavily on computationally expensive sampling approximations, limiting scalability in neural network training. To bridge this gap, we introduce the MVG-CRPS, a novel, strictly proper scoring rule for multivariate Gaussian distributions that maintains robustness to outliers while providing a closed-form expression, enabling efficient training and evaluation. Our approach leverages a whitening transformation, decorrelating multivariate outputs and reducing the multivariate scoring task to tractable univariate CRPS computations. Experiments on real-world datasets for both multivariate autoregressive and univariate sequence-to-sequence (Seq2Seq) forecasting tasks demonstrate that MVG-CRPS enhances robustness and predictive performance.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **背景与动机：** 多元概率预测（如天气、金融、能源等领域）通常基于神经网络输出高斯分布参数，并采用负对数似然（log‑score）作为损失函数。然而，log‑score 对异常值和极端事件高度敏感，会严重损害预测精度。
- **现有不足：** 鲁棒替代方案 Energy Score（ES）虽不易受极端值影响，但缺乏闭式解，必须依赖昂贵的蒙特卡洛采样来近似梯度和得分，大大降低了神经网络的训练效率。
- **本文目标：** 提出一种针对多元高斯分布的、严格合适（strictly proper）且具有闭式表达式的评分规则——MVG‑CRPS，以同时实现异常值鲁棒性与高效计算，从而在神经网络训练中替代 log‑score 和 Energy Score。

### 2. 方法论
- **核心思想：** 通过对预测的多元高斯分布进行 PCA 白化（whitening）变换，将协方差矩阵对角化，把多元连续排序概率分数（CRPS）拆解为若干独立单变量 CRPS 之和。由于单变量高斯 CRPS 拥有闭式解，整个多元得分无需采样即可直接计算。
- **技术流程：**
  - 对预测的协方差矩阵 \(\Sigma_t\) 进行奇异值分解（SVD）：\(\Sigma_t = U_t S_t U_t^\top\)，其中 \(S_t = \mathrm{diag}([\lambda_{1,t}, \dots, \lambda_{N,t}])\)。
  - 计算变换 \(v_t = U_t^\top (z_t - \mu_t)\)，此时 \(v_t \sim \mathcal{N}(0, S_t)\)。
  - 再做标准化 \(w_t = S_t^{-1/2} v_t\)，使得 \(w_{i,t} \sim \mathcal{N}(0,1)\)。
  - 最终 MVG‑CRPS 公式：\[
    \mathrm{MCRPS}(\Phi_N(\mu_t,\Sigma_t), z_t) = \sum_{i=1}^{N} \sqrt{\lambda_{i,t}} \, \mathrm{CRPS}(\Phi, w_{i,t}),
    \]
    其中 \(\Phi\) 为标准正态 CDF。该得分可解析求导，直接用于反向传播。
- **理论保证：** 论文在附录中证明了 MVG‑CRPS 在多元高斯族中是严格合适的评分规则（当且仅当预测分布与真实分布完全一致时期望得分最小）。

### 3. 实验设计
- **数据集：** 来自 GluonTS 的 13 个真实世界时间序列数据集，涵盖不同粒度和领域（电力、金融、交通、旅游等），如 `elec_au`、`cif_2016`、`electricity`、`traffic` 等。
- **任务与模型：**
  - **多元自回归预测**：使用基于 RNN 的 GPVar 和基于 decoder‑only Transformer 的模型。
  - **单变量 Seq2Seq 预测**：使用基于 MLP 的 N‑HiTS 模型。
- **对比方法：** 三种损失函数——log‑score（负对数似然）、Energy Score（蒙特卡洛近似，β=1）以及本文提出的 MVG‑CRPS。此外，还包含 VAR 作为朴素基线。
- **评估指标：** 连续排序概率分数和（CRPS sum）、逐点平均 CRPS（CRPS mean）以及 Energy Score 本身，均基于 100 个采样点近似计算。
- **附加实验：** 合成数据上的参数恢复实验（不同噪声水平）、控制性离群点注入实验、超参数（学习率、低秩维度）敏感性分析。

### 4. 资源与算力
- **硬件配置：** 1 颗 AMD Ryzen Threadripper PRO 5955WX CPU，4 块 NVIDIA RTX A5000 GPU（每块 24 GB 显存）。
- **训练时间对比（以 GPVar 为例，部分数据集）：**
  - `elec_au`：log‑score 33.5 min，Energy Score 717.0 min，MVG‑CRPS 29.1 min。
  - `electricity`：log‑score 67.4 min，Energy Score 782.4 min，MVG‑CRPS 22.7 min。
  可见 MVG‑CRPS 因无需采样，训练时间大幅缩短，甚至略快于 log‑score。

### 5. 实验数量与充分性
- **主要对比实验：** 在 13 个数据集上，对 3 种损失函数、2 类模型（GPVar 和 Transformer），兼及 Seq2Seq 任务（12 个数据集），每种配置均重复 10 次运行并报告均值和标准差。
- **补充实验：**
  - 合成数据上不同噪声水平（0%，2%，4%）的参数估计偏差分析（附箱线图）。
  - Energy Score 采样数量与精度、时间的权衡实验。
  - 可控离群点注入实验（多个数据集上固定噪声比例）。
  - 超参数敏感性网格搜索（学习率、低秩维度）。
- **公平性：** 除超参数敏感性实验外，主实验统一使用为 log‑score 调优的固定超参数，以避免因超参偏向新损失。所有评估指标独立于训练损失，避免了自我评估偏倚。
- 实验量丰富，覆盖了多元与单变量预测、不同模型架构和多种条件，统计检验充分（多次运行），具有较强的客观性和说服力。

### 6. 主要结论与发现
- **预测精度：** MVG‑CRPS 训练出的模型在 CRPS sum、CRPS mean 和 Energy Score 三项指标上平均排名均优于 log‑score，与 Energy Score 训练的结果相当或更优。
- **训练效率：** MVG‑CRPS 无需采样，训练时间仅为 Energy Score 的几十分之一，甚至比 log‑score 更快。
- **鲁棒性：** 在合成和真实数据的离群实验中，MVG‑CRPS 对异常值的敏感度远低于 log‑score，预测分布更稳定，协方差估计更少受极端误差影响。
- **敏感性：** 与 Energy Score 相比，MVG‑CRPS 对预测分布的协方差结构（相关系数等）具有更高的区分能力，同时保持平滑、良态的曲面。

### 7. 优点
- **闭式与高效：** 唯一同时具有严格合适性、鲁棒性和闭式解析梯度的多元评分规则，可直接嵌入深度学习框架，免去采样开销。
- **理论完备：** 给出了严格合适性的证明，以及得分对均值、协方差的敏感分析。
- **实用性强：** 支持低秩加对角协方差参数化，可通过随机批次处理高维序列，降低了高维场景下的计算负担。
- **实验全面：** 包含多种模型、数据集和额外分析，多角度验证了方法的优势与稳定性。

### 8. 不足与局限
- **高斯假设依赖：** 当前方法建立在多元高斯分布假设之上，当真实数据严重偏离正态时，可能影响适用性。
- **协方差分解开销：** 虽然训练总体快，但每次迭代需对 \(B \times B\) 的协方差矩阵做 SVD，当批次维度 \(B\) 很大时计算成本上升为 \(\mathcal{O}(B^3)\)。文中采用较小的 \(B\)（如 20）来缓解此问题。
- **扩展路径有限：** 虽然未来可通过连接函数（copula）扩展至非高斯边缘分布，但目前尚未实现，且该方法主要针对高斯分布族，对多峰或重尾分布的直接处理能力不如生成式模型。
- **Energy Score 的对比未最大化：** 在超参数调优实验中，Energy Score 因时间限制未进行充分调参，部分对比可能存在不公平因素。

（完）
