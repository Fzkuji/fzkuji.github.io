---
title: "LLM-as-Code: Agentic Programming for Agent Harness"
collection: publications
category: conferences
permalink: /publication/2026-06-14-LLM-as-Code
excerpt: 'Agentic Programming inverts the usual agent design: the program governs all control flow and the LLM is an adaptive component invoked only where reasoning is needed, so token explosion and control-flow hallucination become architecturally impossible rather than prompt-tuned away.'
date: 2026-06-14
header:
  teaser: "publications/llm-as-code.jpg"
venue: 'KDD’26 Workshop on Agentic Software Engineering (AgenticSE)'
authors: "Junjia Qi, Zichuan Fu, Jingtong Gao, Wenlin Zhang, Hanyu Yan, Xian Wu, Xiangyu Zhao"
paperurl: 'https://arxiv.org/abs/2606.15874'
paperlabel: "arXiv:2606.15874"
codeurl: 'https://github.com/Fzkuji/OpenProgram'
---

Every major LLM agent framework gives the LLM the role of orchestrator; the model decides what to do next, when to call tools, and when to stop. We argue that token explosion, control-flow hallucination, and unreliable completion are not implementation bugs but architectural consequences of assigning the deterministic work of looping, branching, and sequencing to a probabilistic system. A better prompt or a stronger model cannot guarantee the reliability of the LLM agent. We therefore propose Agentic Programming, in which the program governs all control flow, and the LLM is itself part of it, an adaptive component we call LLM-as-Code and invoke only where a task calls for reasoning or generation. Within each call the model keeps full flexibility, but it cannot alter the program's execution path. With control in the program, the LLM's context is built from the execution history's call tree rather than an ever-growing transcript, so each call sees only what its scope declares.

The reference implementation is [OpenProgram](https://openprogram.io/), a self-programming AI agent framework in which agents create, execute, and refine programs while deterministic runtime controls keep execution inspectable and reliable. The [source code](https://github.com/Fzkuji/OpenProgram) is available under AGPL-3.0.
