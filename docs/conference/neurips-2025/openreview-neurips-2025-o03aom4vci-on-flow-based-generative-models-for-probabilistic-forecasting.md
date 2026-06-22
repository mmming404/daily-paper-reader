---
title: On Flow-based Generative Models for Probabilistic Forecasting
title_zh: 基于流的生成模型用于概率预测
authors: "Edmond Cunningham, Madalina Fiterau, Daniel Sheldon"
date: 2025-05-11
pdf: "https://openreview.net/pdf?id=o03aOm4Vci"
tags: ["query:ts-forecast"]
score: 10.0
evidence: 用于概率预测的基于流的生成模型
tldr: 基于流的生成模型在其他领域取得巨大成功，但在自回归概率预测中应用受限。本文分析这一方法差距，将流模型关键要素推广到时间序列场景，提出一种更实用的算法。理论表明基于线性随机微分方程的流模型具有特定结构，实验验证了其在概率预测任务上的有效性，为生成式时序预测提供了新工具。
source: NeurIPS-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-o03aom4vci/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1276, \"height\": 423, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-o03aom4vci/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 992, \"height\": 338, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-o03aom4vci/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 281, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-o03aom4vci/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 290, \"label\": \"Table\"}]"
motivation: 流模型在概率预测中未得到充分应用，直接方法实践困难。
method: 将流模型要素推广到时序域，设计实用算法，并与线性SDE建立联系。
result: 所提方法在概率预测基准上表现优异，证明了流模型的有效性。
conclusion: 该工作填补了流模型在时序概率预测中的空白，提供了新范式。
---

## Abstract
Flow-based generative models (FBGM) have emerged as a dominant approach to generative modeling in many domains for their scalability and controllability, but have notably not made the same impact on autoregressive probabilistic forecasting.  Although the methodology behind these models can be applied directly to the time series setting, and in theory offers the potential to apply the advances in generative modeling to time series, this direct approach is difficult to use in practice.  In this work, we investigate this methodological gap by generalizing the key elements of flow-based generative modeling to the time series setting to devise a more practical related algorithm.  We show that FBGMs based on linear stochastic differential equations are instances of a more general mean-field variational inference algorithm for conditional exponential family distributions that constructs Bayes estimators of natural parameters.  This insight yields a family of mean-squared error based latent probabilistic forecasters that contains a discrete time counterpart of FBGMs for time series.  We demonstrate that the models we develop inherit the convenient theoretical properties of FBGMs while being easy to work with in practice.

---

## 论文详细总结（自动生成）

好的，以下是根据您提供的论文内容撰写的详细中文总结。

### 1. 论文的核心问题与整体含义

- **核心问题**：基于流的生成模型在图像生成等领域取得了巨大成功，但在自回归概率预测中并未产生同等影响。尽管该方法论在理论上可直接应用于时间序列，但在实践中存在严重的数值困难，例如需要模拟跨长时间域且动力学可能不平滑的随机微分方程。
- **研究动机**：填补流模型在时间序列预测中的方法与实践差距。论文旨在将流模型的关键构建要素推广到时序场景，开发一种更具实用性的相关算法。
- **整体含义**：这项工作揭示了基于线性SDE的流模型是一种更一般的、针对条件指数族分布的变分推断算法的特例。这一见解催生了一族基于均方误差的潜在概率预测器，它们继承了流模型的便利理论属性，同时易于在实践中使用。

### 2. 论文提出的方法论

论文的核心思想是构建一种在理论基础上与流模型等价，但在计算上更为便捷的离散时间预测模型。其技术路径包含三个关键步骤的推广：

- **广义线性随机插值**：
    - 将流模型中的“随机插值”推广到时间序列。通过在高斯条件随机场上引入高斯势函数，来放松线性随机微分方程的端点条件。
    - 构建了一个在用户定义的离散时间点集上，以观测序列为条件的、联合高斯分布的潜在变量序列$\mathbf{x}$。
    - 利用线性时不变SDE的转移分布和高斯势函数，通过消息传递算法，高效地进行推断和采样。

- **约束平均场变分推断**：
    - 这是论文的主要贡献。论文证明，流模型的核心步骤（如马尔可夫投影）是更一般的“约束平均场变分推断”在特定情况下的解。
    - 给定一个包含隐变量$\mathbf{x}$、观测$\mathbf{z}$和仅在训练时可用的参数$\theta$的条件指数族分布$p(\mathbf{x}|\mathbf{z}, \theta)$，CMFVI的目标是找到$p(\mathbf{x}|\mathbf{z})$的一个变分近似$q^*(\mathbf{x}|\mathbf{z})$。
    - 该变分问题的解具有闭式形式：$q^*(\mathbf{x}|\mathbf{z}) = p(\mathbf{x}|\mathbf{z}, \theta^*(\mathbf{z}))$，其中$\theta^*(\mathbf{z}) = E_{p(\theta|\mathbf{z})}[\theta]$是$\theta$的贝叶斯估计量。这个估计量可以通过均方误差最小化来学习。

- **构建离散时间模型**：
    - 通过将CMFVI框架应用于潜在预测分布的自回归因子，论文推导出一族基于MSE的离散时间模型。
    - **朴素CMFVI模型 ($q_{MSE}$)**：直接预测所有未来隐变量的高斯势函数均值，这与非概率性MSE预测器等价。
    - **自回归CMFVI模型 ($q_{MSE-AR}$)**：对自回归转移分布进行近似。其转移核形式为：$q_{transition}(\mathbf{x}_{t_k} | \mathbf{x}_{t_{1:k-1}}, \mathbf{y}_O) \propto \phi_{t_k|t_{k-1}}(\mathbf{x}_{t_k}|\mathbf{x}_{t_{k-1}})\phi(\mathbf{x}_{t_k}|\beta^*_{t_k}(\mathbf{x}_{t_{1:k-1}}, \mathbf{y}_O))$。
        -  这里$\beta^*_{t_k}$是后向消息的贝叶斯估计量，其协方差矩阵与观测值无关，可由消息传递算法预先计算，模型只需学习其均值。
    - **连续时间模型 ($q_{Neural-SDE}$)**：论文的离散模型$q_{MSE-AR}$被视为连续时间马尔可夫投影SDE ($q_{Neural-SDE}$)的离散对应物。两者的核心区别仅在于贝叶斯估计器的条件依赖不同，前者依赖于离散时间点的历史隐状态，后者则依赖于当前连续时间状态$\mathbf{x}_t$。

### 3. 实验设计

- **数据集/场景**：在6个模拟的动态系统数据集上进行潜在概率预测实验。这些系统包括：Brusselator, Double Pendulum, FitzHugh-Nagumo, Lorenz, Lotka-Volterra, Van der Pol。数据包含对动态系统的带噪声观测。
- **任务 benchmark**：任务是概率预测，即基于观测到的序列部分 $\mathbf{y}_O$，生成对未来潜在状态 $\mathbf{x}_{t_{k+1:N}}$ 的预测分布。
- **对比方法**：
    - 论文提出的模型：**MSE** ($q_{MSE}$) 和 **AR-MSE** ($q_{MSE-AR}$)。
    - 基线模型：
        - **AR-MLE**：最大化似然训练的条件高斯自回归模型，分别在**潜在空间**和**观测空间**训练。
        - **FBGM**：使用流匹配训练的非自回归流模型，同样在**潜在空间**和**观测空间**训练。
- **评价指标**：
    - 负对数似然 (Negative Log Likelihood, NLL)：评估概率预测质量（越低越好）。
    - 归一化均方根误差 (Normalized Root Mean Squared Error, NRMSE)：评估点预测的准确性（越低越好）。
- **模型细节**：所有模型均使用一层GRU的循环神经网络作为骨干网络。

### 4. 资源与算力

- **算力资源**：论文明确指出，所有模型均在**单个RTX 3080 Ti GPU**上进行训练。
- **训练配置**：使用AdamW优化器，学习率为$10^{-4}$，包含1000步的线性预热，有效批次大小为256（通过批次大小64和4步梯度累积实现）。
- **训练时长**：文中未明确提及每个模型在特定数据集上的具体训练时长，仅描述了早停策略（每1000步评估一次验证集，若5次评估无改善则停止）。

### 5. 实验数量与充分性

- **实验组数**：在6个不同的动态系统数据集上，分别训练和评估了6种不同的模型配置（2种提出模型+4种基线模型），并使用**5个不同的随机种子**进行重复实验，以减少随机性影响。
- **充分性评估**：
    - **客观性**：实验报告了均值和标准差，保证了结果的统计可靠性。
    - **公平性**：所有模型均使用几乎完全相同的神经网络架构和训练流程，确保了对比的公平性。
    - **局限性**：实验仅限于低维的模拟动态系统，未在更复杂、更高维的真实世界基准数据集上进行验证，实验的广度和外部泛化性有待进一步检验。此外，基线模型之一的FBGM本质上是非自回归模型，与论文提出的自回归模型进行直接比较，可能不完全对等。

### 6. 论文的主要结论与发现

- **理论统一性**：论文建立了流模型、均方误差预测器和条件高斯模型之间的理论联系，揭示了它们在CMFVI框架下的统一性。
- **模型性能**：
    - 提出的AR-MSE模型在大多数数据集上取得了最低的负对数似然，表明其概率预测质量优于对比的MLE和流模型基线，尤其是在Brusselator、Lotka和Van der Pol系统上。
    - 在NRMSE指标上，AR-MSE在多个数据集上也表现出色。简化的MSE预测器在点预测上也能获得有竞争力的结果。
    - 在潜在空间训练的基线模型（AR-MLE, FBGM）通常优于在观测空间训练的版本。
- **离散vs连续**：AR-MSE模型（被视为连续模型的离散版本）在实践中表现良好。论文推测，在数据采样足够频繁的时间序列场景中，连续模型$q_{Neural-SDE}$相较于$q_{MSE-AR}$的额外建模能力可能影响甚微，这使得离散模型在实用性和性能上成为一个极具吸引力的选择。

### 7. 优点

- **理论创新**：提出了约束平均场变分推断框架，为理解流模型、MSE预测器和条件高斯模型之间的关系提供了深刻见解。
- **方法实用性**：所提出的离散时间模型避免了模拟神经SDE的数值困难，在训练和采样上更加稳定高效，同时保留了流模型的理论根基。
- **算法全面性**：论文不仅提出了算法，还详细给出了基于消息传递的并行推断实现方案，增强了方法的可扩展性。
- **可解释性强**：模型的不确定性仅依赖于时间间隔而非观测值，结构清晰，易于理解。

### 8. 不足与局限

- **实验范围有限**：
    - **数据集局限**：仅在6个低维合成动态系统上进行了验证，缺乏在真实世界、高维时间序列预测任务（如天气、交通、金融）上的评估，这削弱了其实用性的说服力。
    - **基线比较**：对比的FBGM是非自回归模型，而论文重点是自回归预测，类比可能不完全公平。未与主流的先进时序扩散/流模型进行更充分的对比。
- **模型假设限制**：
    - CMFVI解的最优性建立在$\mathbf{x}$和$\theta$在给定$\mathbf{z}$时条件独立的强假设上，这在实际中可能不成立，导致模型偏差。
    - 模型的协方差矩阵被假设为与观测值无关，这限制了其表达复杂不确定性的能力。本质上，这是用MSE损失训练的模型，可能在某些高度随机的任务中不如使用似然函数训练的模型。
- **潜在应用限制**：论文承认，只有当潜在过程不太随机，或预测步长足够短、历史信息足够长时，CMFVI近似才可能是合理的。

（完）
