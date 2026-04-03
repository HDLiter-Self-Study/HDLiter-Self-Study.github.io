---
title: Artificial Intelligence
date: 2026-04-02
lastmod: 2026-04-02
tags:
  - ai
  - roadmap
draft: false
---

## Structure

```
Machine Learning ──→ Deep Learning ──→ Applications
       ↑                   ↑
  Math foundations    Reinforcement Learning
```

### Core
- [[ai/machine-learning/index|Machine Learning]] — learning theory + classical methods + optimization (6 phases)
- [[ai/deep-learning/index|Deep Learning]] — theory + architectures + generative models + LLM (5 phases)
- [[ai/reinforcement-learning/index|Reinforcement Learning]] — MDPs + deep RL + RLHF + theory (4 phases)

### Mathematical Foundations
- [[mathematics/linear-algebra/index|Linear Algebra]] · [[mathematics/probability/index|Probability Theory]] · [[mathematics/analysis/index|Real Analysis]] · [[mathematics/information-theory/index|Information Theory]]

### Applications (future)
- `applications/finance/` — ML + quantitative finance
- `applications/science/` — AI for science

## Dependency Map

```
Linear Algebra ─────────┐
                        ├──→ ML Theory (Phase 1-2) ──→ DL Theory (Phase 1)
Probability Theory ─────┤                                    │
                        ├──→ ML Methods (Phase 3-5) ──→ DL Architectures (Phase 2)
Information Theory ─────┘         │                          │
                                  │                    DL Generative (Phase 3)
Real Analysis ──→ Measure Theory ─┘                          │
                                                       Foundation Models (Phase 4)
                                                             │
RL Foundations ──→ Deep RL ──→ RLHF ─────────────────────────┘
                                │
                          Applications (finance, science, ...)
```
