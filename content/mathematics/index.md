---
title: Mathematics
date: 2026-01-14
lastmod: 2026-04-03
tags:
  - mathematics
  - roadmap
draft: false
---

## Overview

Mathematics foundations for AI research and intellectual depth. Organized by concept, not by course — each topic has its own roadmap with textbook mappings and progress tracking.

## Topics

| Topic | Focus | Status |
|-------|-------|--------|
| [[mathematics/logic/index\|Set Theory & Logic]] | FOL, ZFC, incompleteness, computability | Not started |
| [[mathematics/analysis/index\|Real Analysis]] | Sequences, continuity, measure theory, multivariable | Not started |
| [[mathematics/linear-algebra/index\|Linear Algebra]] | Abstract vector spaces, spectral theory, matrix calculus | Not started |
| [[mathematics/probability/index\|Probability Theory]] | Measure-theoretic probability, martingales, statistics | Not started |
| [[mathematics/information-theory/index\|Information Theory]] | Entropy, KL divergence, coding, connections to learning | Not started |

## Recommended Entry Order

```
Logic Phase 0 (FOL) + Analysis Phase 1 (foundations)
         │
    Linear Algebra Phase 1-2
         │
    Analysis Phase 2-3 + Logic Phase 2 (incompleteness, optional)
         │
    Analysis Phase 4 (measure theory) ──→ Probability Phase 1
         │
    Analysis Phase 5 (metric spaces) + Linear Algebra Phase 3-4
         │                │
         │          Probability Phase 2-3 (can run parallel with Analysis Phase 5)
         │                │
    Analysis Phase 6 (multivariable)    Probability Phase 4-5 + Information Theory
```

> Logic Phase 1 (ZFC, ordinals) is optional depth — not on the critical path. Can be deferred until after Analysis Phase 3.
> Probability Phase 4-5 (statistics) depends only on Probability Phase 1-3, not on Analysis Phase 5-6.

See [[mathematics/principles|Mathematics Learning Principles]] for dependency map and AI relevance guide.

## Cross-Subject Links

- [[ai/index|AI roadmap]] — where these foundations are applied
- [[principles|General learning principles]] — cognitive science framework
