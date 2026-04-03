---
title: Linear Algebra (Theoretical) — Learning Roadmap
date: 2026-04-02
lastmod: 2026-04-02
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
- **Sheldon Axler, *Linear Algebra Done Right* (4th ed.)** — determinant-free development, focuses on linear maps over abstract vector spaces. Free PDF at [linear.axler.net](https://linear.axler.net). Author's video lectures at [LADRvideos](https://linear.axler.net/LADRvideos.html).

### Supplementary
- **Halmos, *Finite-Dimensional Vector Spaces*** — elegant, concise companion in the same spirit as his *Naive Set Theory*.
- **Gilbert Strang, MIT 18.06** ([YouTube](https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/video_galleries/video-lectures/)) — geometric intuition on demand. Not for systematic study; watch specific lectures when a concept needs visual grounding.

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

## AI Relevance

| Concept | AI Connection |
|---|---|
| Eigenvalues, spectral theorem | PCA, graph Laplacian, spectral clustering |
| SVD | dimensionality reduction, matrix completion, low-rank approximation |
| Inner products, projections | kernel methods, RKHS, attention as projection |
| Positive definite matrices | covariance matrices, Fisher information, natural gradient |
| Trace | loss functions, matrix calculus |

## Progress

- [ ] Phase 1: Vector Spaces and Linear Maps
- [ ] Phase 2: Structure of Operators
- [ ] Phase 3: Inner Product Spaces
- [ ] Phase 4: Determinants and Multilinear Algebra
