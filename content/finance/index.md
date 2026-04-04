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
| **Dixit & Nalebuff, *The Art of Strategy*** (2008) | Book | Game-theoretic thinking applied to real decisions: commitment, signaling, repeated games, mechanism design | `books/` |
| **Kahneman, *Thinking, Fast and Slow*** (2011) | Book | Systematic cognitive biases: prospect theory, framing, overconfidence, anchoring | `books/` |
| **Acemoglu & Robinson, *Why Nations Fail*** (2012) | Book | Institutions as drivers of economic outcomes — complements Dalio's macro framework | `books/` |

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
| **Pearl, *Causality*** (2nd ed.) | Textbook | Structural causal models, d-separation, do-calculus — the formal framework | Buy (Ch. 1-3 sufficient) |
| **Campbell, Lo, MacKinlay, *The Econometrics of Financial Markets*** | Textbook | Event studies, empirical asset pricing methodology | Reference |

### Courses (all free)
| Course | Instructor | Focus | Link |
|--------|-----------|-------|------|
| **Mehrling, Economics of Money and Banking** | Mehrling (Columbia) | Monetary plumbing, central bank balance sheets, shadow banking | [Coursera](https://www.coursera.org/learn/money-banking) |
| **MIT 18.S096 Math with Applications in Finance** | Various | Bond math, portfolio optimization, ML for finance | [MIT OCW](https://ocw.mit.edu/courses/18-s096-topics-in-mathematics-with-applications-in-finance-fall-2013/) |
| **MIT 14.02 Principles of Macroeconomics** | Various | Blanchard-based macro foundation | [MIT OCW](https://ocw.mit.edu/courses/14-02-principles-of-macroeconomics-fall-2023/) |
| **MIT 15.401 Finance Theory I** | Lo | Asset pricing, portfolio theory, CAPM, EMH | [MIT OCW](https://ocw.mit.edu/courses/15-401-finance-theory-i-fall-2008/) |
| **Yale ECON 252 Financial Markets** | Shiller | Behavioral finance, market institutions, history | [Coursera](https://oyc.yale.edu/economics/econ-252) |
| **Cochrane Asset Pricing** | Cochrane | PhD-level: factor models, SDF, GMM | [YouTube + notes](https://www.johnhcochrane.com/asset-pricing) |
| **De Prado, Cornell ORIE 5256** | De Prado | Backtesting, portfolio construction, why most ML funds fail | [Slides](https://www.quantresearch.org/Lectures.htm) · [Videos](https://www.quantresearch.org/Videos.htm) |

## Roadmap

### Phase 1: How the Economic Machine Works (Macro)
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 1 | GDP, business cycle, and the output gap: productivity growth vs. cyclical fluctuation | Mankiw, MIT 14.02 | |
| 2 | Credit cycles: short-term and long-term debt cycles | Dalio video + Big Debt Crises | |
| 3 | Monetary policy: interest rates, QE/QT, transmission mechanisms | Mankiw / Mishkin, Mehrling | |
| 4 | Yield curve and term structure: expectations hypothesis, term premia — the single most important macro market signal | Mishkin, Cochrane time series notes | |
| 5 | Fiscal policy and government debt dynamics | Mankiw, MIT 14.02 | |
| 6 | Inflation: causes, measurement, central bank response | Mankiw / Mishkin | |
| 7 | Currency and balance of payments: exchange rates, capital flows | Mankiw, Dalio World Order | |
| 8 | Political incentives and policy formation: why central banks, governments, and regulators act the way they do | Acemoglu, Dalio World Order | |
| 9 | Technology-capital cycles: bubble → crash → golden age → maturity. AI as current cycle | Perez | |
| 10 | Cross-asset macro relationships: rates ↔ FX ↔ commodities ↔ equities | Dalio Big Debt Crises, Ilmanen | |
| 11 | Historical crises as case studies: 2008, 1997 Asia, 1930s | Dalio Big Debt Crises | |

### Phase 2: Market Foundations
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 12 | Asset classes: equities, fixed income, FX, commodities — what drives each | Ilmanen, MIT 15.401 | |
| 13 | Credit risk: credit spreads, default probability, CDS — the credit-equity nexus | Mishkin, Pedersen | |
| 14 | Market microstructure: order books, bid-ask spread, liquidity, market impact | Harris Ch. 1-12 | |
| 15 | Adverse selection and information asymmetry: why informed traders profit at the expense of uninformed — the Akerlof/Glosten-Milgrom framework | Harris, Dixit & Nalebuff | |
| 16 | Moral hazard and principal-agent problems: fund manager incentives, risk-shifting, too-big-to-fail | Dixit & Nalebuff, Mankiw micro | |
| 17 | Signaling, commitment, and repeated games: central bank communication as a strategic game | Dixit & Nalebuff | |
| 18 | Efficient market hypothesis and the Grossman-Stiglitz paradox: if markets are efficient, who gathers information? | MIT 15.401, Shiller, Pedersen | |
| 19 | Systematic cognitive biases: prospect theory, loss aversion, overconfidence, anchoring | Kahneman, Shiller | |
| 20 | Information cascades and herding: why markets overshoot | Bikhchandani et al. 1992, Shiller | |
| 21 | Limits to arbitrage: why biases persist (capital constraints, career risk, short-selling costs) | Pedersen Ch. 4-5 | |
| 22 | Risk and return: volatility, drawdown, Sharpe ratio, fat tails | Cochrane Asset Pricing Ch. 1, Ilmanen | |
| 23 | Factor models: CAPM, Fama-French, momentum, quality | Cochrane Asset Pricing, Ang | |
| 24 | Portfolio construction: mean-variance, risk parity, Kelly criterion (links to [[mathematics/information-theory/index|information theory]]) | Ang, De Prado MLA | |

### Phase 3: Financial Time Series
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 25 | Stationarity, unit roots, and differencing | Tsay Ch. 2, Hamilton | |
| 26 | ARIMA models and forecasting | Tsay Ch. 2, Cochrane time series notes | |
| 27 | Volatility modeling: ARCH, GARCH, stochastic volatility | Tsay Ch. 3 | |
| 28 | Realized volatility and high-frequency measures | Tsay Ch. 5 | |
| 29 | Long memory and fractional integration (ARFIMA): why volatility is persistent | Tsay Ch. 2, Hamilton | |
| 30 | Multivariate time series: VAR, Granger causality, cointegration, error correction | Tsay Ch. 8, Hamilton | |
| 31 | Regime switching and structural breaks | Hamilton Ch. 22, Tsay Ch. 4 | |
| 32 | Spectral analysis and filtering: separating signal from noise in macro time series | Hamilton, Cochrane time series notes | |

### Phase 4: Systematic Strategies & Backtesting
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 33 | Non-i.i.d. reality: why standard ML cross-validation fails on financial data | De Prado AFML Ch. 7 | |
| 34 | Signal construction: from raw data to tradeable feature | De Prado AFML Ch. 2-5, Narang | |
| 35 | Labeling: fixed-horizon, triple-barrier, meta-labeling | De Prado AFML Ch. 3-4 | |
| 36 | Feature importance and selection for financial data | De Prado AFML Ch. 6, 8 | |
| 37 | Backtesting: walk-forward, combinatorial purged CV, avoiding biases | De Prado AFML Ch. 7, 9-12 | |
| 38 | Strategy capacity and crowding: how much capital can a signal absorb before it self-destructs | Pedersen, De Prado AFML | |
| 39 | Risk management as a system: position sizing, drawdown controls, correlation regime monitoring | Narang, Ilmanen | |
| 40 | Execution: slippage, market impact, transaction costs | Harris, Narang | |
| 41 | Strategy evaluation: Sharpe, Calmar, deflated Sharpe ratio, probabilistic Sharpe ratio | De Prado AFML Ch. 11 | |

### Phase 5: LLM + Finance
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 42 | Financial text sources: earnings calls, SEC filings (10-K/10-Q/8-K), news, social media, central bank minutes | Survey papers | |
| 43 | Domain adaptation: general LLM vs. financial LLM (FinBERT, BloombergGPT, FinGPT) — when to fine-tune vs. prompt. RAG over financial documents as an architectural pattern | Araci 2019, Wu et al. 2023, Yang et al. 2023 | |
| 44 | Hallucination and reliability: LLMs confidently misinterpret financial jargon ("dovish," "priced in") — detection and mitigation | Project experience | |
| 45 | Sentiment extraction: lexicon-based vs. LLM-based, domain calibration | FinBERT paper, Financial PhraseBank | |
| 46 | Event extraction: what happened, to whom, expected impact. Regulatory/structured text parsing | Project experience | |
| 47 | Information half-life: a news headline is stale in minutes, an earnings insight persists for days — temporal modeling of signal decay | Project experience | |
| 48 | Contradictory signals: hedge language, negation, aggregating conflicting sources | Project experience | |
| 49 | LLM as macro analyst: summarizing Fed minutes, interpreting policy signals | Project experience | |
| 50 | Text signal evaluation: apply triple-barrier labeling (concept 35) and purged CV (concept 37) to text-derived features. Measure marginal Sharpe improvement over quantitative baseline | De Prado AFML methodology | |
| 51 | Combining text signals with quantitative signals | De Prado MLA, project experience | |
| 52 | Look-ahead bias in text: publication timestamp vs. market availability time. Survivorship bias in text corpora | De Prado AFML, project experience | |

### Phase 6: Causal Inference for Finance
Primarily a diagnostic tool: understanding *why* a signal works or breaks, not discovering new alpha. Also essential for evaluating policy-driven macro trades.

| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 53 | Prediction vs. causation: why Granger causality ≠ true causality, and why this matters for signal robustness | Hamilton, Tsay | |
| 54 | Potential outcomes framework and counterfactuals | Angrist & Pischke Ch. 1-2, Cunningham | |
| 55 | Event studies: measuring abnormal returns around an event — the classic causal tool in finance | Angrist & Pischke, Campbell Lo MacKinlay | |
| 56 | Instrumental variables | Angrist & Pischke Ch. 4 | |
| 57 | Panel methods: fixed effects, two-way FE — the workhorse of empirical finance | Angrist & Pischke Ch. 5, Cunningham | |
| 58 | Difference-in-differences and synthetic control | Cunningham | |
| 59 | Structural causal models: d-separation, do-calculus, identification — the formal backbone | Pearl *Causality* Ch. 1-3, De Prado *Causal Factor Investing* | |
| 60 | Causal evaluation of LLM signals: does this text signal cause returns, or does it correlate with a confounding factor? | Project experience, De Prado CFI | |

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
    └── Phase 6 (Causal inference) ← after Phase 3; needs time series concepts
```

Phase 1 and 2 can run in parallel. Phase 5 can start early as a project — you'll revisit it with more rigor after Phase 3-4.

## Progress

- [ ] Phase 1: How the Economic Machine Works (11 concepts)
- [ ] Phase 2: Market Foundations (13 concepts)
- [ ] Phase 3: Financial Time Series (8 concepts)
- [ ] Phase 4: Systematic Strategies & Backtesting (9 concepts)
- [ ] Phase 5: LLM + Finance (11 concepts)
- [ ] Phase 6: Causal Inference for Finance (8 concepts)
