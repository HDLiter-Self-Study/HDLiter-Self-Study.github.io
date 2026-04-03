---
title: Real Analysis
date: 2026-04-02
lastmod: 2026-04-02
tags:
  - mathematics
  - analysis
  - roadmap
draft: false
---

## Overview

A review of real analysis (single-variable through multivariable), combining textbook study with formal verification in Lean 4.

## Resources

### Primary Textbook
- **Stephen Abbott, *Understanding Analysis* (2nd ed.)** — compact, motivation-first, one chapter per core topic. Each chapter opens with a compelling question that the theory resolves.

### Formal Verification
- **Real Analysis, The Game** (Alex Kontorovich, Rutgers Math 311H) — 44 worlds, 138 levels of Lean 4 proofs covering the full undergraduate analysis curriculum. Play at [Lean Game Server](https://adam.math.hhu.de/#/g/AlexKontorovich/RealAnalysisGame). [GitHub](https://github.com/AlexKontorovich/RealAnalysisGame).
- Workflow: read Abbott → attempt corresponding game levels → gaps in understanding surface as unprovable goals → return to Abbott.

### Supplementary
- **Terence Tao, *Analysis I & II* (4th ed.)** — for when a definition or construction needs deeper grounding (especially the real number construction and foundational material).
- **Hairer & Wanner, *Analysis by Its History*** — companion reading for historical context and visual intuition.
- **Francis Su's lectures** (Harvey Mudd, YouTube) — on-demand when a proof or concept remains unclear after reading.
- **Kontorovich's lecture notes** — Socratic dialogues auto-generated from the Lean game, available at the [course page](https://alexkontorovich.github.io/2025F311H/).

### Multivariable Analysis
- **James Munkres, *Analysis on Manifolds*** — standard self-study text for multivariable analysis. Covers R^n differentiation, inverse/implicit function theorems, multiple integrals, differential forms, Stokes' theorem. More detailed and friendlier than Spivak.
- **Tao, *Analysis II* (4th ed.)** — already in collection; latter chapters cover multivariable differentiation and Lebesgue measure.
- **Ted Shifrin, Multivariable Mathematics** (UGA) — two-semester YouTube lecture series covering linear algebra + multivariable calculus + differential forms + Stokes' theorem. The most complete video resource available for this material.
- *Spivak, Calculus on Manifolds* — classic but very terse (~150 pp); better as a second pass than a first read.

### Reference
- Kontorovich, "The Shape of Math to Come" ([arXiv:2510.15924](https://arxiv.org/abs/2510.15924)) — pedagogical rationale for formal analysis teaching.

## Roadmap

The structure follows Abbott's chapters. Each topic becomes one or more concept notes after study.

### Phase 1: Foundations
| # | Topic | Abbott | Lean Game | Concept Notes |
|---|-------|--------|-----------|---------------|
| 1 | The real numbers — completeness, supremum | Ch. 1 | Worlds 1–5 | |
| 2 | Sequences and convergence | Ch. 2 | Worlds 6–12 | |
| 3 | Series | Ch. 2.7 | Worlds 13–15 | |

### Phase 2: Topology and Continuity
| # | Topic | Abbott | Lean Game | Concept Notes |
|---|-------|--------|-----------|---------------|
| 4 | Open/closed sets, compactness | Ch. 3 | Worlds 16–22 | |
| 5 | Continuity | Ch. 4 | Worlds 23–30 | |

### Phase 3: Calculus Made Rigorous
| # | Topic | Abbott | Lean Game | Concept Notes |
|---|-------|--------|-----------|---------------|
| 6 | The derivative | Ch. 5 | Worlds 31–35 | |
| 7 | Sequences and series of functions | Ch. 6 | Worlds 36–40 | |
| 8 | The Riemann integral | Ch. 7 | Worlds 41–44 | |

### Phase 4: Metric Spaces and Fourier Series
| # | Topic | Source | Concept Notes |
|---|-------|--------|---------------|
| 9 | Metric spaces | Tao II / Rudin | Generalize Phase 1–2 results to abstract setting |
| 10 | Fourier series | Abbott Ch. 8 / Tao II | |

### Phase 5: Multivariable Analysis
| # | Topic | Munkres | Tao II | Concept Notes |
|---|-------|---------|--------|---------------|
| 11 | R^n topology, linear maps | Ch. 1–3 | | |
| 12 | Differentiation in R^n, chain rule | Ch. 4 | Ch. 17 | |
| 13 | Inverse function theorem | Ch. 5 | Ch. 17 | |
| 14 | Implicit function theorem | Ch. 5 | Ch. 17 | |
| 15 | Multiple integrals, Fubini's theorem | Ch. 6 | Ch. 18 | |
| 16 | Change of variables | Ch. 6 | Ch. 18 | |
| 17 | Differential forms and wedge product | Ch. 7 | | |
| 18 | Integration of forms, Stokes' theorem | Ch. 8 | | |

## Progress

> Track completed concept notes here as they are written.

- [ ] Phase 1: Foundations
- [ ] Phase 2: Topology and Continuity
- [ ] Phase 3: Calculus Made Rigorous
- [ ] Phase 4: Metric Spaces and Fourier Series
- [ ] Phase 5: Multivariable Analysis
