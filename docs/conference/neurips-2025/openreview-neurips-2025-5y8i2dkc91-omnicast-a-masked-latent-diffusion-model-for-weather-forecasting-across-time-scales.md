---
title: "OmniCast: A Masked Latent Diffusion Model for Weather Forecasting Across Time Scales"
title_zh: OmniCast：跨时间尺度的掩码潜在扩散模型用于天气预报
authors: "Tung Nguyen, Tuan Pham, Troy Arcomano, Rao Kotamarthi, Ian Foster, Sandeep Madireddy, Aditya Grover"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=5Y8I2dKc91"
tags: ["query:ts-forecast"]
score: 9.0
evidence: 使用掩码潜在扩散模型生成跨时间尺度的概率天气预报
tldr: OmniCast 提出一种统一跨时间尺度的概率天气预报模型，通过VAE编码气象数据到低维空间，再用掩码扩散Transformer生成未来潜变量，克服自回归模型在季节尺度上的误差累积，实现技能化概率预测。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 862, \"height\": 390, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 437, \"height\": 200, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 438, \"height\": 106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1303, \"height\": 930, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1305, \"height\": 619, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1306, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1308, \"height\": 939, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 868, \"height\": 528, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1443, \"height\": 783, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1366, \"height\": 1236, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1366, \"height\": 1223, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1374, \"height\": 985, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1376, \"height\": 985, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1169, \"height\": 735, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1445, \"height\": 1606, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1447, \"height\": 1604, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1444, \"height\": 1605, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1444, \"height\": 1606, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-5y8i2dkc91/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1445, \"height\": 1608, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-5y8i2dkc91/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1235, \"height\": 573, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-5y8i2dkc91/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1260, \"height\": 262, \"label\": \"Table\"}]"
motivation: 现有深度学习方法在中短期预报成功，但在次季节-季节尺度因自回归误差积累表现不佳。
method: 由VAE将天气数据编码到连续低维空间，再使用掩码扩散Transformer生成未来潜变量序列。
result: 实现从短期到季节尺度一致的、技能化的概率预报。
conclusion: 扩散模型框架有效统一多时间尺度预报，增强了不确定性量化能力，对气候适应决策有重要价值。
---

## Abstract
Accurate weather forecasting across time scales is critical for anticipating and mitigating the impacts of climate change. Recent data-driven methods based on deep learning have achieved significant success in the medium range, but struggle at longer subseasonal-to-seasonal (S2S) horizons due to error accumulation in their autoregressive approach. In this work, we propose OmniCast, a scalable and skillful probabilistic model that unifies weather forecasting across timescales. OmniCast consists of two components: a VAE model that encodes raw weather data into a continuous, lower-dimensional latent space, and a diffusion-based transformer model that generates a sequence of future latent tokens given the initial conditioning tokens. During training, we mask random future tokens and train the transformer to estimate their distribution given conditioning and visible tokens using a per-token diffusion head. During inference, the transformer generates the full sequence of future tokens by iteratively unmasking random subsets of tokens. This joint sampling across space and time mitigates compounding errors from autoregressive approaches. The low-dimensional latent space enables modeling long sequences of future latent states, allowing the transformer to learn weather dynamics beyond initial conditions. OmniCast performs competitively with leading probabilistic methods at the medium-range timescale while being 10× to 20× faster, and achieves state-of-the-art performance at the subseasonal-to-seasonal scale across accuracy, physics-based, and probabilistic metrics. Furthermore, we demonstrate that OmniCast can generate stable rollouts up to 100 years ahead. Code and model checkpoints are available at https://github.com/tung-nd/omnicast.

---

## 论文详细总结（自动生成）

### 1. 检索相关性
使用掩码潜在扩散模型生成跨时间尺度的概率天气预报。

### 2. 核心内容
OmniCast 提出一种统一跨时间尺度的概率天气预报模型，通过VAE编码气象数据到低维空间，再用掩码扩散Transformer生成未来潜变量，克服自回归模型在季节尺度上的误差累积，实现技能化概率预测。

### 3. 对应检索需求
Probabilistic and generative forecasting methods with uncertainty quantification techniques。

### 4. 来源与原文
- Source：NeurIPS-2025-Accepted
- OpenReview：[https://openreview.net/forum?id=5Y8I2dKc91](https://openreview.net/forum?id=5Y8I2dKc91)
