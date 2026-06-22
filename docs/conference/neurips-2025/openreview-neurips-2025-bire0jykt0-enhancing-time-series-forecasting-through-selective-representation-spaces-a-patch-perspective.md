---
title: "Enhancing Time Series Forecasting through Selective Representation Spaces: A Patch Perspective"
title_zh: 从补丁视角通过选择性表示空间增强时间序列预测
authors: "Xingjian Wu, Xiangfei Qiu, Hanyin Cheng, Zhengyu Li, Jilin Hu, Chenjuan Guo, Bin Yang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=BirE0jYKt0"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 可学习的选择性分块构建灵活的表示空间
tldr: 传统时间序列分块方法采用固定相邻分块，导致表示空间受限。本文首创选择性表示空间，提出SRS模块，通过可学习的选择性分块机制，自适应地包含最具信息量的子序列。该方法增强了表示的灵活性和表达能力，实验表明在多个预测基准上优于固定分块方案，为补丁技术提供了新的扩展方向。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-bire0jykt0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 724, \"height\": 785, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bire0jykt0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1438, \"height\": 581, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bire0jykt0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1441, \"height\": 524, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bire0jykt0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1441, \"height\": 374, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bire0jykt0/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1449, \"height\": 505, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bire0jykt0/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1450, \"height\": 505, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bire0jykt0/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1440, \"height\": 505, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1449, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1451, \"height\": 479, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 735, \"height\": 506, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 730, \"height\": 319, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 703, \"height\": 345, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 706, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1451, \"height\": 845, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1449, \"height\": 267, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1447, \"height\": 371, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1449, \"height\": 372, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1451, \"height\": 757, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bire0jykt0/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1452, \"height\": 730, \"label\": \"Table\"}]"
motivation: 传统固定补丁分割导致表示空间固定，无法灵活捕捉最信息性的子序列。
method: 提出选择性表示空间（SRS）模块，利用可学习的补丁选择和表示优化提升预测性能。
result: SRS在多个数据集上优于传统补丁方法，显著提升了预测精度。
conclusion: 选择性补丁为时间序列表示学习提供了更灵活、更强大的范式。
---

## Abstract
Time Series Forecasting has made significant progress with the help of Patching technique, which partitions time series into multiple patches to effectively retain contextual semantic information into a representation space beneficial for modeling long-term dependencies. However, conventional patching partitions a time series into adjacent patches, which causes a fixed representation space, thus resulting in insufficiently expressful representations. In this paper, we pioneer the exploration of constructing a selective representation space to flexibly include the most informative patches for forecasting. Specifically, we propose the Selective Representation Space (SRS) module, which utilizes the learnable Selective Patching and Dynamic Reassembly techniques to adaptively select and shuffle the patches from the contextual time series, aiming at fully exploiting the information of contextual time series to enhance the forecasting performance of patch-based models. To demonstrate the effectiveness of SRS module, we propose a simple yet effective SRSNet consisting of SRS and an MLP head, which achieves state-of-the-art performance on real-world datasets from multiple domains. Furthermore, as a novel plug-and-play module, SRS can also enhance the performance of existing patch-based models. The resources are available at https://github.com/decisionintelligence/SRSNet.

---

## 论文详细总结（自动生成）

好的，以下是基于所提供的论文内容生成的结构化中文总结。

### 1. 论文的核心问题与整体含义

*   **研究背景与动机**
    *   时间序列预测（TSF）中，“分块（Patching）”技术已成为主流，它通过将时间序列分割成子序列块来捕获局部语义信息，并构建用于建模的表示空间。
    *   然而，传统的分块方法（如PatchTST）采用**固定步长的相邻分块**，导致为所有输入序列构建一个**固定的、缺乏灵活性的表示空间**。
    *   这种固定空间假设所有有用信息均匀分布，但当时间序列存在**周期变化、分布偏移、异常点**时，会引入有害信息或错过关键信息，破坏了该假设。

*   **核心问题**
    *   如何打破固定分块的限制，构建一个**灵活、自适应的选择性表示空间**，使其能够动态地包含对预测最具信息量的子序列块，从而提升模型的表达能力和预测精度。

### 2. 论文提出的方法论

*   **核心思想**
    *   提出一个名为**选择性表示空间 (Selective Representation Space, SRS)**的即插即用模块。该模块不采用固定索引选取子序列，而是通过可学习的方式，自适应地从上下文序列中挑选出最有利于预测的一系列块，并重组其顺序，从而构建一个灵活的表征空间。
*   **关键技术细节**
    *   **选择性分块（Selective Patching）**：
        *   **候选块生成**：以步长1扫描填充后的上下文序列，生成所有可能的候选块。
        *   **可学习评分与选取**：设计一个基于多层感知机（MLP）的`Scorer_s`，为每个候选块的\(n\)次采样生成分数。通过`Argmax`操作选出每轮得分最高的块，实现**有放回选取**。
        *   **梯度保持**：为解决`Argmax`不可导的问题，采用一种巧妙的方法：取出选中块及其最大得分，将该得分的倒数从计算图中分离（独热连接），再与最大得分相乘得到全一矩阵（带梯度），最后将该矩阵与选中块进行哈达玛积，从而构建梯度传播路径。
    *   **动态重组（Dynamic Reassembly）**：
        *   在选定\(n\)个块后，使用另一个基于MLP的`Scorer_r`为这些块打分。
        *   使用`Argsort`根据分数对选中的块进行排序，同样采用上述梯度保持技巧，实现可学习的顺序重组，以确定这些块的最优排列。
    *   **自适应融合（Adaptive Fusion）**：
        *   将来自传统相邻分块和来自SRS模块（经过选择和重组）的块分别进行线性嵌入。
        *   引入一个可学习的凸组合系数\(\alpha \in [0,1]\)，对两组嵌入进行加权融合（\(\tilde{E} = \alpha \odot E_c + (1 - \alpha) \odot E_s\)），最后加上位置编码，构成最终的模型输入。
    *   **整体网络（SRSNet）**
        *   一个极简的强基线模型，将SRS模块与一个简单的MLP预测头组合，用于验证SRS的有效性。

### 3. 实验设计

*   **数据集**：在8个来自不同领域的真实世界数据集上进行实验，包括ETT（4个子集）、Weather、Electricity、Solar和Traffic。
*   **预测设置**：采用4种预测长度（{96, 192, 336, 720}）和多种回溯窗口大小（{96, 336, 512}），报告最优结果。
*   **评估指标**：均方误差（MSE）和平均绝对误差（MAE）。
*   **对比方法（Benchmark）**：
    *   与近年的多个最先进模型进行对比，涵盖多种架构：
        *   **Transformer类**：FEDformer、Stationary (Non-stationary Transformer)、PatchTST、Crossformer、iTransformer。
        *   **CNN/MLP类**：TimesNet、DLinear、TimeMixer、SparseTSF、PatchMLP、xPatch、Amplifier。
        *   **其他**：TimeKAN。

### 4. 资源与算力

*   **硬件平台**：所有实验均在**NVIDIA Tesla-A800 GPU**上执行。
*   **软件环境**：Python 3.8 和 PyTorch。
*   **计算效率**：论文在表5和表6中对比了SRSNet与其他模型的GPU内存占用（MB）和每批次训练时间（s）。将SRS模块集成到PatchTST和Crossformer中，**仅增加了约10%的内存、推理和训练时间开销，且MACs（乘加运算）增加不到5%**，表明其计算开销较小，具有实用性。

### 5. 实验数量与充分性

实验设计**较为全面且充分**，旨在客观、公平地验证方法有效性。
*   **主要结果**：在8个数据集、4种预测长度上与超过10种基线模型进行详尽的性能对比。
*   **消融研究**：
    *   **模块有效性**：将SRS作为插件集成到MLP、PatchTST、Crossformer、PatchMLP、xPatch这5种不同架构和年代的模型中，验证其普适性。
    *   **组件有效性**：设计了4种变体（移除SRS、移除选择性分块、移除动态重组、移除自适应融合）来逐个验证SRS内部各组件的作用。
*   **效率分析**：对比了SRSNet与多种基线模型的计算效率，并单独分析了SRS模块的开销。
*   **参数敏感性分析**：研究了分块大小、回溯窗口长度以及Scorer网络的隐藏层数和维度等关键超参数的影响。

### 6. 论文的主要结论与发现

*   SRS模块能够有效构建**灵活的选择性表示空间**，自适应地捕获对预测最有益的信息，从而显著提升了基于分块模型的预测性能。
*   由SRS和MLP构成的简单模型**SRSNet**，在多个基准数据集上达到了**最先进（SOTA）**或极具竞争力的性能，证明了良好的表示空间比复杂的模型骨架更为关键。
*   作为一个**即插即用**的模块，SRS可以轻松集成到PatchTST、Crossformer等现有模型中，并带来普遍且一致的性能提升。

### 7. 优点

*   **概念新颖**：率先从“选择性表示空间”这一视角审视时间序列分块问题，赋予了模型动态捕获关键信息的能力。
*   **技术巧妙**：通过一种简洁高效的技巧解决了排序/选取操作中的不可导问题，使得整个流程可以通过梯度下降端到端优化。
*   **即插即用**：模块化设计使其能够灵活增强多种现有模型，具有良好的通用性和实用性。
*   **高效且有效**：SRS模块在带来显著性能提升的同时，计算开销相对可控。SRSNet模型结构极简却性能强大，实现了效率与性能的良好平衡。
*   **实验扎实**：实验覆盖多个领域和多种基线，消融研究深入，充分证明了方法的有效性和各组件的贡献。

### 8. 不足与局限

*   **局限于分块模型**：SRS模块的机制天然适用于基于分块的模型。对于非分块模型，强行使用（如设置分块大小为1）会丧失其语义优势，且增加计算开销，因此不具普适性。
*   **可解释性不足**：虽然SRS能选出有用的块，但整个过程是黑盒的、数据驱动的，并非所有被选中的块都具有明确的可解释性。
*   **规模化定律未验证**：在端到端的小规模训练场景下表现良好，但其在大规模语料的预训练基础模型场景下的有效性和可扩展性尚未得到验证。
*   **初始化敏感**：模块中用于平衡融合的系数\(\alpha\)的初始化对性能有一定影响，论文建议根据数据集先验知识手动调整以提升收敛性和稳定性，这增加了使用门槛。
*   **缺乏理论分析**：论文主要依赖实验验证，缺乏理论层面的证明，例如算法的收敛性、泛化误差界等。

（完）
