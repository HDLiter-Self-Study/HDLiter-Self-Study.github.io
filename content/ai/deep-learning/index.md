---
title: Deep Learning — Learning Roadmap
date: 2026-04-02
lastmod: 2026-04-02
tags:
  - ai
  - deep-learning
  - roadmap
draft: false
---

## Overview

Beyond the hands-on introduction (CMU 11-785): deep learning theory, modern architectures, generative models, and foundation models. Emphasis on *why* things work, not just *how* to build them.

Prerequisites: [[ai/machine-learning/index|ML theory]] (at least Phase 1-2) + [[mathematics/linear-algebra/index|linear algebra]] + [[mathematics/probability/index|probability]].

## Resources

### Theory
- **Bach, *Learning Theory from First Principles*** (2024) — rigorous: ERM, kernels, overparameterization, implicit bias. [Free PDF](https://www.di.ens.fr/~fbach/ltfp_book.pdf).
- **Roberts, Yaida, Hanin, *The Principles of Deep Learning Theory*** (2022) — statistical mechanics approach: Gaussian processes, 1/n expansions, effective theory of deep networks. Requires comfort with statistical physics. [arXiv preprint](https://arxiv.org/abs/2106.10165).
- **Telgarsky, *Deep Learning Theory*** — lecture notes: approximation, optimization landscape, generalization. [Free](https://mjt.cs.illinois.edu/dlt/).
- **Stanford CS229M / STATS214** (Tengyu Ma) — NTK, implicit regularization, non-convex optimization. [Lecture notes](https://web.stanford.edu/class/stats214/).

### Textbooks (Modern)
- **Bishop & Bishop, *Deep Learning: Foundations and Concepts*** (2024) — PRML successor covering transformers, diffusion, GNNs. [Free digital](https://www.bishopbook.com).
- **Prince, *Understanding Deep Learning*** (2023) — excellent figures, Jupyter notebooks, covers modern architectures. [Free PDF](https://udlbook.github.io/udlbook/).
- **Zhang et al., *Dive into Deep Learning*** — code-first (PyTorch/JAX), continuously updated. [d2l.ai](https://d2l.ai/).

### Courses

| Course | Instructor | Year | Key Topics | Video |
|--------|-----------|------|------------|-------|
| **MIT 6.7960 Deep Learning** | Isola, Beery, Bernstein | 2024 | Approximation, generalization, scaling, diffusion, LLMs. Theory-heavy | [OCW + YouTube](https://ocw.mit.edu/courses/6-7960-deep-learning-fall-2024/) |
| **Stanford CS336 Language Modeling from Scratch** | Hashimoto, Liang | 2025 | Build an LLM end-to-end: tokenization, GPU kernels, parallelism, scaling laws, RLHF | [cs336.stanford.edu](https://cs336.stanford.edu/) |
| **Stanford CS224n NLP with Deep Learning** | Manning et al. | 2024 | Transformers, pre-training, RLHF, reasoning, agents | [YouTube](https://web.stanford.edu/class/cs224n/) |
| **NYU Deep Learning** | LeCun, Canziani | 2021 | Energy-based models, JEPA, self-supervised learning. Unique LeCun perspective | [YouTube](https://atcold.github.io/NYU-DLSP21/) |
| **Michigan EECS 498-007** | Justin Johnson | 2019 | Best freely available DL-for-vision. CNNs, attention, generative | [YouTube](https://web.eecs.umich.edu/~justincj/teaching/eecs498/) |
| **Stanford CS330 Meta-Learning** | Chelsea Finn | 2022 | Meta-learning, few-shot, transfer, domain adaptation | [YouTube](https://cs330.stanford.edu/) |
| **Stanford CS25 Transformers United** | Various guest speakers | 2026 | Seminar: LLMs, reasoning, robotics, biology. Low commitment, high signal | [YouTube](https://web.stanford.edu/class/cs25/) |
| **CMU 10-708 Probabilistic Graphical Models** | Risteski | 2024 | Bayesian nets, MRFs, variational inference, deep generative models | [Slides](https://andrejristeski.github.io/10708S24/) |
| **CMU 10-714 Deep Learning Systems** | Tianqi Chen, Kolter | 2024 | Build a DL framework from scratch: autograd, GPU backend, operators | [Full video + HW](https://dlsyscourse.org/) |
| **CMU 10-725 Convex Optimization** | Balakrishnan | 2024 | Convex + non-convex optimization for ML, SGD analysis, duality | [Notes](https://www.stat.cmu.edu/~siva/teaching/725/) |
| **CMU 11-667 Large Language Models** | Ippolito | 2026 | LLM full picture: architecture, training, alignment, eval, applications | [Slides](https://cmu-llms.org/) |
| **CMU 11-868 LLM Systems** | | 2025 | GPU programming, distributed training, compression, RAG, multimodal | [Slides](https://llmsystem.github.io/) |
| **CMU 11-777 Multimodal ML** | Morency | 2024 | Multimodal representation, alignment, reasoning, generation | [Slides](https://cmu-mmml.github.io/) |
| **CMU 11-711 Advanced NLP** | Neubig | 2025 | Language modeling, reasoning, code generation | [Slides](https://cmu-l3.github.io/anlp-fall2025/) |

### Diffusion-Specific
- **MIT 6.S183: Practical Intro to Diffusion Models** (IAP 2026) — build from scratch. [practical-diffusion.org](https://www.practical-diffusion.org/).
- **KAIST CS492(D)** (Fall 2024) — diffusion theory + applications. [Course page](https://mhsung.github.io/kaist-cs492d-fall-2024/).

## Roadmap

### Phase 1: Why Deep Learning Works (Theory)
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 1 | Universal approximation theorems | Bach Ch. 6, Telgarsky | |
| 2 | Depth separation: what can deep nets compute that shallow can't? | Telgarsky, Bach Ch. 6 | |
| 3 | Optimization landscape: loss surfaces, saddle points, local minima | Bach Ch. 3-4, CS229M | |
| 4 | SGD convergence and implicit regularization | Bach Ch. 4, 9, CS229M | |
| 5 | Neural tangent kernel (NTK) and lazy training regime | Bach Ch. 7, CS229M | |
| 6 | Overparameterization, interpolation, double descent | Bach Ch. 8, Telgarsky | |
| 7 | Generalization in overparameterized models | Bach Ch. 8-9, Telgarsky | |
| 8 | Statistical mechanics of deep networks: Gaussian process limit, 1/n corrections | Roberts Ch. 1-7 | Requires [[physics]] stat mech |
| 9 | Effective theory of deep networks at finite width | Roberts Ch. 8-11 | |

### Phase 2: Architectures (Deep Dive)
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 10 | Convolutional networks: equivariance, receptive fields, architecture design | Bishop² Ch. 10-11, Michigan 498 | |
| 11 | Recurrent networks and the vanishing gradient problem | Bishop² Ch. 12 | |
| 12 | Attention mechanism: scaled dot-product, multi-head | Bishop² Ch. 12, CS224n | |
| 13 | Transformer architecture: encoder, decoder, positional encoding | Bishop² Ch. 12, CS224n | |
| 14 | Vision transformers (ViT) and architecture unification | MIT 6.7960 | |
| 15 | Graph neural networks | Bishop² Ch. 13, CMU 10-708 | |
| 16 | Normalization, residual connections, and training stabilization | Prince Ch. 11, d2l | |

### Phase 3: Generative Models
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 17 | Latent variable models and variational autoencoders (VAE) | Bishop² Ch. 20, Murphy vol 2 | |
| 18 | ELBO, reparameterization trick, amortized inference | PRML Ch. 10, Murphy vol 2 | |
| 19 | Generative adversarial networks (GAN): theory and training dynamics | Bishop² Ch. 21, Murphy vol 2 | |
| 20 | Normalizing flows and invertible networks | Murphy vol 2 | |
| 21 | Score matching and score-based models | MIT 6.S183, KAIST CS492(D) | |
| 22 | Denoising diffusion probabilistic models (DDPM) | MIT 6.S183, Bishop² Ch. 22 | Links to [[mathematics/analysis/index|stochastic analysis]] |
| 23 | Diffusion theory: forward/reverse SDE, probability flow ODE | KAIST CS492(D), Murphy vol 2 | |

### Phase 4: Foundation Models & LLM
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 24 | Language modeling: autoregressive, masked | CS224n, CS336 | |
| 25 | Pre-training: objectives, data, tokenization | CS336 | |
| 26 | Scaling laws (Chinchilla, compute-optimal) | MIT 6.7960, CS336 | |
| 27 | In-context learning: what is it, why does it work? | CS229M, MIT 6.7960 | |
| 28 | RLHF, DPO, and alignment | CS224n (2024), CS336 | Links to [[ai/reinforcement-learning/index|RL]] |
| 29 | Emergent abilities and reasoning | CS25, MIT 6.7960 | |
| 30 | Inference optimization: KV cache, quantization, speculative decoding | CS336 | |
| 31 | Multimodal models and vision-language | CS25 | |

### Phase 5: Training Engineering
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 32 | Automatic differentiation and computational graphs | CMU 10-714 | |
| 33 | GPU programming: CUDA, Triton kernels | CS336, CMU 10-714 | |
| 34 | Operator fusion and memory optimization | CMU 10-714, CMU 11-868 | |
| 35 | Data parallelism, tensor parallelism, pipeline parallelism | CS336, CMU 11-868 | |
| 36 | Mixed precision training (fp16, bf16, fp8) | CS336, CMU 11-868 | |
| 37 | Model compression: quantization, pruning, distillation | CMU 11-868 | |

## Progress

- [ ] Phase 1: Why Deep Learning Works
- [ ] Phase 2: Architectures
- [ ] Phase 3: Generative Models
- [ ] Phase 4: Foundation Models & LLM
- [ ] Phase 5: Training Engineering
