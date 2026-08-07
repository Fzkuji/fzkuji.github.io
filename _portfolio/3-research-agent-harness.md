---
title: "Research-Agent-Harness — Autonomous Research Pipeline"
excerpt: "Literature survey → idea generation → experiments → paper writing → review, as a single programmable pipeline.<br/><a href='https://github.com/Fzkuji/Research-Agent-Harness'>github.com/Fzkuji/Research-Agent-Harness</a>"
collection: portfolio
---

**[github.com/Fzkuji/Research-Agent-Harness](https://github.com/Fzkuji/Research-Agent-Harness)**

An autonomous research agent covering the loop end to end: literature survey → idea
generation → novelty check → experiment design → execution on GPU → paper draft →
review.

Each stage is an `@agentic_function`, so the parts that must be deterministic — running
an experiment, checking a result against its claim, compiling LaTeX — stay ordinary
Python, while the model contributes only the judgement steps. A failed check sends the
stage back rather than letting a weak claim through.

Built on [OpenProgram](/portfolio/1-openprogram).
