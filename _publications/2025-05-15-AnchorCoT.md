---
title: "AnchorCoT: Anchors Pave the Way for Multi-hop Reasoning"
collection: publications
category: conferences
permalink: /publication/2025-05-15-AnchorCoT
excerpt: 'AnchorCoT predicts key entities as "anchors" to guide multi-hop reasoning and uses a ranking algorithm to ensure logical answer sequences, improving LLM performance on multi-hop QA.'
date: 2025-05-15
header:
  teaser: "publications/anchorcot.jpg"
venue: 'ACL’25 Findings, Findings of the Association for Computational Linguistics'
authors: "Tianshi Ming, Xian Wu, Yingying Zhang, Zichuan Fu, Dawei Cheng"
paperurl: 'https://doi.org/10.18653/v1/2025.findings-acl.801'
paperlabel: "10.18653/v1/2025.findings-acl.801"
---

Large Language Models (LLMs) have made substantial strides in a broad array of natural language tasks. Recently, LLMs have demonstrated potential reasoning capabilities through prompt design, such as the Chain of Thought (CoT). Despite their superiority in question answering, LLMs still face challenges in answering questions that require multi-hop reasoning, often generating unreliable reasoning chains during answer generation. To improve LLMs' performance in multi-hop reasoning, we introduce a novel reasoning approach, AnchorCoT, designed to assist LLMs in answering questions involving complex logical reasoning steps. AnchorCoT first predicts key entities which work as important "anchors" to guide the reasoning process and then employs a novel ranking algorithm to ensure the logical sequence of the predicted answers. We implement AnchorCoT on Qwen2.5-7B/14B and GPT-4o and evaluate our method on widely used multi-hop reasoning datasets, including HotpotQA, 2WikiMultiHopQA, and MuSiQue-Ans. The experimental results show that AnchorCoT outperforms existing methods in multi-hop question reasoning and provides more accurate reasoning results in multi-hop question answering tasks.
