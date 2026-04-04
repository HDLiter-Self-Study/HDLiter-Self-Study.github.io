---
title: Deep Learning
date: 2026-04-02
lastmod: 2026-04-03
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
Note: Bach, Bishop², and Telgarsky also appear in the [[ai/machine-learning/index|ML roadmap]] — they bridge both fields.

- **Bach, *Learning Theory from First Principles*** (2024) — rigorous: ERM, kernels, overparameterization, implicit bias. [Free PDF](https://www.di.ens.fr/~fbach/ltfp_book.pdf).
- **Roberts, Yaida, Hanin, *The Principles of Deep Learning Theory*** (2022) — statistical mechanics approach: Gaussian processes, 1/n expansions, effective theory of deep networks. Requires comfort with statistical physics. [arXiv preprint](https://arxiv.org/abs/2106.10165).
- **Telgarsky, *Deep Learning Theory*** — online lecture notes (web format, not PDF): approximation, optimization landscape, generalization. [Website](https://mjt.cs.illinois.edu/dlt/).
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
| 8 | Statistical mechanics of deep networks: Gaussian process limit, 1/n corrections | Roberts Ch. 1-7 | [Optional / research-track] Requires stat mech background. Revisit after Phase 4 if pursuing DL theory research |
| 9 | Effective theory of deep networks at finite width | Roberts Ch. 8-11 | [Optional / research-track] Same as above |

### Phase 2: Architectures (Deep Dive)
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 10 | Convolutional networks: equivariance, receptive fields, architecture design | Bishop² Ch. 10-11, Michigan 498 | |
| 11 | Recurrent networks and the vanishing gradient problem | Bishop² Ch. 12 | |
| 12 | Attention mechanism: scaled dot-product, multi-head | Bishop² Ch. 12, CS224n | |
| 13 | Transformer architecture: encoder, decoder, positional encoding (incl. RoPE, context extension methods like YaRN) | Bishop² Ch. 12, CS224n, CS336 | |
| 14 | Vision transformers (ViT) and architecture unification | MIT 6.7960 | |
| 15 | Graph neural networks | Bishop² Ch. 13, CMU 10-708 | |
| 16 | State-space models and hybrid architectures (S4, Mamba, Jamba): long-sequence modeling, still evolving — not a first-priority learning target | MIT 6.7960, Mamba paper | |
| 17 | Self-supervised learning: contrastive (SimCLR, CLIP) and masked prediction (MAE, BERT) | NYU DL, MIT 6.7960 | InfoNCE links to [[mathematics/information-theory/index|information theory]] (mutual information) |
| 18 | Normalization, residual connections, and training stabilization | Prince Ch. 11, d2l | |

### Phase 3: Generative Models
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 19 | Latent variable models and variational autoencoders (VAE) | Bishop² Ch. 20, Murphy vol 2 | |
| 20 | ELBO, reparameterization trick, amortized inference | PRML Ch. 10, Murphy vol 2 | Links to [[mathematics/information-theory/index|information theory]] (KL divergence) |
| 21 | Generative adversarial networks (GAN): theory and training dynamics | Bishop² Ch. 21, Murphy vol 2 | |
| 22 | Normalizing flows and invertible networks | Murphy vol 2 | |
| 23 | Score matching and score-based models | MIT 6.S183, KAIST CS492(D) | |
| 24 | Denoising diffusion probabilistic models (DDPM) | MIT 6.S183, Bishop² Ch. 22 | Links to [[mathematics/analysis/index|stochastic analysis]] |
| 25 | Diffusion theory: forward/reverse SDE, probability flow ODE | KAIST CS492(D), Murphy vol 2 | |

### Phase 4: Foundation Models & LLM

> **Internal grouping** (items are numbered sequentially but don't need to be studied top-to-bottom):
> - **Core (26-29):** language modeling fundamentals, scaling, ICL
> - **Alignment pipeline (read in order: 30→31):** SFT *then* RLHF/DPO
> - **Architecture advances (32-34):** MoE, test-time compute, emergent abilities
> - **Inference & multimodal (35-36):** optimization, vision-language
> - **Applications (37-40):** RAG, agents, structured output, evaluation — **37-39 are highest priority for LLM+Finance**

| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 26 | Language modeling: autoregressive, masked | CS224n, CS336 | |
| 27 | Pre-training: objectives, data, tokenization | CS336 | |
| 28 | Scaling laws (Chinchilla, compute-optimal) | MIT 6.7960, CS336 | |
| 29 | In-context learning: what is it, why does it work? | CS229M, MIT 6.7960 | |
| 30 | Instruction tuning and supervised fine-tuning (SFT): data curation, format design | CMU 11-667, Wei et al. (FLAN, 2022), Chung et al. (Flan-T5, 2022), Zhou et al. (LIMA, 2023) | **Study before #31.** LIMA: 1K curated examples can match 50K+ |
| 31 | RLHF, DPO, and alignment | CS224n (2024), CS336 | Links to [[ai/reinforcement-learning/index|RL Phase 3]]. **Requires RL Phase 2** (policy gradient, PPO). RL Phase 3 covers RLHF from the RL side — read together |
| 32 | Mixture of Experts (MoE): sparse gating, Mixtral, DeepSeek-MoE | Fedus et al. (Switch Transformer, 2022), Jiang et al. (Mixtral, 2024), Dai et al. (DeepSeek-MoE, 2024) | Now a mainstream LLM architecture option |
| 33 | Test-time compute and inference-time reasoning: chain-of-thought, process reward models | Snell et al. (test-time compute scaling, 2024), Lightman et al. (PRM, 2023) | Major 2024-2025 paradigm shift |
| 34 | Emergent abilities, reasoning, and RL-based long-chain reasoning | CS25, MIT 6.7960, DeepSeek-R1 (2025, GRPO-trained reasoning) | DeepSeek-R1 uses RL (GRPO), not MCTS. MCTS-based: AlphaCode 2, rStar |
| 35 | Inference optimization: KV cache, quantization, speculative decoding | CS336 | |
| 36 | Multimodal models and vision-language: CLIP alignment, Flamingo, LLaVA, GPT-4V lineage | CS25 (ongoing), CMU 11-777 | |
| 37 | Retrieval-augmented generation (RAG): dense retrieval (DPR, bi-encoders vs cross-encoders), RAG architectures, advanced RAG (re-ranking, query expansion) | Lewis et al. (RAG, 2020), Gao et al. (RAG survey, 2024), CMU 11-868 | **LLM+Finance critical:** retrieval over 10-K, earnings calls |
| 38 | AI agents and agentic architectures: ReAct, tool use / function calling, multi-step planning, memory systems | Yao et al. (ReAct, 2023), Xi et al. (LLM agents survey, Fudan, 2023), Yang et al. (SWE-agent, 2024) | **LLM+Finance critical.** See also: MCP, LangGraph for orchestration |
| 39 | Structured / constrained generation: JSON mode, grammar-constrained decoding, schema enforcement | Willard & Louf (Outlines, 2023), OpenAI structured outputs docs | **LLM+Finance critical:** extracting structured data from 10-K filings |
| 40 | LLM evaluation methodology: automatic metrics limitations, LLM-as-judge biases (position, verbosity, self-enhancement), human eval, benchmark contamination | Zheng et al. (MT-Bench + Chatbot Arena, 2023), Liang et al. (HELM, 2023), CMU 11-667 | |

### Phase 5: Training Engineering
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 41 | Automatic differentiation and computational graphs | CMU 10-714 | |
| 42 | GPU programming: CUDA, Triton kernels | CS336, CMU 10-714 | |
| 43 | Operator fusion and memory optimization | CMU 10-714, CMU 11-868 | |
| 44 | Data parallelism, tensor parallelism, pipeline parallelism | CS336, CMU 11-868 | |
| 45 | Mixed precision training (fp16, bf16, fp8) | CS336, CMU 11-868 | |
| 46 | Model compression: quantization, pruning, distillation | CMU 11-868 | |

## Practice Checkpoints

| After Phase | Checkpoint |
|-------------|-----------|
| Phase 1 | On a simple two-layer network, experimentally demonstrate double descent. Explain wide-network behavior from the NTK perspective |
| Phase 2 | Train a Transformer from scratch on a small language modeling task (tiny Shakespeare or WikiText-2). Must write the attention mechanism yourself |
| Phase 3 | Implement VAE or DDPM from scratch. Generate samples, evaluate quality, ablate components |
| Phase 4a (concepts 26-31) | Fine-tune an open-weight LLM with SFT on a downstream task. Evaluate rigorously (not just vibes) |
| Phase 4b (concepts 37-39) | Build a RAG pipeline for LLM+Finance: retrieve from real documents (10-K or earnings calls), generate answers, evaluate with structured metrics |
| Phase 5 | Write a custom CUDA/Triton kernel for a matrix operation. Profile and compare with PyTorch |

## Progress

- [ ] Phase 1: Why Deep Learning Works
- [ ] Phase 2: Architectures
- [ ] Phase 3: Generative Models
- [ ] Phase 4: Foundation Models & LLM
- [ ] Phase 5: Training Engineering
