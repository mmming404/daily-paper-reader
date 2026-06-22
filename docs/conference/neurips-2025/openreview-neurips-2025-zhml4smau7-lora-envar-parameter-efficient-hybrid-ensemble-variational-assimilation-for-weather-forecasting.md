---
title: "LoRA-EnVar: Parameter-Efficient Hybrid Ensemble Variational Assimilation for Weather Forecasting"
title_zh: LoRA-EnVar：参数高效的混合集变分同化用于天气预报
authors: "Yi Xiao, Hang Fan, Kun Chen, Ye Cao, Ben Fei, Wei Xue, LEI BAI"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=zhMl4Smau7"
tags: ["query:ts-forecast"]
score: 7.0
evidence: 利用LoRA提出参数高效的混合集变分同化方法用于天气预报
tldr: LoRA-EnVar 针对数值天气预报中背景误差估计的挑战，提出一种参数高效的混合方法，将集合与变分同化结合，利用LoRA捕捉非高斯误差，无需手工设计协方差结构。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1401, \"height\": 1044, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1408, \"height\": 363, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1443, \"height\": 840, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1445, \"height\": 842, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1461, \"height\": 567, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1452, \"height\": 758, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1450, \"height\": 579, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1414, \"height\": 607, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1428, \"height\": 600, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1461, \"height\": 2091, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1461, \"height\": 2067, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1461, \"height\": 2065, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1429, \"height\": 1924, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1431, \"height\": 1932, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1430, \"height\": 1960, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1451, \"height\": 1364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-zhml4smau7/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1433, \"height\": 1930, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-zhml4smau7/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1453, \"height\": 336, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zhml4smau7/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1452, \"height\": 354, \"label\": \"Table\"}]"
motivation: 现有混合方法依赖高斯假设和手工协方差设计，无法有效捕获大气复杂的非高斯误差分布。
method: 提出LoRA-EnVar，通过LoRA实现参数效率，融合静态气候协方差与流依赖集合成分的混合集变分同化。
result: 在提升误差估计精度的同时保持计算效率，实验证明优于传统方法。
conclusion: 为数值天气预报同化提供灵活且高效的新思路，有助于推动数据驱动天气预报发展。
---

## Abstract
Accurate estimation of background error (i.e., forecast error) distribution is critical for effective data assimilation (DA) in numerical weather prediction (NWP). In state-of-the-art operational DA systems, it is common to account for the temporal evolution of background errors by employing hybrid methods, which blend a static climatological covariance with a flow-dependent ensemble-derived component. While effective to some extent, these methods typically assume Gaussian-distributed errors and rely heavily on hand-crafted covariance structures and domain expertise, limiting their ability to capture the complex, non-Gaussian nature of atmospheric dynamics. In this work, we propose LoRA-EnVar, a novel hybrid ensemble variational DA algorithm that integrates low-rank adaptation (LoRA) into a deep generative modeling framework. We first learn a climatological background error distribution using a variational autoencoder (VAE) trained on historical data. To incorporate flow-dependent uncertainty, we introduce LoRA modules that efficiently adapt the learned distribution in response to flow-dependent ensemble perturbations. Our approach supports online finetuning, enabling dynamic updates of the background error distribution without catastrophic forgetting. We validate LoRA-EnVar in high-resolution assimilation settings using the FengWu forecast model and simulated observations from ERA5 reanalysis. Experimental results show that LoRA-EnVar significantly improves assimilation accuracy over models assuming static background error distribution and achieves comparable or better performance than full finetuning while reducing the number of trainable parameters by three orders of magnitude. This demonstrates the potential of parameter-efficient adaptation for scalable, non-Gaussian DA in operational meteorology.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
利用LoRA提出参数高效的混合集变分同化方法用于天气预报。

### 2. 核心内容
LoRA-EnVar 针对数值天气预报中背景误差估计的挑战，提出一种参数高效的混合方法，将集合与变分同化结合，利用LoRA捕捉非高斯误差，无需手工设计协方差结构。

### 3. 对应检索需求
innovative model architectures for time series forecasting。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=zhMl4Smau7](https://openreview.net/forum?id=zhMl4Smau7)
