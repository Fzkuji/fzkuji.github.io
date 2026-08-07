---
title: "GUI-Agent-Harness — Autonomous Desktop Agent"
excerpt: "Give it a task, it operates the desktop by vision. 79.8% on OSWorld Multi-Apps.<br/><a href='https://github.com/Fzkuji/GUI-Agent-Harness'>github.com/Fzkuji/GUI-Agent-Harness</a>"
collection: portfolio
---

**[github.com/Fzkuji/GUI-Agent-Harness](https://github.com/Fzkuji/GUI-Agent-Harness)**

**OSWorld Multi-Apps 79.8%** (72.6/91) · **OSWorld Chrome 93.5%** (43/46)

An autonomous GUI agent: give it a task and it drives real desktop applications and
OSWorld VMs by vision alone — no accessibility tree, no application APIs.

The grounding method behind it is [GUI-Lens](/publication/2026-08-04-GUI-Lens): rather
than asking a vision-language model to predict a click coordinate in one shot, the agent
extracts OCR text and detected UI components as coordinate references, then narrows the
search region through successive observations. This matters on dense, high-resolution
interfaces, where a model often recognizes the control it wants without locating it
precisely enough to click.

Built as an installable harness on top of [OpenProgram](/portfolio/1-openprogram), so the
perception loop is ordinary Python while the model supplies only visual judgement.
