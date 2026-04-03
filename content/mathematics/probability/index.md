---
title: Probability Theory — Learning Roadmap
date: 2026-04-02
lastmod: 2026-04-02
tags:
  - mathematics
  - probability
  - measure-theory
  - roadmap
draft: false
---

## Overview

From undergraduate probability review to measure-theoretic foundations. The bridge from real analysis to statistical learning theory and modern ML.

Prerequisites: [[mathematics/analysis/index|real analysis]] (especially Phase 4: measure theory / Lebesgue integration) + [[mathematics/linear-algebra/index|linear algebra]] (inner products, spectral theorem).

## Resources

### Review (undergraduate refresh)
- **Blitzstein & Hwang, *Introduction to Probability* (2nd ed.)** — excellent motivation, rich examples. Pair with [Harvard Stat 110 YouTube lectures](https://www.youtube.com/playlist?list=PL2SOU6wwxB0uwwH80KTQ6ht66KWxbzTIo) at 1.5–2x speed for fast review.

### Primary (measure-theoretic)
- **Williams, *Probability with Martingales*** — concise (~250 pp), builds measure theory and probability together, reaches martingales quickly. Best transition from analysis to probability for self-study.

### Reference
- **Durrett, *Probability: Theory and Examples* (5th ed.)** — standard graduate text, covers more ground (Markov chains, ergodic theory). Free PDF from author. Solutions manual available.
- **Billingsley, *Probability and Measure* (4th ed.)** — encyclopedic reference, simultaneously develops measure theory and probability.
- **Nelson, *Radically Elementary Probability Theory*** — nonstandard analysis approach. Intellectually fascinating but off the main path.

### Courses
- **Harvard Stat 110** (Blitzstein, YouTube) — full undergraduate probability, excellent for review.
- **MIT 18.175 Theory of Probability** (Sheffield) — graduate level, lecture notes + slides on OCW, no video.

## Roadmap

Organized by concept. Phase 0 is review; Phases 1–3 are new material.

### Phase 0: Undergraduate Review (2–3 weeks, fast pass)
| # | Concept | Blitzstein | Stat 110 | Concept Notes |
|---|---------|-----------|----------|---------------|
| 1 | Counting, sample spaces, axioms of probability | Ch. 1 | Lec 1–3 | |
| 2 | Conditional probability, Bayes' theorem, independence | Ch. 2–3 | Lec 4–7 | |
| 3 | Discrete distributions (Bernoulli, binomial, Poisson, geometric) | Ch. 3–4 | Lec 8–12 | |
| 4 | Continuous distributions (uniform, normal, exponential, gamma) | Ch. 5 | Lec 13–17 | |
| 5 | Expectation, variance, covariance, moment generating functions | Ch. 4, 6 | Lec 18–22 | |
| 6 | Joint distributions, transformations, convolutions | Ch. 7–8 | Lec 23–28 | |
| 7 | Law of large numbers, central limit theorem (intuitive) | Ch. 10 | Lec 29–31 | |

### Phase 1: Measure-Theoretic Foundations
| # | Concept | Williams | Durrett | Concept Notes |
|---|---------|---------|--------|---------------|
| 8 | σ-algebras, measurable spaces | Ch. 1 | Ch. 1 | |
| 9 | Measures, probability measures, construction of Lebesgue measure | Ch. 1 | App. A | Link to [[mathematics/analysis/index|Analysis Phase 4]] |
| 10 | Measurable functions, random variables | Ch. 2–3 | Ch. 1 | |
| 11 | Integration and expectation (Lebesgue) | Ch. 5–6 | Ch. 1 | |
| 12 | Convergence concepts (a.s., in probability, in L^p, in distribution) | Ch. 4, 13 | Ch. 2 | |
| 13 | Product measures, Fubini's theorem, independence | Ch. 3–4 | Ch. 2 | |

### Phase 2: Limit Theorems
| # | Concept | Williams | Durrett | Concept Notes |
|---|---------|---------|--------|---------------|
| 14 | Borel-Cantelli lemmas | Ch. 4 | Ch. 2 | |
| 15 | Strong law of large numbers | Ch. 7 | Ch. 2 | |
| 16 | Weak convergence, characteristic functions | Ch. 13 | Ch. 3 | |
| 17 | Central limit theorem (rigorous proof) | Ch. 13 | Ch. 3 | |
| 18 | Large deviations (introduction) | | Durrett Ch. 2 | |

### Phase 3: Conditional Expectation and Martingales
| # | Concept | Williams | Durrett | Concept Notes |
|---|---------|---------|--------|---------------|
| 19 | Conditional expectation (measure-theoretic) | Ch. 9 | Ch. 5 | |
| 20 | Martingales: definition and examples | Ch. 10 | Ch. 5 | |
| 21 | Optional stopping theorem | Ch. 10 | Ch. 5 | |
| 22 | Martingale convergence theorems | Ch. 11 | Ch. 5 | |
| 23 | Uniform integrability | Ch. 12 | Ch. 5 | |
| 24 | Radon-Nikodym theorem and density | Ch. 14 | Ch. 5 | |

### Phase 4 (Future): Toward ML Theory
| # | Concept | Source | Concept Notes |
|---|---------|--------|---------------|
| 25 | Markov chains | Durrett Ch. 6 | |
| 26 | Concentration inequalities (Hoeffding, McDiarmid) | Speciality texts | |
| 27 | Empirical processes, VC dimension | → statistical learning theory | |

## AI Relevance

| Concept | AI Connection |
|---|---|
| Convergence modes (a.s., in prob, in dist) | Understanding when training converges and in what sense |
| Law of large numbers | Why empirical risk approximates true risk |
| Central limit theorem | Confidence intervals, asymptotic normality of estimators |
| Conditional expectation | Foundation of Bayesian inference, regression = E[Y\|X] |
| Martingales | Online learning, stochastic optimization convergence proofs |
| Radon-Nikodym | Density ratios, importance sampling, KL divergence |
| Concentration inequalities | Generalization bounds, PAC learning |

## Progress

- [ ] Phase 0: Undergraduate Review
- [ ] Phase 1: Measure-Theoretic Foundations
- [ ] Phase 2: Limit Theorems
- [ ] Phase 3: Conditional Expectation and Martingales
- [ ] Phase 4: Toward ML Theory
