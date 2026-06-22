---
title: "xLSTM-Mixer: Multivariate Time Series Forecasting by Mixing via Scalar Memories"
title_zh: xLSTM-Mixer：通过标量记忆混合进行多变量时间序列预测
authors: "Maurice Kraus, Felix Divo, Devendra Singh Dhami, Kristian Kersting"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=JlVn0XRpy0"
tags: ["query:ts-forecast"]
score: 9.0
evidence: xLSTM-Mixer：通过标量记忆混合时间和变量信息
tldr: 针对多变量时间序列预测，本文提出xLSTM-Mixer模型，先使用跨变量共享的线性预测，再用xLSTM模块细化序列动态，最终融合多视角信息得到预测。实验证明该模型在多个数据集上取得优异性能，有效捕捉了时间与变量间复杂依赖关系，为时序预测提供了新型混合架构。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-jlvn0xrpy0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 769, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jlvn0xrpy0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1459, \"height\": 437, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jlvn0xrpy0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1456, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jlvn0xrpy0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1426, \"height\": 447, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jlvn0xrpy0/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1430, \"height\": 901, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-jlvn0xrpy0/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1465, \"height\": 1769, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 386, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 932, \"height\": 462, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1442, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1336, \"height\": 462, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1393, \"height\": 409, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1409, \"height\": 247, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1449, \"height\": 1120, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 905, \"height\": 1501, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 932, \"height\": 1507, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 932, \"height\": 1507, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 685, \"height\": 1180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 720, \"height\": 899, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1283, \"height\": 665, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1435, \"height\": 334, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-jlvn0xrpy0/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1443, \"height\": 465, \"label\": \"Table\"}]"
motivation: 多变量时序预测需要同时捕获时间和变量间的复杂模式。
method: 设计xLSTM-Mixer，融合线性预测、xLSTM块和多视角调和。
result: 在多个基准上超越现有模型，验证了架构的有效性。
conclusion: xLSTM-Mixer通过标量记忆混合机制有效建模时序动态。
---

## Abstract
Time series data is prevalent across numerous fields, necessitating the development of robust and accurate forecasting models.
 Capturing patterns both within and between temporal and multivariate components is crucial for reliable predictions.
  We introduce xLSTM-Mixer, a model designed to effectively integrate temporal sequences, joint time-variate information, and multiple perspectives for robust forecasting.
    Our approach begins with a linear forecast shared across variates, which is then refined by xLSTM blocks.
    They serve as key elements for modeling the complex dynamics of challenging time series data.
   xLSTM-Mixer ultimately reconciles two distinct views to produce the final forecast.
    Our extensive evaluations demonstrate its superior long-term forecasting performance compared to recent state-of-the-art methods while requiring very little memory.
    A thorough model analysis provides further insights into its key components and confirms its robustness and effectiveness.
    This work contributes to the resurgence of recurrent models in forecasting by combining them, for the first time, with mixing architectures.

---

## 论文详细总结（自动生成）

# 论文总结：xLSTM-Mixer – 通过标量记忆混合进行多变量时间序列预测

## 1. 论文的核心问题与整体含义
多变量时间序列预测在医疗、制造、金融、交通等领域有广泛应用，核心挑战在于同时捕获**时间维度内部的动态模式**和**变量之间的交互关系**。  
已有方法主要分为两类：  
- 基于 Transformer 的模型虽表达力强，但自注意力机制在长序列和大量变量时计算与内存开销过高；  
- 循环神经网络（RNN）效率较高，但传统 LSTM/GRU 难以建模超长期依赖。  

本文提出 **xLSTM‑Mixer**，首次将**扩展长短期记忆网络（xLSTM）**与**交叉混合（mixing）架构**相结合，旨在以极低的内存占用实现高准确度的长期多变量预测，推动循环模型在时间序列预测中的复兴。

---

## 2. 论文提出的方法论

### 2.1 整体架构
xLSTM‑Mixer 由三个阶段组成：
1. **初始线性预测（Time Mixing）**  
   - 先用可逆实例归一化（RevIN）对每个变量独立标准化。  
   - 采用跨变量**权重共享的 NLinear 模块**，将历史和预测步长进行线性映射，得到初始预测。  
   - 该操作在变量维度上共享参数，起到正则化和降参的作用。

2. **联合混合（Joint Mixing）**  
   - 将初始预测通过一个跨变量共享的线性层**上投影到更高维度 D**。  
   - 使用由 **sLSTM 块**堆叠而成的递归模块，**沿变量轴步进**（每个 token 代表一个变量的全部时间步长），同时混合时间与变量信息。  
   - sLSTM 块采用**标量记忆、指数门控与多头记忆混合**，使其能有效捕捉复杂跨变量和时间依赖。  
   - 引入**可学习的初始嵌入 token η**，作为条件化的软提示，作用于序列开头以提升表达力。

3. **视图混合（View Mixing）**  
   - 对原始嵌入及其**反转维度顺序**的嵌入分别通过 sLSTM 栈得到两个预测视图。  
   - 两个视图通过一个跨变量共享的全连接层**融合成最终预测**。  
   - 这相当于以多任务/集成的方式约束训练，改善泛化能力。  
   - 最后用 RevIN 逆运算恢复原始量纲。

**关键技术细节**  
- 仅使用 **sLSTM**（而弃用 mLSTM）：sLSTM 保留隐状态到隐状态的循环门控，具备记忆混合能力，适合捕获状态切换（如加热↔冷却），是长期预测的关键。  
- 归一化与跳跃连接：RevIN + NLinear 的减法中心化 + sLSTM 内部 skp 连接共同稳定训练。  
- 多视图混合：在原始和反向顺序上共享 sLSTM 权重，最终线性融合，不额外引入大量参数。

### 2.2 核心公式要点（文字描述）
- sLSTM 单元通过遗忘门、输入门、输出门更新细胞状态 `c_t`，并使用指数激活与稳定项 `m_t` 防止梯度问题。  
- 上投影：`x_up = FC_up(x_initial)`，将长度 H 的初始预测映射到维度 D。  
- sLSTM 处理：以变量顺序为序列，保持多头块对角循环矩阵以限制参数。  
- 最终输出：`y_norm = FC_view(y’, y’’)`，之后反归一化。

---

## 3. 实验设计

### 3.1 数据集与基准
- **长期预测基准**：Weather、Electricity、Traffic、ETTh1、ETTh2、ETTm1、ETTm2（共7个数据集），预测长度 {96, 192, 336, 720}，使用标准化后的 MSE 与 MAE。
- **概率预测基准**：GIFT‑Eval（含多域数据），评估 MASE 和 CRPS，同样适配模型输出分位数。

### 3.2 对比方法
覆盖循环模型（xLSTMTime、LSTM）、混合模型（TimeMixer++、TimeMixer、TSMixer）、MLP 模型（CycleNet、DLinear、TiDE）、状态空间模型（S‑Mamba、Chimera）、Transformer（PatchTST、iTransformer）、卷积模型（ModernTCN、TimesNet）以及预训练模型（Timer‑XL、Moirai Base）等，**共十余种 SOTA 方法**，对比全面。

### 3.3 评估方式
- 所有实验均采用**最优回溯窗口长度**（而非固定 96）进行公平比较，避免基准偏差。
- 每个设置重复 3 次（种子 2021,2022,2023），报告均值。
- 统计显著性检验：Friedman 检验加 Conover 事后检验，控制族错误率。

---

## 4. 资源与算力
- 模型训练在**单个 NVIDIA A100 80GB GPU** 上进行，使用 PyTorch + Lightning 框架。
- sLSTM 采用定制 CUDA 实现，要求 GPU 计算能力 ≥ 8.0。
- 论文未明确给出总训练时长（仅提供了每迭代时间及内存消耗随回溯长度变化的图），但强调其内存足迹极小，显著优于基于 Transformer 的模型。

---

## 5. 实验数量与充分性
- **长期预测**：7 数据集 × 4 预测长度 = 28 个主场景，每场景 3 次运行，对比 14 种以上模型。
- **消融研究**：13 种不同的模型配置（更换 RNN 类型、缺失组件、改变混合维度等），全面考察每个模块的贡献。
- **超参数敏感性**：隐藏维度 D、回溯长度 T、多头数量、学习率等影响分析。
- **概率预测**：GIFT‑Eval 全榜单 39 个模型对比，涵盖多领域。
- **分类任务**：在 10 个 UEA 分类数据集上评估，作为嵌入模型。
- **附加分析**：初始嵌入可视化、变量排列鲁棒性、多视图集成数量实验、特征归因（SHAP 值）等。  

整体实验**非常充分**，既有标准基准，又有多维度消融与定性分析，对比公平且包含统计检验。

---

## 6. 主要结论与发现
- xLSTM‑Mixer 在 28 个长期预测设置中，分别在 MSE 和 MAE 上取得了 11 次和 16 次最优，于 6/7 数据集上达到 SOTA，并具有极低内存占用。
- 在 GIFT‑Eval 概率预测中排名第 2（所有模型）且为最佳纯监督模型；分类任务上也表现优异。
- 消融实验表明，sLSTM 块、时间混合、视图混合等每个组件都对性能有正向贡献，缺一不可。
- 标量记忆型 sLSTM 比 mLSTM、LSTM、GRU 更适合长期混合预测；变体顺序虽有影响，但默认排序已足够有效。

---

## 7. 优点
- **高性能与高效率兼得**：精度与当前最佳模型持平或超越，而内存仅为 Transformer 模型的几十分之一。
- **架构创新**：首次将 xLSTM 与混合架构融合，利用 NLinear、变量维度循环、多视图调和，兼顾正则化和表达能力。
- **训练稳定**：通过 RevIN、跳跃连接、可学习初始 token、权重共享等设计，使模型在长回溯窗口下仍能稳健训练。
- **可解释性分析**：可视化初始 token 与特征归因，表明模型确实学习到数据集的季节模式和跨变量依赖。
- **复现性与代码开源**：详细附录和已公开代码，实验可复现。

---

## 8. 不足与局限
- **变量顺序固定**：默认使用数据集给定的顺序，虽然随机排列实验显示差异不大，但理论上顺序可能影响学习。
- **不适用不规则时间序列**：要求所有变量在统一时间网格上采样，缺失或非均匀时间戳需预处理。
- **极端高维度变量时可能受限**：递归步进变量轴，变量数极大时导致线性增长的运行时间和内存需求。
- **多视图混合增加归因难度**：同时混合两个视图使对单个预测的解释变得复杂，细节归因不够透明。
- **未涉及其他任务**：虽已拓展分类，但在异常检测、填充等任务上的适用性未经测试。

---

（完）
