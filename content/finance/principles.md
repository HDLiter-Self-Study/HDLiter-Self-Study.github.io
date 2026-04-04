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
  └── Causal Inference for Finance (diagnostic tool, not alpha generator)
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

**On Dalio's framework specifically:** Dalio's economic machine model is useful for building macro intuition quickly. Read it as a practitioner's mental model, not an empirically validated theory. Its value is in the *questions it prompts* (what phase of the credit cycle are we in? who is the marginal buyer of this debt?) rather than the *predictions it implies*. Cross-check every Dalio claim against Mishkin and academic macro before treating it as a first principle.

### Think in incentives, not events
News says "Fed raises rates." A naive model encodes the event. A better question: *what were the Fed's incentives? Was this move priced in? Who is hurt, who benefits, and what will they do next?* Every market movement is the result of agents acting on incentives under constraints. Game-theoretic reasoning — commitment, signaling, repeated interaction — is more durable than memorizing "rate hikes → stocks down."

### Know when rationality breaks — and why it persists
Markets are mostly efficient, but systematically inefficient at specific points: when participants are loss-averse (prospect theory), when they anchor to irrelevant numbers, when they extrapolate recent trends (recency bias), when herding dominates (information cascades). These are predictable patterns rooted in cognitive biases.

But a bias is only exploitable if there are **structural limits to arbitrage** preventing sophisticated participants from eliminating it (Shleifer & Vishny 1997): capital constraints, career risk ("being right but early gets you fired"), short-selling costs, or liquidity constraints. Well-documented biases in large-cap liquid markets are likely already priced in. The remaining opportunities tend to be where arbitrage is structurally difficult — small-cap, distressed, illiquid, or cross-asset.

### Adversarial data environment
Financial data is fundamentally different from natural science data:
- **Non-stationary** — the distribution shifts because markets adapt
- **Fat-tailed** — 6-sigma events happen far more often than Gaussian models predict
- **Reflexive** — your model, if successful, changes the data it models
- **Low signal-to-noise** — most apparent patterns are noise
- **Small-T problem** — effective independent samples are scarce. A full business cycle is 7-10 years; you may observe only a handful. This fundamentally limits statistical power and is why De Prado stresses combinatorial purged CV

Treat every result with suspicion. The default hypothesis is always "this is noise."

### Backtesting discipline
A backtest is not evidence — it is a hypothesis that needs out-of-sample validation. Rules:
1. **No lookahead** — at time t, you can only use information available at time t. This includes universe selection: don't use today's S&P 500 constituents to backtest 2010 strategies (survivorship bias)
2. **Account for costs** — slippage, spread, market impact, borrowing costs
3. **Walk-forward validation** — train on [0, T], test on [T, T+Δ], roll forward
4. **Multiple testing correction** — if you tested 100 signals, some will "work" by chance. Use deflated Sharpe ratio or BHY correction for dependent tests
5. **Regime awareness** — a strategy that works in low-vol doesn't necessarily work in a crisis
6. **Survivorship bias** — delisted stocks, dead funds, retracted articles must be included in the data
7. **Backfill bias** — alternative data vendors often backfill historical data with corrections not available in real-time
8. **No p-hacking through specification** — tweaking holding period, entry threshold, or lookback window until it "works" is overfitting to history

### The alpha decay problem
Strategies have a shelf life. A published signal loses potency as more people trade it. Engineering knowledge in AI decays because frameworks change; alpha in finance decays because markets learn. The durable skills: understanding economic mechanisms, rigorous methodology, fast iteration.

## What to Skip

**Technical execution (AI-replaceable or not on your path):**
- **Accounting/financial statements deep dive** — LLMs can extract this. Know the key metrics, don't become an accountant.
- **Options pricing derivations (Black-Scholes, Greeks in depth)** — unless specifically trading options. However, **implied volatility, vol surface, and variance risk premium are NOT skippable** — they are core macro signals (VIX, skew) that BW and all macro funds track. Know the signal, skip the derivation.
- **Supply-demand curve computation, consumer/producer surplus** — microeconomics textbook exercises. The *thinking* (incentives, equilibrium) matters; the *calculation* doesn't.
- **Proprietary trading firm interview prep (brain teasers, mental math)** — not Bridgewater's style.

**Entire subfields not relevant to your direction:**
- **Labor economics, industrial organization** — applied micro subfields, too specialized.
- **International trade theory** — comparative advantage, Heckscher-Ohlin. Academic; the actually useful parts (exchange rates, capital flows) are already in Phase 1.
- **Corporate finance** — DCF, WACC, capital structure. You're doing macro + systematic, not equity fundamental analysis.
- **Crypto-specific protocols** — unless your project scope includes crypto markets.

## Bridgewater-Specific Context

Bridgewater runs two distinct strategies:
- **Pure Alpha** — directional systematic macro. Takes leveraged long/short positions across asset classes based on economic thesis. This is the flagship.
- **All Weather** — risk parity. Balances risk contributions across asset classes for all economic environments. No directional view.

Core philosophy:
- **Economic machine thinking** — every market movement has a cause rooted in credit, monetary policy, or productivity
- **Systematization** — investment logic must be expressible as rules that a machine can execute
- **Radical transparency / believability weighting** — this is *culture*, not investment methodology. Decisions are debated openly, weighted by track record. Relevant for interviews but distinct from the investment process.

As an investment engineer, you sit at the intersection of investment logic and implementation. The job is not "build ML models" — it's "translate an economic thesis into a testable, executable system."

The systemization pipeline: **investment logic → rule specification → historical simulation → validation → production monitoring.** An IE contributes at every stage — from formalizing a PM's thesis into testable rules, to designing the backtest infrastructure, to monitoring live signal degradation.

Technical context: BW's stack is primarily C++ and Python, with heavily self-built data infrastructure. Interviews may test system design ability (e.g., "design a backtestable signal pipeline"). As a new IE, your "believability" weight starts low — it accumulates through documented predictions and demonstrated reasoning quality.
