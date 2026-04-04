---
title: Finance
date: 2026-04-03
lastmod: 2026-04-03
tags:
  - finance
  - roadmap
draft: false
---

## Overview

Finance learning path for the AI + finance career direction. Theory-practice parallel: understand economic mechanisms while building LLM-based signal extraction systems.

Prerequisites: [[mathematics/probability/index|probability theory]] (at least Phase 1) + [[ai/machine-learning/index|ML]] (at least Phase 1-2) + [[ai/deep-learning/index|DL]] Phase 4 (LLMs).

See [[finance/principles|Finance Learning Principles]] for domain-specific methodology.

## Resources

### Macroeconomics & Economic Thinking
| Resource | Type | Focus | Available? |
|----------|------|-------|------------|
| **Dalio, *How the Economic Machine Works*** | Video (30 min) | Credit cycles, deleveraging, the economic machine | [YouTube](https://www.youtube.com/watch?v=PHe0bXAIuk0) |
| **Dalio, *Principles for Navigating Big Debt Crises*** | Book (2018) | Historical debt crises, templates for deleveraging | `books/` |
| **Dalio, *Principles for Dealing with the Changing World Order*** | Book (2021) | Rise/decline of empires, reserve currency cycles | `books/` |
| **Mankiw, *Macroeconomics*** | Textbook | Standard macro: IS-LM, AD-AS, monetary/fiscal policy | Owned (paper) |
| **Mishkin, *The Economics of Money, Banking, and Financial Markets*** (13th ed.) | Textbook | Monetary policy transmission, central banking, financial crises | `books/` |
| **Perez, *Technological Revolutions and Financial Capital*** (2002) | Book | Tech revolution cycles and financial capital: bubble → crash → golden age. AI as current cycle | `books/` |

### Economic Thinking
| Resource | Type | Focus | Available? |
|----------|------|-------|------------|
| **Varian, *Intermediate Microeconomics*** (9th ed.) | Textbook | Incentives, game theory, information asymmetry, mechanism design — read selectively | Buy or reference |
| **Kahneman, *Thinking, Fast and Slow*** (2011) | Book | Systematic cognitive biases: prospect theory, framing, overconfidence, anchoring | Buy |
| **Acemoglu & Robinson, *Why Nations Fail*** (2012) | Book | Institutions as drivers of economic outcomes — complements Dalio's macro framework | Buy |

### Market Microstructure & Trading
| Resource | Type | Focus | Available? |
|----------|------|-------|------------|
| **Harris, *Trading and Exchanges*** (2003) | Textbook | The definitive microstructure book: order types, market makers, liquidity, price discovery | `books/` (draft) |
| **Narang, *Inside the Black Box*** (3rd ed., 2024) | Book | How systematic trading firms actually work: alpha models, risk, execution, infrastructure | `books/` |

### Financial Time Series & Econometrics
| Resource | Type | Focus | Available? |
|----------|------|-------|------------|
| **Tsay, *Analysis of Financial Time Series*** (3rd ed.) | Textbook | ARIMA, GARCH, volatility, multivariate time series, non-linear models | `books/` |
| **Cochrane, *Time Series for Macroeconomics and Finance*** | Lecture notes | Concise, connects macro to time series | `books/` |
| **Hamilton, *Time Series Analysis*** | Textbook (reference) | Comprehensive econometrics: stationarity, cointegration, state-space models | `books/` |

### Quantitative & Systematic Finance
| Resource | Type | Focus | Available? |
|----------|------|-------|------------|
| **De Prado, *Advances in Financial Machine Learning*** (2018) | Book | ML for finance done right: cross-validation for financial data, feature importance, backtesting pitfalls, meta-labeling. **Highest priority** | `books/` |
| **De Prado, *Machine Learning for Asset Managers*** (2020) | Book | Shorter, focused: portfolio optimization, signal processing, clustering | `books/` |
| **De Prado, *Causal Factor Investing*** (2023) | Monograph | Causal inference applied to factor investing | `books/` |
| **Pedersen, *Efficiently Inefficient*** (2015) | Book | How hedge funds actually work: macro, equity, quant strategies. Bridges academia and practice. **Key for Bridgewater context** | `books/` |
| **Ilmanen, *Expected Returns*** (2011) | Book (AQR) | What drives returns across asset classes. Systematic macro practitioner's bible | `books/` |
| **Ang, *Asset Management*** (2014) | Textbook | Factor investing theory, risk parity — Bridgewater's approach formalized | `books/` |
| **Hull, *Options, Futures, and Other Derivatives*** (11th ed.) | Reference | Derivatives pricing, hedging. Reference only — not primary reading | `books/` |

### LLM + Finance (Applied)
| Resource | Type | Focus | Available? |
|----------|------|-------|------------|
| **Jansen, *Machine Learning for Algorithmic Trading*** (2nd ed.) | Book (2020) | Practical: alternative data, NLP for trading, backtesting | `books/` · [Free notebooks](https://github.com/stefan-jansen/machine-learning-for-trading) |
| **Survey papers on NLP in finance** | Papers | FinBERT, BloombergGPT, LLM-based sentiment | arXiv |

### Causal Inference
| Resource | Type | Focus | Available? |
|----------|------|-------|------------|
| **Angrist & Pischke, *Mostly Harmless Econometrics*** | Textbook | IV, RDD, DID — the applied econometrics standard | `books/` |
| **Cunningham, *Causal Inference: The Mixtape*** | Textbook | Same topics, more accessible, code examples | [Free online](https://mixtape.scunning.com/) |

### Courses (all free)
| Course | Instructor | Focus | Link |
|--------|-----------|-------|------|
| **Mehrling, Economics of Money and Banking** | Mehrling (Columbia) | Monetary plumbing, central bank balance sheets, shadow banking | [Coursera](https://www.coursera.org/learn/money-banking) |
| **MIT 18.642 Math with Applications in Finance** | Various | Bond math, portfolio optimization, ML for finance | [MIT OCW (2024)](https://ocw.mit.edu/courses/18-642-topics-in-mathematics-with-applications-in-finance-fall-2024/) |
| **MIT 14.02 Principles of Macroeconomics** | Various | Blanchard-based macro foundation | [MIT OCW](https://ocw.mit.edu/courses/14-02-principles-of-macroeconomics-fall-2023/) |
| **MIT 15.401 Finance Theory I** | Lo | Asset pricing, portfolio theory, CAPM, EMH | [MIT OCW](https://ocw.mit.edu/courses/15-401-finance-theory-i-fall-2008/) |
| **Yale ECON 252 Financial Markets** | Shiller | Behavioral finance, market institutions, history | [Coursera](https://oyc.yale.edu/economics/econ-252) |
| **Cochrane Asset Pricing** | Cochrane | PhD-level: factor models, SDF, GMM | [YouTube + notes](https://www.johnhcochrane.com/asset-pricing) |
| **De Prado, Cornell ORIE 5256** | De Prado | Backtesting, portfolio construction, why most ML funds fail | [Slides](https://www.quantresearch.org/Lectures.htm) · [Videos](https://www.quantresearch.org/Videos.htm) |

## Roadmap

### Phase 1: How the Economic Machine Works (Macro)
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 1 | Credit cycles: short-term and long-term debt cycles | Dalio video + Big Debt Crises | |
| 2 | Monetary policy: interest rates, QE/QT, transmission mechanisms | Mankiw / Mishkin, MIT 14.02 | |
| 3 | Fiscal policy and government debt dynamics | Mankiw, MIT 14.02 | |
| 4 | Inflation: causes, measurement, central bank response | Mankiw / Mishkin | |
| 5 | Currency and balance of payments: exchange rates, capital flows | Mankiw, Dalio World Order | |
| 6 | Cross-asset macro relationships: rates ↔ FX ↔ commodities ↔ equities | Dalio Big Debt Crises, Bridgewater research | |
| 7 | Political incentives and policy formation: why central banks, governments, and regulators act the way they do | Acemoglu, Dalio World Order | |
| 8 | Technology-capital cycles: bubble → crash → golden age → maturity. AI as current cycle | Perez | |
| 9 | Historical crises as case studies: 2008, 1997 Asia, 1930s | Dalio Big Debt Crises | |

### Phase 2: Market Foundations
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 10 | Asset classes: equities, fixed income, FX, commodities — what drives each | MIT 15.401, Harris | |
| 11 | Market microstructure: order books, bid-ask spread, liquidity, market impact | Harris Ch. 1-12 | |
| 12 | Incentives and information asymmetry: adverse selection, moral hazard, signaling — why market participants behave the way they do | Varian (selected chapters) | |
| 13 | Game-theoretic reasoning: Nash equilibrium, repeated games, mechanism design — central bank vs. market as a repeated game | Varian (selected chapters) | |
| 14 | Efficient market hypothesis and its limits | MIT 15.401, Shiller | |
| 15 | Systematic cognitive biases: prospect theory, loss aversion, overconfidence, anchoring — when and why markets are irrational | Kahneman, Shiller | |
| 16 | Risk and return: volatility, drawdown, Sharpe ratio, fat tails | Cochrane Asset Pricing Ch. 1 | |
| 17 | Factor models: CAPM, Fama-French, momentum, quality | Cochrane Asset Pricing | |
| 18 | Portfolio construction: mean-variance, risk parity, Kelly criterion | Cochrane, De Prado MLA | |

### Phase 3: Financial Time Series
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 19 | Stationarity, unit roots, and differencing | Tsay Ch. 2, Hamilton | |
| 20 | ARIMA models and forecasting | Tsay Ch. 2 | |
| 21 | Volatility modeling: ARCH, GARCH, stochastic volatility | Tsay Ch. 3 | |
| 22 | Multivariate time series: VAR, cointegration, error correction | Tsay Ch. 8, Hamilton | |
| 23 | Regime switching and structural breaks | Hamilton Ch. 22, Tsay Ch. 4 | |
| 24 | Non-i.i.d. reality: why standard ML cross-validation fails on financial data | De Prado AFML Ch. 7 | |

### Phase 4: Systematic Strategies & Backtesting
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 25 | Signal construction: from raw data to tradeable feature | De Prado AFML Ch. 2-5 | |
| 26 | Labeling: fixed-horizon, triple-barrier, meta-labeling | De Prado AFML Ch. 3-4 | |
| 27 | Feature importance and selection for financial data | De Prado AFML Ch. 6, 8 | |
| 28 | Backtesting: walk-forward, combinatorial purged CV, avoiding biases | De Prado AFML Ch. 7, 9-12 | |
| 29 | Execution: slippage, market impact, transaction costs | Harris, Narang | |
| 30 | Strategy evaluation: Sharpe, Calmar, deflated Sharpe ratio | De Prado AFML Ch. 11 | |

### Phase 5: LLM + Finance
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 31 | Financial text sources: earnings calls, SEC filings, news, social media | Survey papers | |
| 32 | Sentiment extraction: lexicon-based vs. LLM-based, domain calibration | FinBERT paper, project experience | |
| 33 | Event extraction: what happened, to whom, expected impact | Project experience | |
| 34 | LLM as macro analyst: summarizing Fed minutes, interpreting policy signals | Project experience | |
| 35 | Signal evaluation: is the text-derived signal actually predictive? | De Prado AFML methodology | |
| 36 | Combining text signals with quantitative signals | De Prado MLA, project experience | |

### Phase 6: Causal Inference for Finance
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 37 | Potential outcomes framework and counterfactuals | Angrist & Pischke / Cunningham | |
| 38 | Instrumental variables | Angrist & Pischke | |
| 39 | Regression discontinuity and difference-in-differences | Cunningham | |
| 40 | Granger causality vs. true causality | Hamilton, Tsay | |
| 41 | Causal reasoning for robust signal construction | Pearl (light), project experience | |

## Suggested Sequencing

```
Phase 1 (Macro) ← START HERE — immediately relevant to Bridgewater
    │
Phase 2 (Market foundations) ← can overlap with Phase 1
    │
    ├── Phase 3 (Time series) ← connects to probability theory
    │       │
    │       └── Phase 4 (Systematic strategies) ← the methodology backbone
    │               │
    │               └── Phase 5 (LLM + Finance) ← your project
    │
    └── Phase 6 (Causal inference) ← start anytime after Phase 2
```

Phase 1 and 2 can run in parallel. Phase 5 can start early as a project — you'll revisit it with more rigor after Phase 3-4.

## Progress

- [ ] Phase 1: How the Economic Machine Works
- [ ] Phase 2: Market Foundations
- [ ] Phase 3: Financial Time Series
- [ ] Phase 4: Systematic Strategies & Backtesting
- [ ] Phase 5: LLM + Finance
- [ ] Phase 6: Causal Inference for Finance
