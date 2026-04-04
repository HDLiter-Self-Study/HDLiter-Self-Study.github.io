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
  ├── Political economy (why policies are what they are)
  │
  ├── Market Foundations (microstructure, asset classes, risk)
  │     │
  │     ├── Incentives & game theory (market participant behavior)
  │     │
  │     ├── Cognitive biases (when and why markets are irrational)
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

### Think in incentives, not events
News says "Fed raises rates." A naive model encodes the event. A better question: *what were the Fed's incentives? Was this move priced in? Who is hurt, who benefits, and what will they do next?* Every market movement is the result of agents acting on incentives under constraints. Game-theoretic reasoning — commitment, signaling, repeated interaction — is more durable than memorizing "rate hikes → stocks down."

### Know when rationality breaks
Markets are mostly efficient, but systematically inefficient at specific points: when participants are loss-averse (prospect theory), when they anchor to irrelevant numbers, when they extrapolate recent trends (recency bias), when herding dominates. These are not random failures — they are predictable patterns rooted in cognitive biases. The value of behavioral economics is not "markets are irrational" but "markets are irrational *in specific, exploitable ways*."

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

**Technical execution (AI-replaceable or not on your path):**
- **Accounting/financial statements deep dive** — LLMs can extract this. Know the key metrics, don't become an accountant.
- **Options pricing theory (Black-Scholes, Greeks in depth)** — unless specifically trading options. Know the intuition, skip the derivations.
- **Supply-demand curve computation, consumer/producer surplus** — microeconomics textbook exercises. The *thinking* (incentives, equilibrium) matters; the *calculation* doesn't.
- **Proprietary trading firm interview prep (brain teasers, mental math)** — not Bridgewater's style.

**Entire subfields not relevant to your direction:**
- **Labor economics, industrial organization** — applied micro subfields, too specialized.
- **International trade theory** — comparative advantage, Heckscher-Ohlin. Academic; the actually useful parts (exchange rates, capital flows) are already in Phase 1.
- **Corporate finance** — DCF, WACC, capital structure. You're doing macro + systematic, not equity fundamental analysis.
- **Crypto-specific protocols** — unless your project scope includes crypto markets.

## Bridgewater-Specific Context

Bridgewater's investment philosophy is systematic macro:
- **Economic machine thinking** — every market movement has a cause rooted in credit, monetary policy, or productivity
- **Risk parity** — balance risk across asset classes rather than allocating by capital
- **Radical transparency / believability weighting** — investment decisions are debated openly, weighted by track record
- **Systematization** — investment logic must be expressible as rules that a machine can execute

As an investment engineer, you sit at the intersection of investment logic and implementation. The job is not "build ML models" — it's "translate an economic thesis into a testable, executable system."
