---
title: "Ensemble-Hub — Tandem: Collaborative LLM–SLM Reasoning"
collection: talks
type: "Open-source project (code for Tandem, ACL 2026 Findings)"
permalink: /talks/2026-04-14-ensemble-hub-tandem
venue: "GitHub"
date: 2026-04-14
header:
  teaser: "talks/ensemble-hub.jpg"
location: "github.com/Fzkuji/Ensemble-Hub"
link: "https://github.com/Fzkuji/Ensemble-Hub"
excerpt: 'Reference implementation of Tandem (ACL 2026 Findings): a mentor–intern framework where an LLM emits compact GPRA reasoning insights to guide an efficient SLM, with cost-aware termination and progressive effort levels. ~40% cost reduction; +2.56% accuracy over a standalone 32B LLM at 59% of its compute on MATH.'
---

Ensemble-Hub is the reference implementation of **Tandem** (ACL 2026 Findings), a collaborative LLM–SLM reasoning framework. The LLM acts as a strategic mentor, generating compact reasoning insights with the GPRA schema (Goal, Planning, Retrieval, Action), while a smaller, more efficient SLM executes the full reasoning. A lightweight cost-aware classifier decides when sufficient guidance has accumulated, enabling early stopping, and three progressive effort levels (low / medium / high) allocate deeper support only to harder problems. Classifiers trained on mathematical reasoning transfer to code generation without retraining. On MATH, Tandem achieves +2.56% accuracy over a standalone 32B LLM while using only 59% of its compute, with roughly 40% overall cost reduction, and works with both open-source (DeepSeek) and API models (GPT-4o).
