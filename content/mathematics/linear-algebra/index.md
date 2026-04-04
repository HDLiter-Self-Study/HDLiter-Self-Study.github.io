---
title: Linear Algebra
date: 2026-04-02
lastmod: 2026-04-03
tags:
  - mathematics
  - linear-algebra
  - roadmap
draft: false
---

## Overview

A proof-based treatment of linear algebra, building on computational familiarity from a CS background. The goal is not to re-learn row reduction but to understand *why* the spectral theorem works, what determinants really measure, and how inner product structure governs everything from PCA to quantum mechanics.

## Resources

### Primary
- **Sheldon Axler, *Linear Algebra Done Right* (4th ed.)** — determinant-free development, focuses on linear maps over abstract vector spaces. Free PDF at [linear.axler.net](https://linear.axler.net). Author's video lectures at [LADRvideos](https://linear.axler.net/LADRvideos.html). **Note:** Axler defers determinants to Ch. 10 by design. Excellent for abstract intuition, but for the geometric meaning of determinants and their role in Jacobians / change of variables ([[mathematics/analysis/index|Analysis Phase 6]]), supplement with Phase 4 or Hoffman & Kunze.

### Supplementary
- **Halmos, *Finite-Dimensional Vector Spaces*** — elegant, concise companion in the same spirit as his *Naive Set Theory*.
- **Gilbert Strang, MIT 18.06** ([YouTube](https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/video_galleries/video-lectures/)) — geometric intuition on demand. Not for systematic study; watch specific lectures when a concept needs visual grounding.

### Matrix Calculus (Phase 5)
- **Johnson & Edelman, *Matrix Calculus (for Machine Learning and Beyond)*** (2025) — the most modern and ML-focused treatment. Derivatives as linear operators, forward/reverse mode (backpropagation), Jacobians, Hessians, second-order methods. Textbook form of MIT 18.S096. [arXiv:2501.14787](https://arxiv.org/abs/2501.14787). Free. **Recommended primary text.**
- **Parr & Howard, *The Matrix Calculus You Need For Deep Learning*** (2018) — ~30-page warm-up tutorial: scalar to Jacobians for neural net layers. Good 1-2 day primer before Johnson & Edelman. [arXiv:1802.01528](https://arxiv.org/abs/1802.01528). Free.
- **Magnus & Neudecker, *Matrix Differential Calculus with Applications in Statistics and Econometrics*** (3rd ed., 2019) — the rigorous standard. Differentials, Kronecker products, vec operator. Use as reference for specific topics (e.g., Fisher information matrix derivations).
- **MIT 18.S096: Matrix Calculus for Machine Learning and Beyond** (Edelman & Johnson, IAP 2023/2025) — 6 lectures + problem sets. [OCW](https://ocw.mit.edu/courses/18-s096-matrix-calculus-for-machine-learning-and-beyond-january-iap-2023/) · [GitHub](https://github.com/mitmath/matrixcalc).
- **Petersen & Pedersen, *The Matrix Cookbook*** (2012) — identity reference sheet, not a textbook. Keep on hand. [Free PDF](https://www.math.uwaterloo.ca/~hwolkowic/matrixcookbook.pdf).

### Numerical Linear Algebra (Reference)
- **Trefethen & Bau, *Numerical Linear Algebra*** (1997) — the standard text. 40 short lectures: QR, SVD algorithms, conditioning/stability, iterative methods (CG, GMRES, Arnoldi/Lanczos). Read when you need to understand how LA computations work on actual hardware.
- **Golub & Van Loan, *Matrix Computations*** (4th ed., 2013) — encyclopedic reference. Blocking strategies, parallel decomposition, sparse methods. Use after Trefethen for specific topics.
- **fast.ai Computational Linear Algebra** (Rachel Thomas, 2017) — code-first with NumPy/PyTorch. [GitHub](https://github.com/fastai/numerical-linear-algebra). Good for quick hands-on understanding.

### Reference
- **Hoffman & Kunze, *Linear Algebra*** — the "Rudin of linear algebra." Not owned; acquire if deeper reference is needed.

## Roadmap

Organized by concept, not by textbook chapter. Multiple sources per concept where useful.

### Phase 1: Vector Spaces and Linear Maps
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 1 | Vector spaces, subspaces, span, independence | Axler 1–2, Halmos 1 | |
| 2 | Bases and dimension | Axler 2, Halmos 2 | |
| 3 | Linear maps: kernel, image, rank-nullity | Axler 3, Halmos 3 | |
| 4 | Matrices as representations of linear maps | Axler 3 | |
| 5 | Isomorphism and change of basis | Axler 3, Halmos 4 | |

### Phase 2: Structure of Operators
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 6 | Invariant subspaces | Axler 5, Halmos 6 | |
| 7 | Eigenvalues and eigenvectors | Axler 5, Strang lec 21 | |
| 8 | Minimal and characteristic polynomials | Axler 5, 8 | |
| 9 | Generalized eigenvectors, nilpotent operators | Axler 8 | |
| 10 | Jordan normal form | Axler 8, Halmos | |

### Phase 3: Inner Product Spaces
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 11 | Inner products, norms, orthogonality | Axler 6, Strang lec 15 | |
| 12 | Gram-Schmidt and orthonormal bases | Axler 6 | |
| 13 | Orthogonal projections and complements | Axler 6, Strang lec 16 | |
| 14 | Adjoint operators | Axler 7 | |
| 15 | Self-adjoint and normal operators | Axler 7 | |
| 16 | Spectral theorem (real and complex) | Axler 7 | |
| 17 | Positive operators and polar decomposition | Axler 7 | |
| 18 | Singular value decomposition | Axler 7, Strang lec 29 | |

### Phase 4: Determinants and Multilinear Algebra
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 19 | Determinant as signed volume / alternating multilinear form | Axler 10 | |
| 20 | Trace, characteristic polynomial revisited | Axler 10 | |
| 21 | Dual spaces and tensors | Halmos, Axler 3F | |

### Phase 5: Matrix Calculus
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 22 | Derivatives of scalar-by-vector and vector-by-vector functions, Jacobian matrices | Parr & Howard, Johnson & Edelman Ch. 1-2 | |
| 23 | Chain rule for vector/matrix functions, backpropagation as matrix calculus | Johnson & Edelman Ch. 3-4, MIT 18.S096 | Links to [[ai/deep-learning/index|DL Phase 1]] |
| 24 | Matrix-by-matrix derivatives: differentials, vec operator, Kronecker products | Magnus & Neudecker Ch. 1-5, Johnson & Edelman Ch. 5 | |
| 25 | Hessian matrices and second-order optimization | Johnson & Edelman Ch. 6, Boyd & Vandenberghe | Links to [[ai/machine-learning/index|ML Phase 5]] |

> Items 22-23 can be started after Phase 2 (eigenvalues). Items 24-25 (Kronecker products, Hessians) benefit from Phase 3 (inner products) for understanding Fisher information matrix. For AI applications, this is the highest-priority extension of the core roadmap.

## AI Relevance

| Concept | AI Connection |
|---|---|
| Eigenvalues, spectral theorem | PCA, graph Laplacian, spectral clustering |
| SVD | dimensionality reduction, matrix completion, low-rank approximation |
| Inner products, projections | kernel methods, RKHS, attention as projection |
| Positive definite matrices | covariance matrices, Fisher information, natural gradient |
| Trace | loss functions, matrix calculus |
| Fisher information matrix | Natural gradient (NGD), information geometry, Cramér-Rao bounds |
| Jacobian, chain rule (matrix) | Backpropagation is literally this |
| Hessian | Second-order optimization (Newton, L-BFGS), loss landscape curvature |
| Numerical stability (QR, SVD algorithms) | Why naive implementations blow up on GPU; conditioning |

## Progress

- [ ] Phase 1: Vector Spaces and Linear Maps
- [ ] Phase 2: Structure of Operators
- [ ] Phase 3: Inner Product Spaces
- [ ] Phase 4: Determinants and Multilinear Algebra
- [ ] Phase 5: Matrix Calculus
