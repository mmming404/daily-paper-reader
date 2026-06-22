---
title: "Many Minds, One Goal: Time Series Forecasting via Sub-task Specialization and Inter-agent Cooperation"
title_zh: 众智一心：通过子任务专业化和智能体间合作进行时间序列预测
authors: "Qihe Huang, Zhengyang Zhou, Yangze Li, Kuo Yang, Binwu Wang, Yang Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=Uon41HfqR3"
tags: ["query:ts-forecast"]
score: 10.0
evidence: 通过子任务专业化和智能体间合作进行时间序列预测
tldr: 相较于单一模型，本文提出多智能体合作框架，将预测任务分解为不同子任务，由专业智能体分工处理，再通过协同得出最终预测。该方法能适应多样时序模式和多步预测需求，在多个数据集上展现了优于整体模型的泛化能力和鲁棒性，为智能体在时序预测中的应用提供了有效范式。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1344, \"height\": 476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1176, \"height\": 662, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1318, \"height\": 595, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1282, \"height\": 537, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1233, \"height\": 427, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1445, \"height\": 223, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1023, \"height\": 518, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1446, \"height\": 558, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1447, \"height\": 559, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1447, \"height\": 566, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1448, \"height\": 569, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1447, \"height\": 560, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1448, \"height\": 566, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1448, \"height\": 570, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1445, \"height\": 560, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1448, \"height\": 563, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1448, \"height\": 570, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1445, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1447, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1448, \"height\": 494, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1445, \"height\": 492, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1446, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1445, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1447, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1445, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1445, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1445, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1447, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uon41hfqr3/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1446, \"height\": 493, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-uon41hfqr3/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1447, \"height\": 470, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uon41hfqr3/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 352, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uon41hfqr3/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1150, \"height\": 579, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uon41hfqr3/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1445, \"height\": 2067, \"label\": \"Table\"}]"
motivation: 单一模型难以同时捕捉时间序列的多样性模式和预测范围。
method: 提出多智能体系统，各智能体专攻子任务，通过合作实现预测。
result: 在多种复杂预测场景下，合作框架优于传统单体模型。
conclusion: 智能体分工合作机制为时序预测提供了灵活且强大的新途径。
---

## Abstract
Time series forecasting is a critical and complex task, characterized by diverse temporal patterns, varying statistical properties, and different prediction horizons across datasets and domains. Conventional approaches typically rely on a single, unified model architecture to handle all forecasting scenarios. However, such monolithic models struggle to generalize across dynamically evolving time series with shifting patterns. In reality, different types of time series may require distinct modeling strategies. Some benefit from homogeneous multi-scale forecasting awareness, while others rely on more complex and heterogeneous signal perception. Relying on a single model to capture all temporal diversity and structural variations leads to limited  performance and poor interpretability. To address this challenge, we propose a Multi-Agent Forecasting System (MAFS) that abandons the one-size-fits-all paradigm. MAFS decomposes the forecasting task into multiple sub-tasks, each handled by a dedicated agent trained on specific temporal perspectives (e.g., different forecasting resolutions or signal characteristics).  Furthermore, to achieve holistic forecasting, agents share and refine information through different communication topology, enabling cooperative reasoning across different temporal views. A lightweight voting aggregator then integrates their outputs into consistent final predictions. Extensive experiments across 11 benchmarks demonstrate that MAFS significantly outperforms traditional single-model approaches, yielding more robust and adaptable forecasts.

---

## 论文详细总结（自动生成）

好的，以下是对该论文的结构化、深入、客观的总结。

### 1. 论文的核心问题与整体含义

*   **研究动机**：传统的时间序列预测模型通常采用“一刀切”的单体架构，试图用一个统一的模型捕捉所有时间模式（如趋势、周期性、不同尺度等）。然而，现实世界中的时间序列数据具有多样性和动态变化的特点，不同的数据或预测范围可能需要不同的建模策略。
*   **核心问题**：单体模型难以同时泛化到具有异质性、非平稳性的多种时间模式上，导致预测性能受限且可解释性差。
*   **整体含义**：本文旨在打破单体模型的范式，引入多智能体系统（MAS）来解决时间序列预测的复杂性。核心思想是“众智一心”，即通过多个专业化的智能体分工协作，各自处理特定子任务，最终通过合作推理和聚合，实现比单一模型更稳健、更适应性强、更可解释的预测。

### 2. 论文提出的方法论

*   **核心思想**：提出了一个名为 **MAFS（多智能体预测系统）** 的框架。该框架包含`N`个专门的预测智能体。它将全局预测任务分解，让每个智能体专注于一个特定的子任务，并通过结构化的通信和投票机制进行协作，最终生成统一的预测结果。
*   **技术细节与流程**：
    *   **整体流程**：
        \[
        \hat{Y} = \text{AVA}(\text{Comm}(\{\text{Agent}_1(X), \dots, \text{Agent}_N(X)\}; G))
        \]
        其中，输入序列`X`经过各智能体处理，然后通过通信图`G`进行信息交换，最后由智能体评分投票聚合器（AVA）生成最终预测`Ŷ`。
    *   **智能体架构**：每个智能体采用可插拔的编码器-解码器架构（实验中使用了 iTransformer），共享输入，但根据不同的子任务目标优化专属参数 \( \Theta_A \)。
    *   **两阶段训练**：
        1.  **阶段一：专长预训练**：为每个智能体分配独特的子任务（见下文），并在每层编码器后，通过固定的通信拓扑图（环、星、链、全连接）进行信息交互（基于图卷积）。此阶段只优化智能体自身参数。
        2.  **阶段二：协同预测**：冻结所有智能体的参数，只训练**拓扑感知权重调节器**（使通信边权 \( \Theta_T \) 可学习）和**智能体评分投票聚合器**（AVA，参数 \( \Theta_P \)）。
    *   **子任务分解（促进专业化）**：
        1.  **同质分解（多尺度预测）**：各智能体负责预测不同长度的未来序列（如智能体`i`预测未来的前 `i/N * L` 步），形成短期到长期的层次化预测。
        2.  **异质分解（多视角预测）**：各智能体负责预测未来信号的不同特性，如趋势成分、季节性成分、频率域能量、统计矩（均值、方差等）。
    *   **智能体间通信**：采用图卷积网络（GCN）实现。每个智能体的隐藏状态`Hl_i`会根据其邻居`N(i)`的隐藏状态进行更新，公式为：
        \[
        HC^l_i = \sigma\left(\sum_{j \in N(i)} A_{ij} \cdot W \cdot H^l_j\right)
        \]
        其中`A`为归一化的邻接矩阵，`W`是可学习的投影矩阵。
    *   **投票聚合器（AVA）**：包含两个部分：
        1.  **智能体置信度估计器**：每个智能体通过一个自评估的闸门网络，融合自身预测和全局上下文，生成置信度调整后的表示。
        2.  **全局投票器**：通过一个 MLP 网络学习各智能体的协同权重，对置信度调整后的表示进行加权求和，生成统一隐藏表示，最终通过线性层投射为预测结果。

### 3. 实验设计

*   **数据集与场景**：在 **11 个** 来自不同领域的真实世界数据集上进行了长期时间序列预测实验。
    *   **电力领域**：ETTh1， ETTh2, ETTm1, ETTm2。
    *   **环境领域**：Weather， PM2.5, AQShunyi, AQWan。
    *   **自然领域**：CzeLan， ZafNoo, Temp。
*   **对比基准（Benchmark）**：与 **9 种** 最具代表性的先进模型进行了对比，涵盖了不同架构：
    *   **Transformer类**：iTransformer, Crossformer, PatchTST, Autoformer, Informer。
    *   **线性/简单模型类**：TimeMixer, DLinear。
    *   **多层感知机类**：TiDE。
    *   **周期建模类**：TimesNet。
*   **评估指标**：均方误差（MSE）和平均绝对误差（MAE）。

### 4. 资源与算力

*   论文明确指出所有实验均在配备 **8 块 NVIDIA A100 GPU（80GB 显存）** 的服务器上进行。
*   实现框架为 PyTorch 1.13.0，使用 Adam 优化器和 L2 损失函数。
*   训练分为两个阶段，每阶段均训练 **10 个 epochs**。智能体数量在 {4, 8, 12， 16, 20， 24} 范围内验证。然而，论文**未明确报告**整体的训练时长。

### 5. 实验数量与充分性

*   **实验数量庞大且全面，充分性高。**
*   **主实验**：在11个数据集 × 4种预测长度下，与9个基线模型进行全面对比，构成了一个庞大的实验结果矩阵。
*   **消融实验**：系统地移除了通信模块、投票聚合器和子任务专业化，以验证各组件的有效性。
*   **模型分析实验**：
    *   **规模化实验**：研究了不同智能体数量（4 - 24个）对性能的影响。
    *   **通信拓扑实验**：对比了环、星、链、全连接四种通信结构。
    *   **子任务分解策略实验**：对比了同质分解与异质分解在不同数据集上的表现。
*   **案例研究**：通过可视化智能体子任务表现、投票权重和通信权重，增强了模型的可解释性。
*   **公平性**：论文遵循了统一的实验设置（如对称预测长度），并纠正了先前评估流程中的一个小错误（`drop_last=True`），确保了评估的完整和公平。

### 6. 论文的主要结论与发现

*   **性能优越且鲁棒**：MAFS 在所有 11 个基准数据集上一致地超越了先进的单体模型基线，在22个（MSE和MAE）指标中，获得了 **16 个第一、20 个前二** 的排名。相较于其骨干网络 iTransformer，MAFS 平均降低了 **6.35% 的 MSE** 和 **4.03% 的 MAE**。
*   **组件有效性已验证**：消融研究证实，智能体通信、任务专业化和投票聚合器是 MAFS 性能提升的关键驱动因素，移除任一部分都会导致性能显著下降。
*   **分工与协作机制的优势**：通过子任务分解，各智能体能成功发展出不同的专业能力；通过投票和自适应通信，系统能有效整合这些专业能力，避免了智能体坍塌或对单一专家的过度依赖。
*   **系统可扩展性强**：在一定范围内增加智能体数量通常能提高或稳定性能，但存在饱和点（约16个）。

### 7. 优点

*   **新颖的范式**：首次将多智能体系统（MAS）的思想系统性地引入时间序列预测，为处理复杂时序数据提供了全新的“分工-协作”视角，打破了单体模型的设计局限。
*   **灵活且模块化的设计**：智能体的骨干网络可插拔，通信拓扑可配置，子任务可灵活定义（同质/异质分解），具有高度的模块化和可扩展性。
*   **增强的可解释性**：通过显式地分解子任务、可视化投票权重和通信强度，模型的决策过程比传统的黑盒模型更加透明和可解释。
*   **严谨且全面的实验验证**：实验设计非常扎实，不仅与大量SOTA模型在广泛数据集上对比，还进行了详尽的消融、参数分析和案例研究，结论极具说服力。
*   **有效的协同机制**：提出的两阶段投票聚合器（AVA）结合了自评估和全局评估，能动态地、自适应地整合不同智能体的贡献，优于简单的平均或固定融合策略。

### 8. 不足与局限

*   **计算开销未充分讨论**：尽管报告了硬件，但未明确给出 MAFS 相较于基线模型的具体训练/推理时间和参数量。运行 `N` 个智能体实例并相互通信，其计算和内存成本显然高于单体模型，这对其在资源受限场景下的实用性构成了挑战。
*   **训练稳定性**：作者在附录的局限性部分也承认，当智能体数量增加或处理高度波动数据时，训练过程可能出现不稳定性，暗示了优化过程可能较为困难。
*   **超参数敏感性**：论文引入了多个新超参数（智能体数量、通信拓扑、分解策略），虽然进行了分析和推荐，但在实际应用中选择和调优这些参数可能会增加使用成本和复杂度。
*   **协作机制的复杂度**：当前的通信机制和投票机制相对复杂，未来是否存在更简洁高效的协作方式值得探索。这也可以看作是未来优化的方向，而非纯负面影响。

（完）
