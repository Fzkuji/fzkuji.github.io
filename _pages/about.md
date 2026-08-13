---
permalink: /
title: "Welcome"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hello and welcome to my personal homepage! My name is Zichuan Fu, and I am thrilled to share my educational background and aspirations with you.

<div class="edu-row">
  <div class="edu-card">
    <img src="/images/education/cityu.jpg" alt="City University of Hong Kong">
    <div class="edu-card__text">
      <strong>City University of Hong Kong</strong>
      <span>Ph.D. in Data Science · 2023 – present</span>
    </div>
  </div>
  <div class="edu-card">
    <img src="/images/education/sheffield.jpg" alt="University of Sheffield">
    <div class="edu-card__text">
      <strong>University of Sheffield</strong>
      <span>M.Sc. Advanced Computer Science · 2021 – 2022</span>
    </div>
  </div>
  <div class="edu-card">
    <img src="/images/education/xjtu.jpg" alt="Xi'an Jiaotong University">
    <div class="edu-card__text">
      <strong>Xi'an Jiaotong University</strong>
      <span>B.Eng. Software Engineering · 2017 – 2021</span>
    </div>
  </div>
</div>

I completed my undergraduate studies at Xi'an Jiaotong University's School of Software Engineering, where I earned my Bachelor of Engineering degree. I was fortunate to be mentored by Professor [Jiakun Zhao](http://gr.xjtu.edu.cn/web/zhaojk) during my time there. Following my undergraduate education, I pursued a Master of Science degree in Advanced Computer Science at the University of Sheffield. There, I had the pleasure of working under the guidance of Dr. [Anton Ragni](https://www.sheffield.ac.uk/dcs/people/academic/anton-ragni).

I am now excited to embark on my journey as a Ph.D. candidate at City University of Hong Kong, under the supervision of Professor [Xiangyu Zhao](https://zhaoxyai.github.io/).

As a passionate advocate for artificial general intelligence (AGI), I am eager to contribute my efforts to help bring this revolutionary technology to fruition. I firmly believe that AGI has the potential to reshape our world for the better, and I am committed to playing an active role in its development. Thank you for visiting my page and learning more about my background and aspirations.

## Research

My work centres on **making LLM agents reliable enough to trust with real tasks**. Current
agent frameworks hand the model the role of orchestrator, and then treat the resulting
token explosion, control-flow hallucination, and unreliable stopping as bugs to be
prompt-engineered away. I argue these are architectural consequences of asking a
probabilistic system to do deterministic work, and that the fix is structural.

That line of work runs through three connected threads:

- **Agentic Programming** — putting control flow back in the program and invoking the
  model only where a task calls for judgement
  ([LLM-as-Code](/publication/2026-06-14-LLM-as-Code), KDD'26 AgenticSE Workshop;
  implemented in [OpenProgram](https://openprogram.io/), with a
  [project page](/portfolio/1-openprogram)).
- **Grounded interaction** — letting agents act in real interfaces through active visual
  observation rather than one-shot prediction
  ([GUI-Lens](/publication/2026-08-04-GUI-Lens); [GUI-Agent-Harness](/portfolio/2-gui-agent-harness),
  79.8% on OSWorld Multi-Apps).
- **Efficient and well-behaved attention** — what models spend their context on, and why
  they misallocate it ([Lazy Attention](/publication/2026-01-02-Lazy-Attention),
  [SWAT](/publication/2025-02-26-SWAT)).

Alongside these I work on model merging and knowledge editing, temporal and multi-hop
reasoning, and LLMs for recommendation. Code for most projects is on
[GitHub](https://github.com/Fzkuji).
