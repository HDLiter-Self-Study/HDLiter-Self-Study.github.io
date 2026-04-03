---
title: Machine Learning
date: 2026-04-02
lastmod: 2026-04-02
tags:
  - ai
  - machine-learning
  - learning-theory
  - roadmap
draft: false
---

## Overview

A theory-first path through machine learning — from the computational learning theory foundations ("what does it mean to learn?") through classical statistical methods to modern deep learning theory ("why does overparameterization generalize?").

Prerequisites: [[mathematics/linear-algebra/index|linear algebra]] (spectral theorem, SVD) + [[mathematics/probability/index|probability theory]] (measure-theoretic, at least through Phase 2) + [[mathematics/analysis/index|real analysis]] (convergence, compactness).

## Resources

### Foundational Theory
- **Shalev-Shwartz & Ben-David, *Understanding Machine Learning: From Theory to Algorithms*** (2014) — the best "first theory book." PAC learning, VC dimension, Rademacher complexity, all with full proofs. [Free PDF](https://www.cs.huji.ac.il/~shais/UnderstandingMachineLearning/understanding-machine-learning-theory-algorithms.pdf).
- **Mohri, Rostamizadeh, Talwalkar, *Foundations of Machine Learning*** (2nd ed.) — more terse and advanced than UML. [Free PDF](https://cs.nyu.edu/~mohri/mlbook/).

### Statistical / Probabilistic ML
- **Bishop, *Pattern Recognition and Machine Learning*** (2006) — Bayesian perspective, excellent on graphical models and variational inference. Classic. (owned, paper copy)
- **Hastie, Tibshirani, Friedman, *The Elements of Statistical Learning*** (2nd ed.) — frequentist perspective, strong on regularization, ensemble methods, high-dimensional statistics. [Free PDF](https://hastie.su.domains/ElemStatLearn/). (owned, paper copy)
- **Murphy, *Probabilistic Machine Learning*** (2 volumes, 2022/2023) — modern encyclopedic reference. Vol 1: intro through DNNs. Vol 2: advanced (VAE, diffusion, causality). [Free PDFs](https://probml.github.io/pml-book/).

### Information-Theoretic
- **MacKay, *Information Theory, Inference, and Learning Algorithms*** (2003) — unique perspective connecting information theory, Bayesian inference, and ML. [Free PDF](http://www.inference.org.uk/mackay/itila/).

### Modern Theory (Deep Learning)
- **Bach, *Learning Theory from First Principles*** (2024) — the most current and rigorous treatment: ERM, kernels, overparameterization, implicit bias, double descent. [Free PDF](https://www.di.ens.fr/~fbach/ltfp_book.pdf). **Highest priority for AI career goal.**
- **Bishop & Bishop, *Deep Learning: Foundations and Concepts*** (2024) — modernized PRML covering transformers, diffusion, GNNs. [Free digital](https://www.bishopbook.com).
- **Telgarsky, *Deep Learning Theory*** — lecture notes covering approximation, optimization landscape, generalization for deep nets. [Free](https://mjt.cs.illinois.edu/dlt/).

### High-Dimensional Statistics
- **Wainwright, *High-Dimensional Statistics: A Non-Asymptotic Viewpoint*** (2019) — concentration inequalities, random matrices, minimax theory. The mathematical machinery behind modern generalization bounds. (not owned, acquire when needed)

### Open Courses

| Course | Instructor | What | Video? | Materials |
|--------|-----------|------|--------|-----------|
| **Caltech CS156 "Learning from Data"** | Abu-Mostafa | VC theory, bias-variance, regularization, SVM, neural nets. Pedagogically superb | [YouTube (18 lec)](https://work.caltech.edu/telecourse.html) | Textbook + HW |
| **Stanford CS229M / STATS214** | Tengyu Ma | Modern ML theory: uniform convergence, NTK, implicit regularization, non-convex optimization | No video | [Lecture notes (excellent)](https://web.stanford.edu/class/stats214/) |
| **MIT 9.520/6.7910** | Poggio, Rosasco | Regularization theory, kernels, deep learning theory, generalization | No video | [Notes + slides](https://poggio-lab.mit.edu/9-520/) |
| **UC Berkeley CS189/289A** | Shewchuk | Full ML course, more mathematical than CS229 | Screencasts on course site | [Lecture notes (best in class)](https://people.eecs.berkeley.edu/~jrs/189/) |
| **Stanford CS224n** | Manning et al. | NLP with deep learning, transformers | [YouTube (2024)](https://web.stanford.edu/class/cs224n/) | Slides + assignments |
| **Stanford CS231n** | Fei-Fei Li et al. | Deep learning for vision, CNNs | YouTube (2017) | Slides + assignments |

## Roadmap

Organized by fundamental questions, not by book chapter. Each concept draws from multiple sources.

### Phase 1: What Does It Mean to Learn?
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 1 | The learning problem: hypothesis classes, loss functions, ERM | UML Ch. 2, Caltech lec 1–2 | |
| 2 | Overfitting, bias-variance tradeoff | ESL Ch. 7, Caltech lec 4, 8 | |
| 3 | Regularization as complexity control | ESL Ch. 3.4, PRML Ch. 1.1, Caltech lec 12 | |
| 4 | Cross-validation and model selection | ESL Ch. 7 | |

### Phase 2: Why Does Learning Generalize?
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 5 | PAC learning framework | UML Ch. 3–4, Caltech lec 2 | |
| 6 | Finite hypothesis classes, union bound | UML Ch. 4 | |
| 7 | VC dimension and growth function | UML Ch. 6, Caltech lec 6–7, Mohri Ch. 3 | |
| 8 | Rademacher complexity | UML Ch. 26, Mohri Ch. 3, Bach Ch. 2 | |
| 9 | Generalization bounds and uniform convergence | UML Ch. 4, 6, Bach Ch. 2 | |
| 10 | No-free-lunch theorem | UML Ch. 5 | |

### Phase 3: Linear and Kernel Methods
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 11 | Linear regression (frequentist and Bayesian) | ESL Ch. 3, PRML Ch. 3 | |
| 12 | Linear classification, logistic regression | ESL Ch. 4, PRML Ch. 4 | |
| 13 | Support vector machines and maximum margin | UML Ch. 15, ESL Ch. 12, Caltech lec 14 | |
| 14 | Kernel trick, Mercer's theorem, RKHS | PRML Ch. 6, Bach Ch. 5 | Links to [[mathematics/probability/index|functional analysis]] |
| 15 | Ensemble methods: bagging, boosting, random forests | ESL Ch. 10, 15–16, UML Ch. 10 | |

### Phase 4: Probabilistic Models
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 16 | Bayesian inference: prior, posterior, predictive | PRML Ch. 1–2, MacKay Ch. 2–3, Murphy vol 1 | |
| 17 | Graphical models: Bayesian networks, Markov random fields | PRML Ch. 8, Murphy vol 1 | |
| 18 | Expectation-Maximization algorithm | PRML Ch. 9, ESL Ch. 8 | |
| 19 | Variational inference | PRML Ch. 10, Murphy vol 2 | |
| 20 | MCMC and sampling methods | PRML Ch. 11, MacKay Ch. 29–30, Murphy vol 2 | |
| 21 | Information-theoretic view: KL divergence, maximum entropy, MDL | MacKay Ch. 4, 28 | |

### Phase 5: Optimization for ML
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 22 | Convex optimization basics: convexity, duality, KKT | Bach Ch. 3, Boyd & Vandenberghe (reference) | |
| 23 | Gradient descent: convergence rates, step size | Bach Ch. 3, CS229M notes | |
| 24 | Stochastic gradient descent and variance reduction | Bach Ch. 4 | |
| 25 | Non-convex optimization landscape: saddle points, local minima | CS229M notes, Telgarsky | |

### Phase 6: Online Learning
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 26 | Online convex optimization, regret bounds | UML Ch. 21, Bach Ch. 12 | |
| 27 | Multi-armed bandits, exploration-exploitation | UML Ch. 24, Bach Ch. 13 | |

→ Deep learning theory, architectures, and generative models continue in [[ai/deep-learning/index|Deep Learning]].
→ Sequential decision-making continues in [[ai/reinforcement-learning/index|Reinforcement Learning]].

## Suggested Sequencing

```
Phase 1–2 (theory foundations) ← start here, use UML + Caltech CS156
    │
Phase 3 (methods) ← ESL + PRML in parallel, by concept
    │
    ├── Phase 4 (probabilistic) ← PRML + MacKay + Murphy
    │
    └── Phase 5 (optimization) ← Bach + CS229M notes
            │
        Phase 6 (online) ← UML + Bach
            │
        → Deep Learning (separate roadmap)
```

Phases 3 and 4 can be interleaved. Phase 5 can start as soon as Phase 2 is done.

## Books to Acquire (Free)

All high-priority books are freely available as PDF:
- [x] ESL (owned, paper)
- [x] PRML (owned, paper)
- [x] MacKay (owned, digital)
- [ ] UML — [free PDF](https://www.cs.huji.ac.il/~shais/UnderstandingMachineLearning/understanding-machine-learning-theory-algorithms.pdf)
- [ ] Murphy vol 1+2 — [free PDFs](https://probml.github.io/pml-book/)
- [ ] Mohri et al. — [free PDF](https://cs.nyu.edu/~mohri/mlbook/)
- [ ] Wainwright — not free, acquire when needed

## Progress

- [ ] Phase 1: What Does It Mean to Learn?
- [ ] Phase 2: Why Does Learning Generalize?
- [ ] Phase 3: Linear and Kernel Methods
- [ ] Phase 4: Probabilistic Models
- [ ] Phase 5: Optimization for ML
- [ ] Phase 6: Online Learning
