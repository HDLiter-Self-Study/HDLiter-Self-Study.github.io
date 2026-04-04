---
title: Set Theory & Logic
date: 2026-04-02
lastmod: 2026-04-03
tags:
  - mathematics
  - logic
  - set-theory
  - roadmap
draft: false
---

## Overview

A rigorous study of the logical and set-theoretic foundations that underpin modern mathematics. Prioritized alongside (and partly before) [[mathematics/analysis/index|real analysis]], since FOL and ZFC form the language in which analysis is written.

## Resources

### Primary Courses (Video + Textbook)

- **UCB Math 125A — Mathematical Logic** (Antonio Montalbán)
  Textbook: Enderton, *A Mathematical Introduction to Logic* (2nd ed.)
  [YouTube playlist](https://www.youtube.com/playlist?list=PLjJhPCaCziSRSUtQiTA_yx5TJ76G_EqUJ) · [Course page](https://math.berkeley.edu/~antonio/math125A/) (HW + solutions + exams)

- **UCB Math 135 — Introduction to the Theory of Sets** (Antonio Montalbán)
  Textbook: Enderton, *Elements of Set Theory*
  [YouTube playlist](https://www.youtube.com/playlist?list=PLjJhPCaCziSQyON7NLc8Ac8ibdm6_iDQf)

### Textbooks

| Role | Book |
|---|---|
| Phase 0 primary | Enderton — *A Mathematical Introduction to Logic*, 2ed |
| Phase 1 primary | Enderton — *Elements of Set Theory* |
| Phase 1 companion | Halmos — *Naive Set Theory* |
| Phase 2 primary | Smith — *An Introduction to Gödel's Theorems*, 2ed |
| Phase 2 supplement | Boolos, Burgess, Jeffrey — *Computability and Logic*, 5ed (+ solutions) |
| Phase 2 deep dive | Cutland — *Computability: An Introduction to Recursive Function Theory* |
| Phase 3 primary | Kunen — *Set Theory: An Introduction to Independence Proofs* |
| Reference | Li, Vitányi — *An Introduction to Kolmogorov Complexity and Its Applications*, 4ed |

### Supplementary
- **Peter Smith's *Teach Yourself Logic* guide** — [logicmatters.net](https://www.logicmatters.net/tyl/) — the best meta-resource for sequencing logic self-study.
- **Frederic Schuller** (YouTube, first ~8 lectures) — fast foundations overview from logic to topology.
- **Ryan O'Donnell** (CMU, YouTube) — rigorous Gödel incompleteness lectures.

## Roadmap

### Phase 0: First-Order Logic (before / parallel to Analysis Phase 1)
| # | Topic | Enderton Logic | UCB 125A | Concept Notes |
|---|-------|---------------|----------|---------------|
| 1 | Sentential logic | Ch. 1 | | |
| 2 | First-order logic: syntax & semantics | Ch. 2.1–2.4 | | |
| 3 | A deductive calculus; soundness | Ch. 2.5 | | |
| 4 | The completeness theorem | Ch. 2.5 | | |
| 5 | Compactness and applications | Ch. 2.6 | | |

### Phase 1: Axiomatic Set Theory (parallel to Analysis Phase 1)
| # | Topic | Enderton ST | UCB 135 | Concept Notes |
|---|-------|------------|---------|---------------|
| 6 | Axioms of set theory (ZFC) | Ch. 1–3 | | |
| 7 | Relations, functions, order | Ch. 3–5 | | |
| 8 | Natural numbers, recursion, arithmetic | Ch. 4 | | |
| 9 | Ordinal numbers, transfinite induction | Ch. 7 | | |
| 10 | Cardinal numbers and their arithmetic | Ch. 6, 8 | | |
| 11 | Axiom of choice and equivalents | Ch. 6 | | |
| 12 | Construction of the real numbers | Ch. 5 | | ZFC formalization of Analysis Phase 1 content — do after Analysis Phase 1, not in parallel |

### Phase 2: Incompleteness & Computability (parallel to Analysis Phase 2–3)
| # | Topic | Source | Concept Notes |
|---|-------|--------|---------------|
| 13 | Primitive recursion, μ-recursion | BBJ / Cutland | |
| 14 | Turing machines, Church–Turing thesis | BBJ | |
| 15 | Representability, diagonalization | Smith | |
| 16 | Gödel's first incompleteness theorem | Smith | |
| 17 | Gödel's second incompleteness theorem | Smith | |
| 18 | Undecidability results | BBJ | |

### Phase 3: Advanced Set Theory (Optional — no AI relevance, pursue only if independence proofs become a personal interest)
| # | Topic | Source | Concept Notes |
|---|-------|--------|---------------|
| 19 | Constructible universe (L) | Kunen | |
| 20 | Forcing | Kunen | |
| 21 | Independence of CH and AC | Kunen | |

> **Note:** This phase covers PhD-level pure mathematics (forcing alone requires months to years). It has zero connection to ML/AI or other parts of this vault. Defer indefinitely unless AI-for-math (AlphaProof, Lean 4 formalization of set theory) becomes a primary research direction.

## Progress

- [ ] Phase 0: First-Order Logic
- [ ] Phase 1: Axiomatic Set Theory
- [ ] Phase 2: Incompleteness & Computability
- [ ] Phase 3: Advanced Set Theory
