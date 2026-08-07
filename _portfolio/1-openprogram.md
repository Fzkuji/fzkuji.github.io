---
title: "OpenProgram — Open-Source Agent Harness"
excerpt: "The reference implementation of Agentic Programming: write an agent as an ordinary Python function, where the docstring is the prompt and every LLM call is a node on a shared execution DAG.<br/><a href='https://github.com/Fzkuji/OpenProgram'>github.com/Fzkuji/OpenProgram</a>"
collection: portfolio
---

**[github.com/Fzkuji/OpenProgram](https://github.com/Fzkuji/OpenProgram)** · AGPL-3.0 · Python 3.11+ · macOS / Linux / Windows

The reference implementation of the *Agentic Programming* paradigm introduced in
[LLM-as-Code](/publication/2026-06-14-LLM-as-Code) (KDD'26 AgenticSE Workshop).

![One decorator turns a Python function into an agent: the docstring becomes the system prompt, type annotations become the tool schema, runtime.exec() calls become retryable DAG nodes, and plain if/for/return stays deterministic](/images/portfolio/openprogram-agentic-function.jpg)

Most agent frameworks make the LLM the orchestrator. OpenProgram inverts that: the
Python program governs control flow, and the model is invoked only where a task
genuinely calls for judgement.

```python
@agentic_function
def triage(ticket: str, runtime=None) -> str:
    """Classify the ticket as bug / feature / question, then draft a reply."""
    kind = runtime.exec(ticket, choices=["bug", "feature", "question"])
    if kind == "bug":
        return runtime.exec(f"Reply using:\n{search_logs(ticket)}")
    return runtime.exec("Draft a short reply.")
```

One decorator binds what every other harness makes you hand-write — the **docstring
becomes the system prompt**, **type annotations become the tool schema**, and plain
`if` / `for` / `return` stays deterministic Python the model cannot skip.

Four mechanisms sit underneath:

- **Agentic Function** — the primitive above; `choices=` is a code gate that sends an
  invalid answer back to be re-decided rather than letting it drift past.
- **DAG Context** — every user turn, LLM call, and function call is one node on a flat
  DAG. Context is an addressable node rather than a per-agent buffer, so forking,
  spawning sub-agents, and cross-session messaging are all "select a different node set".

  ![Every user, LLM, and function call is one node on a single flat DAG, tied by caller and predecessor edges; a branch can spawn a sub-agent on its own lane and attach the result back](/images/portfolio/openprogram-dag-context.jpg)

- **Agentic Workflow** — agents write and hot-load their own `@agentic_function`s with
  ordinary file edits; no `create()` / `fix()` machinery.
- **Event Infrastructure** — one process-wide bus that the agent loop, auth, context,
  channels, and memory all emit onto.

Ships with a web UI, a terminal UI, and a library mode for embedding the engine in
your own stack. Third-party harnesses install with one command.
