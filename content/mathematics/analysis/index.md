---
title: Real Analysis — Learning Roadmap
date: 2026-04-02
lastmod: 2026-04-02
tags:
  - mathematics
  - analysis
  - roadmap
draft: false
---

## Overview

A review of single-variable real analysis, combining textbook study with formal verification in Lean 4.

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

### Phase 4 (Optional): Beyond Abbott
| # | Topic | Source | Notes |
|---|-------|--------|-------|
| 9 | Metric spaces | Tao II / Rudin | Generalize Phase 1–2 results |
| 10 | Fourier series | Abbott Ch. 8 / Tao II | |

## Progress

> Track completed concept notes here as they are written.

- [ ] Phase 1: Foundations
- [ ] Phase 2: Topology and Continuity
- [ ] Phase 3: Calculus Made Rigorous
- [ ] Phase 4: Beyond Abbott
