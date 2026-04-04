---
title: Real Analysis
date: 2026-04-02
lastmod: 2026-04-03
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
- **Terence Tao, *Analysis I & II* (4th ed.)** — for when a definition or construction needs deeper grounding (especially the real number construction and foundational material). *Analysis II* also covers Lebesgue measure (Phase 4).
- **Hairer & Wanner, *Analysis by Its History*** — companion reading for historical context and visual intuition.
- **Francis Su's lectures** (Harvey Mudd, YouTube) — on-demand when a proof or concept remains unclear after reading.
- **Kontorovich's lecture notes** — Socratic dialogues auto-generated from the Lean game, available at the [course page](https://alexkontorovich.github.io/2025F311H/).

### Measure Theory (Phase 4)
- **Stein & Shakarchi, *Real Analysis: Measure Theory, Integration, and Hilbert Spaces*** (Princeton Lectures in Analysis III) — clean, modern treatment. Pairs well with Tao II for a second perspective.
- **Tao, *Analysis II* (4th ed.)** — latter chapters (Ch. 7-8) cover Lebesgue measure and integration.

### Measure Theory Video Courses (Phase 4)
- **Claudio Landim, IMPA** — ~35 lectures, 30+ hours. The gold standard for free measure theory video lectures. Calm, pedagogical, well-organized whiteboard lectures. Exercises PDF available on [instructor page](https://w3.impa.br/~landim/lectures.html). [YouTube playlist](https://www.youtube.com/watch?v=llnNaRzuvd4&list=PLo4jXE-LdDTQq8ZyA8F8reSQHej3F6RFX). Also mirrored on Bilibili with Chinese subtitles.
- **Bright Side of Mathematics (Julian Grossmann)** — 21 short videos (~5 hours total). Excellent animated overview: σ-algebras through Radon-Nikodym. Best as a quick first pass before Landim or textbook study. [YouTube playlist](https://www.youtube.com/playlist?list=PLBh2i93oe2qvMVqAzsX1Kuv6-4fjazZ8j).
- **MIT OCW** — no video lectures for measure theory. 18.125 (Measure and Integration) has notes only; 18.175 (Theory of Probability) has slides only.

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

### Phase 4: Measure Theory & Lebesgue Integration
| # | Topic | Source | Concept Notes |
|---|-------|--------|---------------|
| 9 | Lebesgue outer measure, measurable sets, σ-algebras | Tao II Ch. 7 / Stein & Shakarchi III Ch. 1 | |
| 10 | Measurable functions | Tao II Ch. 7 | |
| 11 | Lebesgue integral: construction, monotone convergence, Fatou's lemma, dominated convergence | Tao II Ch. 7-8 / Stein & Shakarchi III Ch. 2 | |
| 12 | L^p spaces, completeness, Hölder and Minkowski inequalities | Stein & Shakarchi III Ch. 4 | Link to [[mathematics/probability/index|Probability Phase 1]] |

> **Why here:** This phase is the bridge to measure-theoretic probability. [[mathematics/probability/index|Probability Phase 1]] directly builds on this material.

### Phase 5: Metric Spaces and Fourier Analysis

> Items 14-15 depend on L^p space completeness (Phase 4, Item 12).

| # | Topic | Source | Concept Notes |
|---|-------|--------|---------------|
| 13 | Metric spaces | Tao II Ch. 12-13 | Generalize Phase 1–2 results to abstract setting |
| 14 | Fourier series: L² convergence, Dirichlet kernel, Gibbs phenomenon | Abbott Ch. 8 / Tao II / Stein & Shakarchi I | |
| 15 | Fourier transform on R: Schwartz space, Plancherel theorem | Stein & Shakarchi I Ch. 5-6 | Connects to characteristic functions in [[mathematics/probability/index|Probability Phase 2]] |

### Phase 6: Multivariable Analysis
| # | Topic | Munkres | Tao II | Concept Notes |
|---|-------|---------|--------|---------------|
| 16 | R^n topology, linear maps | Ch. 1–3 | | |
| 17 | Differentiation in R^n, chain rule | Ch. 4 | Ch. 17 | |
| 18 | Inverse function theorem | Ch. 5 | Ch. 17 | |
| 19 | Implicit function theorem | Ch. 5 | Ch. 17 | |
| 20 | Multiple integrals, Fubini's theorem | Ch. 6 | Ch. 18 | |
| 21 | Change of variables | Ch. 6 | Ch. 18 | |
| 22 | Differential forms and wedge product (optional — defer if not pursuing information geometry) | Ch. 7 | | |
| 23 | Integration of forms, Stokes' theorem (optional — same as above) | Ch. 8 | | |

> Items 16–21 are the core path for AI. Items 22–23 (differential forms, Stokes) can be deferred unless information geometry becomes a focus.

## Progress

> Track completed concept notes here as they are written.

- [ ] Phase 1: Foundations
- [ ] Phase 2: Topology and Continuity
- [ ] Phase 3: Calculus Made Rigorous
- [ ] Phase 4: Measure Theory & Lebesgue Integration
- [ ] Phase 5: Metric Spaces and Fourier Analysis
- [ ] Phase 6: Multivariable Analysis
