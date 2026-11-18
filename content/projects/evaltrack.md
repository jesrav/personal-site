---
title: "evaltrack"
weight: 10
lead: "A pytest plugin that gates and tracks your evals, and handles LLM flakiness without rerunning CI."
links:
  - name: Docs
    url: "https://evaltrack.jesravnbol.dk/latest/"
  - name: GitHub
    url: "https://github.com/jesrav/evaltrack"
---

I think at least a subset of an agentic application's evals should run and gate in CI, enough to know the main agentic behaviour still works. But LLMs are stochastic, and a single flaky eval means rerunning the whole pipeline.

evaltrack reruns only the evals that fail, tracks each case's pass rate over time, and keeps every run in storage you own, so you can compare a branch to what is deployed. It works with pydantic-evals and DeepEval today.
