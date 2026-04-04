---
title: Finance Learning Principles
date: 2026-04-03
lastmod: 2026-04-03
tags:
  - finance
  - meta-learning
draft: false
---

Domain-specific principles for finance. See [[principles|general learning principles]] for the cross-subject cognitive science framework.

## Dependency Map

```
Macroeconomics (credit cycles, monetary policy, cross-asset)
  │
  ├── Market Foundations (microstructure, asset classes, risk)
  │     │
  │     ├── Financial Time Series / Econometrics
  │     │     │
  │     │     └── Systematic Strategies & Backtesting
  │     │           │
  │     │           └── LLM + Finance (signal extraction, evaluation)
  │     │
  │     └── Portfolio Construction & Risk Management
  │
  └── Causal Inference for Finance
```

### Cross-references

| This vault | Finance connection |
|---|---|
| [[mathematics/probability/index\|Probability Theory]] | Stochastic processes, fat tails, extreme value theory |
| [[mathematics/information-theory/index\|Information Theory]] | Signal-to-noise in financial data, Kelly criterion |
| [[ai/machine-learning/index\|Machine Learning]] | Feature engineering, generalization (but financial data breaks i.i.d.) |
| [[ai/deep-learning/index\|Deep Learning]] Phase 4 | LLM for financial text understanding |
| [[ai/reinforcement-learning/index\|Reinforcement Learning]] | Portfolio optimization as sequential decision-making |

## Finance-Specific Methods

### Domain first, model second
The most common failure mode in quantitative finance: building a sophisticated model on top of a misunderstanding of what the data represents. Before writing any code, ask: *what economic mechanism would cause this signal to exist, and why hasn't it been arbitraged away?*

### Adversarial data environment
Financial data is fundamentally different from natural science data:
- **Non-stationary** — the distribution shifts because markets adapt
- **Fat-tailed** — 6-sigma events happen far more often than Gaussian models predict
- **Reflexive** — your model, if successful, changes the data it models
- **Low signal-to-noise** — most apparent patterns are noise

Treat every result with suspicion. The default hypothesis is always "this is noise."

### Backtesting discipline
A backtest is not evidence — it is a hypothesis that needs out-of-sample validation. Rules:
1. **No lookahead** — at time t, you can only use information available at time t
2. **Account for costs** — slippage, spread, market impact, borrowing costs
3. **Walk-forward validation** — train on [0, T], test on [T, T+Δ], roll forward
4. **Multiple testing correction** — if you tested 100 signals, some will "work" by chance
5. **Regime awareness** — a strategy that works in low-vol doesn't necessarily work in a crisis

### The alpha decay problem
Strategies have a shelf life. A published signal loses potency as more people trade it. Engineering knowledge in AI decays because frameworks change; alpha in finance decays because markets learn. The durable skills: understanding economic mechanisms, rigorous methodology, fast iteration.

## What to Skip

- **Options pricing theory (Black-Scholes, Greeks in depth)** — unless you're specifically trading options. Know the intuition, skip the stochastic calculus derivations for now.
- **Accounting/financial statements deep dive** — LLMs can extract this information. Understand the key metrics (P/E, debt/equity, free cash flow) but don't become an accountant.
- **Proprietary trading firm interview prep (brain teasers, mental math)** — not relevant to Bridgewater's style, which emphasizes thinking frameworks over speed.
- **Crypto-specific protocols** — unless your project scope includes crypto markets.

## Bridgewater-Specific Context

Bridgewater's investment philosophy is systematic macro:
- **Economic machine thinking** — every market movement has a cause rooted in credit, monetary policy, or productivity
- **Risk parity** — balance risk across asset classes rather than allocating by capital
- **Radical transparency / believability weighting** — investment decisions are debated openly, weighted by track record
- **Systematization** — investment logic must be expressible as rules that a machine can execute

As an investment engineer, you sit at the intersection of investment logic and implementation. The job is not "build ML models" — it's "translate an economic thesis into a testable, executable system."
