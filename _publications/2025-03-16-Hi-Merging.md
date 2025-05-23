---
title: "Training-free LLM Merging for Multi-task Learning"
collection: publications
category: conferences
permalink: /publication/2025-03-16-Hi-Merging
excerpt: 'Hi-Merging: a training-free method that merges specialized LLMs into a unified multi-task model using hierarchical pruning and scaling, preserving individual strengths while minimizing parameter conflicts across languages and tasks.'
date: 2025-03-16
venue: 'ACL’25, Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics'
paperurl: ''
citation: >-
  
---

Large Language Models (LLMs) have demonstrated exceptional capabilities across diverse natural language processing (NLP) tasks.
The release of open-source LLMs like LLaMA and Qwen has triggered the development of numerous fine-tuned models tailored for various tasks and languages. In this paper, we explore an important question: is it possible to combine these specialized models to create a unified model with multi-task capabilities.
We introduces Hierarchical Iterative Merging (Hi-Merging), a training-free method for unifying different specialized LLMs into a single model.
Specifically, Hi-Merging employs model-wise and layer-wise pruning and scaling, guided by contribution analysis, to mitigate parameter conflicts.
Extensive experiments on multiple-choice and question-answering tasks in both Chinese and English validate Hi-Merging's ability for multi-task learning. 
The results demonstrate that Hi-Merging consistently outperforms existing merging techniques and surpasses the performance of models fine-tuned on combined datasets in most scenarios. 
Code is available at [Applied-Machine-Learning-Lab/Hi-Merging](https://github.com/Applied-Machine-Learning-Lab/Hi-Merging.git).


