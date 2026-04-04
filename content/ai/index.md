---
title: Artificial Intelligence
date: 2026-04-02
lastmod: 2026-04-03
tags:
  - ai
  - roadmap
draft: false
---

## Career Logic

The immediate target is the **LLM+Finance** domain. The dependency chain:

```
ML Theory (why models generalize) → DL Phase 4 (foundation models, ICL, RAG, agents)
                                              → RL Phase 3 (RLHF, DPO)
                                                        → Finance application
```

The full ML theory roadmap is not a prerequisite for the application layer — it is the foundation that lets you **diagnose failures and extend beyond tutorials**. When motivation dips during abstract theory phases, this is the anchor: every concept here serves the ability to build, debug, and reason about real AI systems.

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

### Applications
- [[finance/index|Finance]] — macro, systematic strategies, LLM + finance
- `applications/science/` — AI for science (future)

## Dependency Map

```
Linear Algebra ─────────┐
                        ├──→ ML Theory (Phase 1-2) ──→ DL Theory (Phase 1)
Probability Theory ─────┤                                    │
                        ├──→ ML Methods (Phase 3-5) ──→ DL Architectures (Phase 2)
Information Theory ─────┘         │                          │
                                  │                    DL Generative (Phase 3)
Real Analysis ──→ Measure Theory ─┘                          │
                                                       Foundation Models (Phase 4) ──→ Finance (LLM + Finance)
                                                             │
RL Foundations ──→ Deep RL (Phase 2) ──→ RLHF (Phase 3) ────┘
                                │
                          Finance (RL for portfolio), AI for science, ...

Key cross-dependencies:
  ML Phase 6 (Online Learning) ──→ RL Phase 4 (bandit theory, regret bounds)
  RL Phase 2 (policy gradient, PPO) ──→ DL Phase 4 RLHF/DPO
  Probability Phase 2+ ──→ RL Phase 2 (importance sampling, policy gradient proofs)
  RL Phase 3 (RLHF) and DL Phase 4 (RLHF) cover the same topic from complementary angles — read together
```
