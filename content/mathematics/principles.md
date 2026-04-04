---
title: Mathematics Learning Principles
date: 2026-04-02
lastmod: 2026-04-03
tags:
  - mathematics
  - meta-learning
draft: false
---

Domain-specific principles for mathematics. See [[principles|general learning principles]] for the cross-subject cognitive science framework.

## Dependency Map

```
Logic (FOL, completeness, compactness)
  │
  ├── Set Theory (ZFC, ordinals, cardinals, AC)
  │     │
  │     └── Real Analysis (sequences, continuity, integration)
  │           │
  │           ├── Metric Spaces & Topology
  │           │     │
  │           │     └── Functional Analysis → RKHS, operator theory
  │           │
  │           ├── Measure Theory & Lebesgue Integration ◄── Analysis Phase 4
  │           │     │
  │           │     └── Probability Theory → Statistical Learning Theory → ML
  │           │
  │           └── Multivariable Analysis
  │                 │
  │                 ├── Optimization (convex analysis, gradient flow)
  │                 └── Differential Geometry → information geometry, diffusion models
  │
  └── Computability & Incompleteness
        │
        └── AI for Mathematics (Lean 4, formal verification, AlphaProof direction)

Linear Algebra (vector spaces, spectral theory)
  │
  ├── Matrix Calculus (Jacobians, Hessians) → backpropagation, optimization
  ├── Inner Product Spaces → merges into Functional Analysis (above, at "Metric Spaces & Topology" node)
  ├── Spectral Theorem → PCA, graph Laplacian, merges into Probability (covariance)
  └── Numerical Linear Algebra → GPU computation, large-scale optimization
Note: LA and Analysis trees merge at the Functional Analysis node.
LA Phase 3 (inner products, Hilbert spaces) is needed before Functional Analysis can begin.
```

### Parallel Learning Protocol

No more than two active math lines at once. Suggested pairings:
- **Logic Phase 0 + Analysis Phase 1** — both ground in formal language and sequences
- **Linear Algebra Phase 1-2 + Analysis Phase 2-3** — LA provides concrete examples for analysis
- **Analysis Phase 4 (measure theory) first, then Probability Phase 1** — not parallel, sequential dependency

Logic Phase 1 (ZFC, ordinals, cardinals) is not a prerequisite for Analysis — it deepens foundations but can be deferred until Analysis Phase 3 is complete without blocking progress.

## Math-Specific Methods

### Formalize to verify (Lean 4)
Lean 4 game levels and formalization enforce honest self-assessment. A natural-language proof that "feels right" may hide gaps; the Lean proof state shows exactly what hasn't been established.

### Proof before reading
Read the theorem statement, close the book, attempt the proof for 15+ minutes. Only then read the author's proof. Compare your approach — where did you diverge? Why?

## What to Skip

- **Pure computation drill** — integration tricks, limit evaluation techniques, series convergence tests beyond the main three (comparison, ratio, root). If a problem tests technique rather than understanding, skip it.
- **Overly technical lemmas** — if a lemma exists only to service one proof and doesn't illuminate a concept, note its existence and move on.
- **Generality for its own sake** — learn the R^n version before the Banach space version. Abstraction should follow concrete understanding, not precede it.

## AI Relevance Guide

What to pay extra attention to, given the AI career goal:

| Math Concept | AI Connection |
|---|---|
| Completeness, compactness | Foundation for optimization convergence proofs |
| Metric spaces, topology | Wasserstein distance, convergence of distributions |
| Measure theory, Lebesgue integration | Probability theory done right |
| Multivariable chain rule, Jacobians | Backpropagation is literally this |
| Inverse/implicit function theorem | Manifold learning, normalizing flows |
| Matrix calculus (Jacobians, Hessians) | Backpropagation, second-order optimization, Fisher information matrix |
| Convex analysis (duality, KKT) | SGD convergence proofs, constrained optimization in ML |
| Fisher information | Natural gradient, information geometry, Cram&eacute;r-Rao bounds |
| Numerical linear algebra | GPU matrix ops, L-BFGS, conjugate gradient, training at scale |
| Stochastic calculus (It&ocirc;, SDEs) | Diffusion models (Score SDE), Langevin dynamics, quantitative finance |
| Differential forms | Information geometry (advanced) |
| Gödel incompleteness | Theoretical limits of AI reasoning |
| Lean 4 formalization | AI-for-math (AlphaProof, autoformalization) |
