---
title: "Attention Needs to Focus: A Unified Perspective on Attention Allocation"
collection: publications
category: arxiv
permalink: /publication/2026-01-02-Lazy-Attention
excerpt: 'A unified perspective tracing representational collapse and attention sink to improper attention allocation, introducing Lazy Attention with positional discrimination and Elastic-Softmax for focused attention.'
date: 2026-01-02
venue: 'arXiv preprint arXiv:2601.00919'
paperurl: 'https://arxiv.org/abs/2601.00919'
citation: 'Zichuan Fu, Wentao Song, Guojing Li, Yejing Wang, Xian Wu, Yimin Deng, Hanyu Yan, Yefeng Zheng, and Xiangyu Zhao. 2026. Attention Needs to Focus: A Unified Perspective on Attention Allocation. arXiv preprint arXiv:2601.00919. <a href="https://arxiv.org/abs/2601.00919">arXiv:2601.00919</a>'
---

The Transformer architecture, a cornerstone of modern Large Language Models (LLMs), has achieved extraordinary success in sequence modeling, primarily due to its attention mechanism. However, despite its power, the standard attention mechanism is plagued by well-documented issues: representational collapse and attention sink. Although prior work has proposed approaches for these issues, they are often studied in isolation, obscuring their deeper connection. In this paper, we present a unified perspective, arguing that both can be traced to a common root -- improper attention allocation. We identify two failure modes: 1) Attention Overload, where tokens receive comparable high weights, blurring semantic features that lead to representational collapse; 2) Attention Underload, where no token is semantically relevant, yet attention is still forced to distribute, resulting in spurious focus such as attention sink. Building on this insight, we introduce Lazy Attention, a novel mechanism designed for a more focused attention distribution. To mitigate overload, it employs positional discrimination across both heads and dimensions to sharpen token distinctions. To counteract underload, it incorporates Elastic-Softmax, a modified normalization function that relaxes the standard softmax constraint to suppress attention on irrelevant tokens. Experiments on the FineWeb-Edu corpus, evaluated across nine diverse benchmarks, demonstrate that Lazy Attention successfully mitigates attention sink and achieves competitive performance compared to both standard attention and modern architectures, while reaching up to 59.58% attention sparsity.
