---
title: "TS-RAG: Retrieval-Augmented Generation based Time Series Foundation Models are Stronger Zero-Shot Forecaster"
title_zh: TS-RAG：基于检索增强生成的时间序列基础模型实现更强的零样本预测
authors: "Kanghui Ning, Zijie Pan, Yu Liu, Yushan Jiang, James Y. Zhang, Kashif Rasul, Anderson Schneider, Lintao Ma, Yuriy Nevmyvaka, Dongjin Song"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=PymOnHw4Ty"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 检索增强生成框架用于零样本时间序列预测
tldr: 现有时间序列基础模型在零样本泛化和处理分布漂移方面面临挑战。本文提出TS-RAG，一个检索增强生成框架，利用预训练编码器检索语义相似的序列片段，并将其融入预测生成过程。实验结果表明，该方法有效提升了零样本预测的泛化性和可解释性，为增强基础模型适应能力提供了新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-pymonhw4ty/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1423, \"height\": 648, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pymonhw4ty/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1412, \"height\": 680, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pymonhw4ty/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1364, \"height\": 343, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pymonhw4ty/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 695, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pymonhw4ty/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 657, \"height\": 464, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pymonhw4ty/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 554, \"height\": 794, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pymonhw4ty/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1291, \"height\": 781, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pymonhw4ty/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1279, \"height\": 901, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pymonhw4ty/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1288, \"height\": 786, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-pymonhw4ty/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1278, \"height\": 906, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1451, \"height\": 400, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1229, \"height\": 264, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1326, \"height\": 230, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 617, \"height\": 138, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 711, \"height\": 134, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1443, \"height\": 751, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1439, \"height\": 310, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1439, \"height\": 416, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1429, \"height\": 344, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1429, \"height\": 443, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1441, \"height\": 308, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1355, \"height\": 354, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1428, \"height\": 325, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-pymonhw4ty/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1083, \"height\": 278, \"label\": \"Table\"}]"
motivation: 时间序列基础模型在非平稳动态和分布漂移下泛化能力有限。
method: 提出TS-RAG，使用预训练时间序列编码器检索相关片段，增强生成式预测。
result: 在零样本预测任务上取得更强泛化性和可解释性。
conclusion: 检索增强生成为提高时间序列基础模型的适应性和透明度提供了有效范式。
---

## Abstract
Large Language Models (LLMs) and Foundation Models (FMs) have recently become prevalent for time series forecasting tasks. While fine-tuning LLMs enables domain adaptation, they often struggle to generalize across diverse and unseen datasets. Moreover, existing Time Series Foundation Models (TSFMs) still face challenges in handling non-stationary dynamics and distribution shifts, largely due to the lack of effective mechanisms for adaptation. To this end, we present TS-RAG, a retrieval-augmented generation framework for time series forecasting that enhances the generalization and interpretability of TSFMs. Specifically, TS-RAG leverages pre-trained time series encoders to retrieve semantically relevant segments from a dedicated knowledge base, enriching the contextual representation of the input query. Furthermore, we propose an Adaptive Retrieval Mixer (ARM) module that dynamically fuses the retrieved patterns with the TSFM's internal representation, improving forecasting accuracy without requiring task-specific fine-tuning. Thorough empirical studies on seven public benchmark datasets demonstrate that TS-RAG achieves state-of-the-art zero-shot forecasting performance, outperforming the existing TSFMs by up to 6.84\% across diverse domains while also providing desirable interpretability. Our code and data are available at: https://github.com/UConn-DSIS/TS-RAG.

---

## 论文详细总结（自动生成）

# 论文总结：TS-RAG——基于检索增强生成的时间序列基础模型实现更强的零样本预测

## 1. 研究动机与核心问题
- **背景**：时间序列预测在金融、医疗、能源、气象等领域至关重要。近年来，大语言模型（LLM）和时间序列基础模型（TSFM）被广泛应用，但其零样本泛化能力仍存在瓶颈。
- **痛点**：
  - 微调后的 LLM 难以泛化到未见过的新数据集。
  - 现有 TSFM 缺乏对非平稳动态和分布漂移的有效适应机制，导致在跨域或真实场景下性能下降。
  - TSFM 的预测过程通常缺乏可解释性，限制了在高风险决策中的应用。
- **整体意图**：提出 **TS-RAG**，一个检索增强生成框架，通过动态检索与输入查询语义相似的历史片段，并自适应地融合到生成预测中，**在不需下游微调的情况下，提升 TSFM 的零样本预测性能和可解释性**。

## 2. 方法论

### 2.1 核心思想
- 将检索增强生成（RAG）范式引入时间序列预测。
- 对于一个输入查询窗口，利用预训练编码器检索语义上最接近的若干历史片段及其对应的未来观测，通过一个可学习的**自适应检索混合器（ARM）**将这些检索到的模式与 TSFM 的内部表征动态融合，最终生成更准确的预测。

### 2.2 关键技术组件
1. **检索知识库（Retrieval Knowledge Base）**
   - 基于 Chronos 的预训练数据集，构建包含数百万条 `(历史窗口, 未来窗口)` 的数据对。
   - 使用预训练的 Chronos 编码器为每个历史窗口生成嵌入向量，形成 `{(x_i, e_i, y_i)}` 三元组存储。
   - 支持多种建库策略：同域、分布偏移、跨域、多域。

2. **检索器（Retriever）**
   - 输入查询序列 \(x_q\)，由同一个 Chronos 编码器 \(f_{enc}\) 得到嵌入 \(e_q\)。
   - 计算与知识库嵌入的欧氏距离，选取 top-k 最相似候选集 \(C = \{ (x_i, y_i) \}\)。

3. **自适应检索混合器（ARM）**
   - 对检索到的未来窗口 \(y_i\) 通过 MLP 投影得到 \( \hat{e}_i \)。
   - 将查询表征 \(\hat{e}_q\) 与检索到的 k 个表征拼接，得到 \(E_{concat} \in \mathbb{R}^{(k+1)\times d}\)。
   - 经过多头自注意力（MHA）和残差连接，再通过前馈网络（FFN）和 Dropout：
     \[
     E_{att} = \text{MHA}(E_{concat}) + E_{concat}
     \]
     \[
     E_{ffn} = \text{Dropout}(FFN(E_{att})) + E_{att}
     \]
   - 学习每个位置的权重 \(\alpha = \text{Softmax}(W_g E_{ffn} + b_g)\)，进行加权求和并加上跳跃连接（原始查询嵌入）：
     \[
     e_{final} = \hat{e}_q + \sum_{i=1}^{k+1} \alpha_i E_{ffn,i}
     \]
   - 最终表示 \(e_{final}\) 送入 TSFFM 原有的输出投影层，得到预测值 \(\hat{y}_q\)。

### 2.3 训练与推理策略
- **预训练**：只训练 ARM 中的 MLP 投影和混合模块，TSFM 主干和检索编码器完全冻结。预训练数据为 Chronos 预训练集的子集（2600 万对），损失函数与主干模型一致（如 Chronos-Bolt 的分位数回归损失）。
- **零样本推理**：直接使用预训练的 ARM 和检索知识库，无需任何下游微调。
- **扩展预测长度**：通过滚动预测，每次迭代都进行检索增强。

## 3. 实验设计

### 3.1 数据集
- **评测基准**：七个公共数据集：ETTh1, ETTh2, ETTm1, ETTm2, Weather, Electricity, Exchange Rate。
- **预训练与知识库**：从 Chronos 预训练集均匀采样 5 千万点作为预训练数据，再从中采样 5 百万点构建多域检索知识库。
- **数据划分**：ETT 数据集 6:2:2，Weather/Electricity/Exchange 7:1:2。

### 3.2 对比方法
- 主要基线：**Chronos-Bolt**（TS-RAG 的主干模型）、**Chronos**、**MOMENT**、**TTM**、**Moirai**、**TimesFM**、**Time-MoE**。
- 还专门与近期的检索增强预测方法 **RAF** 进行了有效性和效率对比。

### 3.3 评估指标
- 均方误差（MSE）、平均绝对误差（MAE）。

## 4. 资源与算力
- **硬件**：所有训练在 **单块 NVIDIA A6000 (48 GB)** GPU 上完成，使用 TF32 精度。
- **训练时间**：在 2600 万对预训练数据上，训练 20,000 步仅需 **约 1 小时**。
- **推理效率**：使用 FAISS 加速检索，单次查询检索耗时 9.2 ms，ARM 前向 0.44 ms，总耗时 **9.62 ms/查询**，比 RAF 的 3.47 秒快约 360 倍。

## 5. 实验数量与充分性

### 5.1 主要实验
- **零样本长期预测（512→64）**：在 7 个数据集上对比 8 种方法，包含 TS-RAG 与 Chronos-Bolt、MOMENT、TTM、Moirai、TimesFM、Chronos、Time-MoE。报告 MSE 和 MAE。

### 5.2 消融实验
- **检索知识库的影响**：四种建库策略（同域、分布偏移、跨域、多域），全面评估不同场景下的增益。
- **ARM 模块有效性**：与简单的门控线性融合对比，证明 ARM 设计的优越性。
- **更长的预测跨度**：扩展到 96、192、336、720 步，展示滚动预测中 RAG 的持续增益。
- **检索回看长度**：测试 64、128、256、512 四种长度，分析历史上下文长度的影响。
- **检索序列数量 k**：从 1 到 20 变化，观察性能变化趋势。
- **检索编码器选择**：对比 Chronos、TTM、MOMENT 三种不同架构的检索编码器，显示框架对编码器选择的鲁棒性。
- **距离度量**：对比欧氏距离、余弦相似度和 DTW 距离，表明嵌入空间度量更优。
- **与 RAF 的全面对比**：包括有效性和效率分析，并提供基于相同主干（Chronos-Bolt）的公平比较。

### 5.3 其他分析
- **可解释性案例研究**：通过可视化检索到的相似序列及其在预测中的作用，展示 RAG 提供的证据和透明权重。
- **统计特性与增益关系**：分析数据集的自相关性、噪声比、波动率和平稳性，发现强自相关性对应的数据增益更显著。

总体而言，实验覆盖了多个维度，对比基线丰富，消融和定性分析充分且设计公平，可信度较高。

## 6. 主要结论与发现
- **TS-RAG 在全部七个数据集上均取得最优零样本预测性能**，相比 Chronos-Bolt 平均降低 MSE 3.54%，在 Exchange Rate 数据集上降低达 6.84%。
- **检索增强方案通用性强**：将框架应用于 Chronos-Bolt 和 MOMENT 两种不同架构的 TSFM 主干，均能一致提升预测精度。
- **ARM 模块设计关键**：相比简单的门控融合，基于注意力机制的动态混合器能更有效地融合检索信息，性能提升更显著。
- **检索质量对性能有决定性影响**：同域检索效果最好，较长的回看窗口（256 或 512）通常能检索到更相关的模式。
- **TS-RAG 兼具高效与高效**：推理速度远快于同期检索增强方案 RAF，且性能更优。
- **显著增强可解释性**：通过直接展示检索到的相似序列及其权重，提供了预测的证据支持。

## 7. 优点
- **方法论创新**：首次将 RAG 思想系统地构建成适用于多种 TSFM 的即插即用框架，并提出精巧的 ARM 混合模块。
- **零样本能力强**：无需微调，利用外部检索库显著提升对未见域的泛化性能。
- **效率卓越**：训练只微调极少参数（1 小时单卡），推理近乎无额外开销（9.62 ms），实际应用潜力大。
- **实验充分扎实**：覆盖多个数据集、多种 TSFM 主干、多种检索设置，消融实验和案例分析全面。
- **可解释性突出**：为“黑箱”基础模型提供了透明的决策依据，利于高风险场景部署。
- **开源与可复现**：提供代码和数据存储库。

## 8. 不足与局限
- **模态单一**：目前仅使用时间序列数据作为检索源，未融入文本、元数据等多模态信息，限制了在复杂上下文场景下的潜力。
- **应用场景受限**：主要评测集中在标准公开基准，尚未在金融、医疗等真实复杂业务场景中大规模验证，实际泛化风险尚不明确。
- **同域检索依赖**：若无法获取同分布或同模态的检索库（如全新传感器数据），性能增益可能大幅降低。
- **检索回看长度选择缺乏自适应性**：更长回看虽普遍有益，但可能引入噪声，目前为固定超参。
- **统计显著性缺失**：零样本预测为确定性过程，未报告方差或置信区间，一定程度上影响结论的稳健性论述。
- **预训练数据仍来源于原 TSFM 数据集**：难以完全避免与某些基准数据集的信息泄露风险（论文已按标准划分）。

（完）
