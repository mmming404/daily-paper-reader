---
title: "DecompNet: Enhancing Time Series Forecasting Models with Implicit Decomposition"
title_zh: DecompNet：通过隐式分解增强时间序列预测模型
authors: "Donghao Luo, Xue Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=ioXn68lBjO"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 隐式分解框架在无推理开销的情况下增强预测模型
tldr: 针对传统时序预测模型逐步分解带来的计算开销，本文提出DecompNet框架，通过隐式分解将分解知识注入模型，在推理时不需实际分解序列即可继承分解的性能收益。在多个基准数据集上验证，DecompNet能显著提升各类基模型的预测精度，同时保持推理效率，为高效时序建模提供了新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1440, \"height\": 393, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 730, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1443, \"height\": 563, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1453, \"height\": 371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 684, \"height\": 226, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 716, \"height\": 456, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 673, \"height\": 224, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1448, \"height\": 531, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 649, \"height\": 203, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 654, \"height\": 208, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 645, \"height\": 204, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 647, \"height\": 213, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 646, \"height\": 203, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 611, \"height\": 203, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 640, \"height\": 203, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 615, \"height\": 205, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1175, \"height\": 1007, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1173, \"height\": 1008, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ioxn68lbjo/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1464, \"height\": 1076, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1160, \"height\": 436, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1433, \"height\": 511, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1438, \"height\": 248, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1144, \"height\": 295, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1143, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1444, \"height\": 438, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1447, \"height\": 868, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1442, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1150, \"height\": 386, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1148, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1143, \"height\": 323, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1432, \"height\": 1632, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1440, \"height\": 1568, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1341, \"height\": 1923, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ioxn68lbjo/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1342, \"height\": 1924, \"label\": \"Table\"}]"
motivation: 传统时序分解在推理时引入额外计算，降低效率，且难以与预测模型深度融合。
method: 提出隐式分解概念，设计DecompNet框架，将分解知识注入模型，实现不显式分解的预测增强。
result: 在多个数据集上，DecompNet显著提升基模型的预测性能，且无额外推理开销。
conclusion: DecompNet为时序预测提供了一种高效增强方案，兼顾性能与效率，具有广泛适用性。
---

## Abstract
In this paper, we pioneer the idea of implicit decomposition. And based on this idea, we propose a powerful decomposition-based enhancement framework, namely DecompNet. Our method converts the time series decomposition into an implicit process, where it can give a time series model the decomposition-related knowledge during inference, even though this model does not actually decompose the input time series. Thus, our DecompNet can enable a model to inherit the performance promotion brought by time series decomposition but will not introduce any additional inference costs, successfully enhancing the model performance while enjoying better efficiency. Experimentally, our DecompNet exhibits promising enhancement capability and compelling framework generality. Especially, it can also enhance the performance of the latest and state-of-the-art models, greatly pushing the performance limit of time series forecasting. Through comprehensive comparisons, DecompNet also shows excellent performance and efficiency superiority, making the decomposition-based enhancement framework surpass the well-recognized normalization-based frameworks for the first time. Code is
available at this repository: https://github.com/luodhhh/DecompNet.

---

## 论文详细总结（自动生成）

好的，以下是根据您提供的论文内容生成的详细中文总结。

### 1. 论文的核心问题与整体含义

-   **研究背景**：时间序列预测在交通、能源等领域应用广泛。为了提升模型性能，模型无关的增强框架成为了研究热点。
-   **核心问题**：传统的时序分解方法能有效处理非平稳性，但因需要**显式**分解输入序列并维护多个专家模型（如季节性和趋势性模型），导致严重的推理效率低下（计算量和内存占用翻倍），不适合作为轻量级的增强框架。当前主流框架仍集中在基于归一化的方法。
-   **整体含义**：本文开创性地提出了**隐式分解**思想，旨在将分解知识注入单个模型，使其在推理时不实际分解序列，却能继承显式分解带来的性能提升，从而完美平衡性能与效率。

### 2. 论文提出的方法论

-   **核心思想**：将时间序列分解从一个显式的数据预处理和双模型推理过程，转变为一个隐式的模型知识注入过程。
-   **关键技术1：“先解耦后融合”的多阶段训练**
    -   **预训练阶段**：对于给定的待增强模型，创建两个副本，分别在分解出的季节性和趋势性数据上进行预训练，使其成为两个专家模型。
    -   **解耦训练策略**：提出将整体序列预测任务解耦为独立的季节性预测和趋势性预测任务。该方法通过分别计算季节性预测损失 `Ls = ‖Ŷs − Ys‖²₂` 和趋势性预测损失 `Lt = ‖Ŷt − Yt‖²₂`，为两个专家模型提供更直接和清晰的监督信号，从而更充分地发挥分解潜力并加速收敛。
    -   **融合阶段**：使用**季节性-趋势重参数化**技术将两个预训练的专家模型融合为单一模型，将其中的分解知识合并，得到增强后的模型。
-   **关键技术2：季节性-趋势重参数化**
    -   **目标**：将双模型显式分解的推理过程 `Ŷ = XsWs + XtWt` ，转换为单模型隐式处理的推理过程 `Ŷ = X(Ws + λWt) = XW` ，从而消除推理时的额外开销。
    -   **实现方式**：
        1.  基于 `X = Xs + Xt` 的可合并性，引入可学习的**融合因子λ**。
        2.  构造一个概念上的训练结构，让 `Ws` 和 `Wt` 直接接收原始序列 `X`，并以 `λ` 权重求和输出，进行额外训练以学习最优 `λ`。
        3.  训练完成后，通过 `W = Ws + λWt` 合并参数，仅部署参数为 `W` 的单个模型进行推理。
    -   **推广**：该方法可推广至卷积层和更复杂的模型，前提是需要融合的模型具有相同的架构（本文中专家模型是同一原始模型的两个副本，故满足该前提）。

### 3. 实验设计

-   **数据集/场景**：在8个主流的真实世界基准数据集上进行长期时间序列预测实验，包括 **Weather、Traffic、ECL、Solar-Energy** 以及 **ETTh1、ETTh2、ETTm1、ETTm2**。
-   **基线对比**
    -   **主实验(4.1节)**：以5种代表性的SOTA预测模型作为基模型，包括 Transformer 类（PatchTST, iTransformer）、MLP 类（RLinear, RMLP）和卷积类（ModernTCN），验证 DecompNet 对各类先进模型的增强能力。
    -   **框架对比(4.2节)**：与多种主流增强框架（归一化类：Dish-TS, SAN, FAN；先验类：SparseTSF, CycleNet）在性能、泛化能力、效率和鲁棒性上进行了全面比较。
    -   **方法论对比(4.3节)**：与最新的显式分解方法（MICN, Leddam）进行对比，并进行了组件级分析，探究其性能优势的来源。

### 4. 资源与算力

-   **有明确说明**：论文在附录C中提到，所有深度学习网络均使用 PyTorch 实现，并在 **NVIDIA A100 40GB GPU** 上进行实验。
-   **无详细说明**：文中未提及具体的训练总时长或使用的GPU数量。

### 5. 实验数量与充分性

-   **实验组数**：
    -   **主增强实验**：在5个基模型 × 8个数据集 × 4种预测长度上进行了性能评估，并报告了完整的误差棒。
    -   **框架对比实验**：使用2种基模型，对比了5种增强框架，从性能、效率、框架泛化能力、输入长度鲁棒性等多个维度展开。
    -   **显式分解对比实验**：对比了2种显式分解方法，并进行了逐步修改的组件分析。
    -   **消融实验**：验证了“解耦训练策略”和“季节性-趋势重参数化”两个核心设计的有效性。
    -   **其他**：还包括参数敏感性分析、训练效率分析、非平稳数据集上的鲁棒性验证、对新分解形式的拓展实验等。
-   **充分性与公平性**：实验设计**非常充分、客观且公平**。覆盖了多种基模型和数据集，对比了领域内最新的同类方法，严格遵守了主流实验协议（如固定输入长度、公开数据集划分），并汇报了多次运行的误差棒，确保了结果的可信度。

### 6. 论文的主要结论与发现

-   **卓越的增强能力**：DecompNet 能一致性地大幅提升所有基模型（含SOTA模型）的性能（如Solar数据集上平均MSE提升8.0%），并**在不引入任何额外推理成本**的情况下推高了时序预测的性能上限。
-   **全面的优越性**：与现有增强框架相比，DecompNet 在性能和效率上均达到**最优**，且是**首个让分解类框架性能超越公认的归一化类框架的方法**。它能有效增强归一化方法所不能的强大基模型。
-   **方法论创新**：
    1.  证明了**隐式分解优于显式分解**。
    2.  揭示了**更好的训练策略（解耦训练）**比更复杂的数据处理更重要，是释放分解方法潜力的关键。
    3.  挑战了“专家模型必须采用不同架构”的传统观念，发现使用相同架构配合解耦训练同样有效，为重参数化融合铺平了道路。

### 7. 优点

-   **方法论创新性强**：首创“隐式分解”概念，将模型增强从数据操作层面提升到知识注入层面，提供了解决问题的新范式。
-   **完美平衡性能与效率**：这是该工作最突出的亮点。该框架可以显著提升预测精度，同时保证推理过程的计算量和速度与原始模型**完全相同**，具有极高的实用价值。
-   **框架通用性好**：可无缝应用于 Transformer、MLP、卷积等不同架构的预测模型，展现了强大的模型无关性。
-   **实验全面扎实**：对比实验广泛，与多个强基线比较，并通过消融研究和组件分析深刻阐明了其优越性的来源，结论具有说服力。

### 8. 不足与局限

-   **分解方法较为基础**：论文主要采用“季节-趋势”的二分解模式，并结合了主流的移动平均法。作者也指出了未来可探索与更先进的分解方法（如STL）和多成分分解结合。
-   **模型融合存在前提条件**：当前的季节性-趋势重参数化技术要求两个专家模型具有**完全相同**的架构，这虽然在使用原始模型副本时成立，但限制了其融合不同架构模型的能力。
-   **缺乏更深层的理论分析**：论文指出主要通过详尽的实证来验证其有效性，并提到对模型融合进行更深入的理论解释是未来的工作方向。
-   **应用场景限制**：该方法的有效性依赖于序列具备可分离的季节性和趋势性成分假设，对于此假设不成立的序列（如纯随机游走），其增强效果可能有局限性，但论文未对此进行深入讨论。

（完）
