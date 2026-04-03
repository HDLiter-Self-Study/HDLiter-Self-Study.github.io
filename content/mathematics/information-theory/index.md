---
title: Information Theory
date: 2026-04-02
lastmod: 2026-04-02
tags:
  - mathematics
  - information-theory
  - roadmap
draft: false
---

## Overview

Information theory as the mathematical language connecting coding, inference, and learning. Focus on concepts that directly serve the AI learning path: entropy, KL divergence, mutual information, rate-distortion, and their roles in variational inference, generative models, and generalization bounds.

Prerequisites: [[mathematics/probability/index|probability theory]] (at least Phase 1).

## Resources

### Textbooks
| Book | Style | Free? |
|------|-------|-------|
| **MacKay, *Information Theory, Inference, and Learning Algorithms*** (2003) | Unique: bridges IT, Bayesian inference, and ML in one book. Opinionated, excellent exercises | [Free PDF](http://www.inference.org.uk/mackay/itila/) (owned) |
| **Polyanskiy & Wu, *Information Theory: From Coding to Learning*** (2024) | Most modern text. Explicitly connects IT to statistics, learning theory, high-dimensional probability. MIT 6.441 textbook | [Draft PDF](https://people.lids.mit.edu/yp/homepage/data/itbook-export.pdf) |
| **Cover & Thomas, *Elements of Information Theory*** (2nd ed.) | The standard reference. Comprehensive and rigorous. Less ML-focused | Not free, acquire if needed |

### Courses
| Course | Notes |
|--------|-------|
| **MIT 6.441 / 6.7710** (Polyanskiy) | Uses Polyanskiy & Wu. Lecture notes on OCW, no video |
| **Mathematicalmonk** (YouTube) | ~30 videos covering entropy, KL, channel coding. Excellent for quick intuition |
| **Raymond Yeung** (Coursera) | Full course, free to audit. Based on Yeung's textbook |

## Roadmap

### Phase 1: Core Concepts
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 1 | Entropy, joint entropy, conditional entropy | MacKay Ch. 2, P&W Ch. 2 | |
| 2 | KL divergence and its properties | MacKay Ch. 2, P&W Ch. 3 | Appears everywhere: ELBO, variational inference, PAC-Bayes |
| 3 | Mutual information | MacKay Ch. 2, P&W Ch. 3 | Feature selection, InfoNCE, representation learning |
| 4 | Data processing inequality | P&W Ch. 3 | Why deep nets can lose information |
| 5 | Maximum entropy principle | MacKay Ch. 22 | Connects to exponential families, softmax |

### Phase 2: Coding and Compression
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 6 | Source coding theorem (Shannon) | MacKay Ch. 4-5, P&W Ch. 5 | |
| 7 | Huffman coding, arithmetic coding | MacKay Ch. 5-6 | |
| 8 | Channel capacity and noisy channel theorem | MacKay Ch. 9-10, P&W Ch. 7 | |
| 9 | Rate-distortion theory | P&W Ch. 10, MacKay Ch. 33 | Connects to VAE: lossy compression = generation |

### Phase 3: Connections to Learning
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 10 | Minimum description length (MDL) and model selection | MacKay Ch. 28 | Information-theoretic Occam's razor |
| 11 | Information-theoretic generalization bounds | P&W Ch. 31-32 | Alternative to VC/Rademacher |
| 12 | PAC-Bayes bounds | P&W Ch. 33, Bach | Bridge between Bayesian and frequentist learning theory |
| 13 | Variational inference as KL minimization | MacKay Ch. 33, PRML Ch. 10 | Links to [[ai/deep-learning/index|DL generative models]] |
| 14 | Information bottleneck | P&W | Deep learning through the IT lens |

## Progress

- [ ] Phase 1: Core Concepts
- [ ] Phase 2: Coding and Compression
- [ ] Phase 3: Connections to Learning
