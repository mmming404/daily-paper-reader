---
title: "TARFVAE: Efficient One-Step Generative Time Series Forecasting via TARFLOW based VAE"
title_zh: TARFVAE：基于TARFLOW的VAE实现高效一步生成式时间序列预测
authors: "Jiawen Wei, Lan Jiang, Pengbo Wei, Ziwen Ye, Teng Song, Chen Chen, Guangrui Ma"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=3hnqwOq7iT"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 提出TARFVAE，一步式生成VAE用于高效概率时间序列预测
tldr: TARFVAE 针对现有生成式时间序列预测方法反复生成或去噪步骤导致效率低、不适合长期预测的问题，提出基于TARFLOW的一步VAE模型，实现快速且有效的长期概率预测。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-3hnqwoq7it/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1421, \"height\": 580, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-3hnqwoq7it/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 746, \"height\": 410, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-3hnqwoq7it/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1380, \"height\": 326, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-3hnqwoq7it/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 1135, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-3hnqwoq7it/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1442, \"height\": 464, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-3hnqwoq7it/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 731, \"height\": 772, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-3hnqwoq7it/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1370, \"height\": 530, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-3hnqwoq7it/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 730, \"height\": 300, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-3hnqwoq7it/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1383, \"height\": 147, \"label\": \"Table\"}]"
motivation: 现有生成式方法预测过程冗长，尤其长期预测效率低且实际优势不明。
method: 基于TARFLOW的VAE实现一步生成，避免多步迭代。
result: 在长期预测任务上表现优于现有生成式方法，且与确定性方法相比有竞争力。
conclusion: 一步生成显著提升效率，揭示了生成式时序预测在长期预测中的实践潜力。
---

## Abstract
Time series data is ubiquitous, with forecasting applications spanning from finance to healthcare. Beyond popular deterministic methods, generative models are gaining attention due to advancements in areas like image synthesis and video generation, as well as their inherent ability to provide probabilistic predictions. However, existing generative approaches mostly involve recurrent generative operations or repeated denoising steps, making the prediction laborious, particularly for long-term forecasting. Most of them only conduct experiments for relatively short-term forecasting, with limited comparison to deterministic methods in long-term forecasting, leaving their practical advantages unclear. This paper presents TARFVAE, a novel generative framework that combines the Transformer-based autoregressive flow (TARFLOW) and variational autoencoder (VAE) for efficient one-step generative time series forecasting. Inspired by the rethinking that complex architectures for extracting time series representations might not be necessary, we add a flow module, TARFLOW, to VAE to promote spontaneous learning of latent variables that benefit predictions. TARFLOW enhances VAE's posterior estimation by breaking the Gaussian assumption, thereby enabling a more informative latent space. TARFVAE uses only the forward process of TARFLOW, avoiding autoregressive inverse operations and thus ensuring fast generation. During generation, it samples from the prior latent space and directly generates full-horizon forecasts via the VAE decoder. With simple MLP modules, TARFVAE achieves superior performance over state-of-the-art deterministic and generative models across different forecast horizons on benchmark datasets while maintaining efficient prediction speed, demonstrating its effectiveness as an efficient and powerful solution for generative time series forecasting. Our code is available at https://github.com/Gavine77/TARFVAE.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
提出TARFVAE，一步式生成VAE用于高效概率时间序列预测。

### 2. 核心内容
TARFVAE 针对现有生成式时间序列预测方法反复生成或去噪步骤导致效率低、不适合长期预测的问题，提出基于TARFLOW的一步VAE模型，实现快速且有效的长期概率预测。

### 3. 对应检索需求
generative models for time series forecasting。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=3hnqwOq7iT](https://openreview.net/forum?id=3hnqwOq7iT)
