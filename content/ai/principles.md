---
title: AI Learning Principles
date: 2026-04-03
lastmod: 2026-04-03
tags:
  - ai
  - meta-learning
draft: false
---

Domain-specific principles for AI. See [[principles|general learning principles]] for the cross-subject cognitive science framework.

## Two-Track Approach: Theory + Practice

Theory and practice run in parallel, not sequentially. Each reinforces the other:

- **Theory track** — textbooks, papers, proofs. Answers *why* things work.
- **Practice track** — project repos, reimplementations, experiments. Answers *what actually happens*.

The failure mode of theory-only: can derive the gradient but can't debug a training run. The failure mode of practice-only: can get a model to converge but can't diagnose *why* it doesn't on a new problem.

**The bridge:** after each theory phase, pick a project that exercises the concepts. After each project, identify what you couldn't explain — that's the next theory gap.

### Practice Track Conventions

Projects live in external git repos (not this vault). Each project should contain:
- A short doc explaining what was built, why, and what was learned
- Notes on non-obvious engineering decisions and their outcomes

Periodically, extract durable insights from project docs into this vault (concept notes or learning log). The test for whether an engineering insight is worth keeping: **would it still be useful if the framework/library changed?** If yes, it's a principle. If no, it's an implementation detail — leave it in the project repo.

## Dependency Map

```
                    Theory Track                          Practice Track
                    ────────────                          ──────────────

ML Theory (Phase 1-2)                              Implement classical ML
  What is learning? Generalization.                 from scratch (numpy-level)
        │                                                    │
ML Methods (Phase 3-5)                              Scikit-learn → real datasets
  Kernels, Bayes, optimization.                     Kaggle-style experiments
        │                                                    │
DL Theory (Phase 1)                                 Reimplement backprop,
  Why depth? NTK. Double descent.                   build a mini-framework
        │                                                    │
DL Architectures (Phase 2)                          Train CNNs/Transformers
  Convolutions, attention, transformers.            on standard benchmarks
        │                                                    │
DL Generative (Phase 3)                             Implement VAE / diffusion
  VAE, GAN, diffusion, flows.                       from scratch
        │                                                    │
Foundation Models (Phase 4)                         Fine-tune / build on top of
  Scaling, ICL, alignment.                          open-weight LLMs
        │                                                    │
Training Engineering (Phase 5)                      GPU kernels, distributed
  CUDA, parallelism, compression.                   training at scale
        │                                                    │
RL (Phase 1-3)                                      Implement agents,
  MDPs, deep RL, RLHF.                             game environments
```

The tracks don't need to be perfectly synchronized. It's fine to be one phase ahead in theory or practice — but don't let the gap grow to two phases.

## AI-Specific Methods

### Reproduce before extending
The AI equivalent of "proof before reading." Before reading ablation studies or claiming to understand a method, reimplement the core algorithm and reproduce the main result (even at small scale). A surprising number of "intuitions" in the field don't survive reimplementation.

When NOT to reimplement: when the value is in scale (you won't learn much reimplementing GPT-3), when the codebase itself is the contribution (large systems like Megatron — read the code instead), or when a well-tested library exists and your goal is the downstream task.

### Paper reading triage
Not all papers deserve the same depth:

| Type | Time | What to extract |
|------|------|-----------------|
| **Landmark** (< 5/year) | Full day+ | Reimplement. Read every proof. Write a concept note | 
| **Key method** | 2–4 hours | Algorithm, key theorem, how it connects to what you know |
| **Survey / tutorial** | 1–2 hours | Build a mental map of the subfield. Note what to read next |
| **Incremental** | 15 min | Abstract + results table + figures. Move on |

How to tell which is which: if it introduces a name practitioners use (ADAM, ResNet, DDPM), it's at least a key method. If it changes how people build systems within a year, it's a landmark. Citation count is a lagging indicator — don't rely on it for recent work.

### Math first, intuition second (usually)
AI is full of hand-wavy "intuitions" that mislead (e.g., "attention is like human attention," "dropout is like an ensemble"). The default: **understand the mathematical mechanism, then construct your own intuition from it.** Borrowed metaphors are memory aids, not understanding.

The exception: for generative/constructive ideas (VAE, diffusion, normalizing flows), build intuition from the generative process first, *then* formalize with ELBO/SDE math. For analysis and theory (optimization, generalization), math-first is correct.

### Ablation mindset
When studying a method, always ask: *which component is actually load-bearing?* Many papers bundle 5 tricks together. The ablation table (or your own experiment) tells you which ones matter. This skill transfers directly to debugging training runs.

## What to Skip

- **Framework API churn** — don't memorize PyTorch/JAX API details. Know the concepts (autograd, vmap, compilation); look up the syntax when needed.
- **Training recipe collections** — "use cosine annealing with warmup for 3 epochs" is perishable knowledge. Understand *why* learning rate schedules help (loss landscape geometry), skip memorizing specific recipes.
- **Hype-cycle papers** — if a paper's main contribution is a benchmark number with no new idea, skip it. Next month's paper will beat it.
- **Exhaustive architecture variants** — don't study every ResNet/ViT variant. Understand the design principles (skip connections solve gradient flow; patch embedding trades inductive bias for scale), then learn specific variants only when a project demands it.

## Math Prerequisites Guide

Reverse index of [[mathematics/principles|Mathematics Learning Principles]] → AI Relevance Guide:

| AI Topic | Math You Need | When |
|----------|---------------|------|
| ML theory (generalization) | Real analysis (convergence, compactness), probability (concentration inequalities) | ML Phase 2 |
| Kernel methods, RKHS | Functional analysis (Hilbert spaces, Riesz representation) | ML Phase 3 |
| Bayesian ML | Measure-theoretic probability, information theory (KL, entropy) | ML Phase 4 |
| Optimization | Convex analysis, matrix calculus, spectral theory | ML Phase 5 |
| Deep learning theory | All of the above + random matrix theory | DL Phase 1 |
| Generative models (diffusion) | Stochastic calculus (SDEs, Fokker-Planck) | DL Phase 3 |
| Information geometry | Differential geometry (Riemannian manifolds) | Advanced |

Don't front-load all the math. Learn it just-in-time: start an AI phase, hit a wall, go learn the math, come back.

## AI Concept Mastery Criteria

Adapted from [[principles|general learning principles]] "When to Move On" for AI-specific content. A concept is done when you can answer YES to at least 2 of:

1. **Explain without notes:** state the core idea, the key assumption, and one thing that breaks if the assumption fails
2. **Derive the key result:** reproduce the main theorem/algorithm derivation without looking
3. **Implement from scratch:** produce working code at numpy/pseudocode level (where applicable)
4. **Connect:** link it to at least one concept in a different Phase or subject
5. **Critique:** identify one real-world scenario where this method would fail and why

Practice Checkpoints (in each roadmap) verify integrated, hands-on understanding. For individual concepts, aim for at least 1 criterion (theoretical concepts) or 2 criteria (method-level concepts) before moving on. Completing a checkpoint does NOT mean every concept in that Phase is mastered — use the criteria above to check each concept that later Phases depend on.

## Review Cadence

- After completing each Phase, schedule one review session for the previous Phase's key concepts before going deep into the new one.
- At the end of each month, pick the 3-5 most-depended-on concepts from that month's work (e.g., generalization bounds, Bellman equation, attention mechanism) and write one sentence each: "what would break if I assumed this was false?"
- A concept you can't quickly explain 4 weeks after learning it was never consolidated — it needs a dedicated session, not a skim.
- Record review outcomes in [[ai/learning-log|AI Learning Log]].

## Paper-to-Note Pipeline

After [[#Paper reading triage|triaging]] a paper, use this workflow to convert reading into durable knowledge:

1. **Read abstract + intro:** what problem, what claim?
2. **Read conclusion + figures:** what was actually shown?
3. **Find the one key equation or algorithm** (usually 1-3 per paper)
4. **Derive it yourself** or identify exactly where you can't follow
5. **Write a concept note only for the idea that generalizes beyond this paper** — don't transcribe the paper
6. **Record in [[ai/learning-log|learning log]]:** what mental model did this update?

Not every paper gets all steps — the triage level determines depth. But step 6 (logging the mental model update) applies even to 15-minute incremental reads.

## Engineering Experience: The Decay Problem

AI engineering knowledge has a half-life measured in months. Frameworks change, best practices get superseded, hardware shifts the tradeoff landscape. Strategy:

1. **Separate principle from implementation.** "Gradient checkpointing trades compute for memory" is a principle (durable). "Use `torch.utils.checkpoint`" is an implementation detail (perishable).
2. **Record the *why*, not the *how*.** In project docs: "We used mixed precision because the model didn't fit in 24GB at fp32" > "We added `torch.cuda.amp.autocast()`."
3. **Accept graceful forgetting.** Don't maintain a database of every training trick. The ones you use regularly will stick; the rest you can re-derive or look up from first principles.
4. **Invest in transferable skills.** Profiling, debugging numerics, reading GPU utilization — these survive framework changes. Specific API calls don't.
