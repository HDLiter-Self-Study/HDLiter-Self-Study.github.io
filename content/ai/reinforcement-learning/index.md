---
title: Reinforcement Learning — Learning Roadmap
date: 2026-04-02
lastmod: 2026-04-02
tags:
  - ai
  - reinforcement-learning
  - roadmap
draft: false
---

## Overview

Reinforcement learning as a separate paradigm from supervised/unsupervised learning: sequential decision-making under uncertainty. From tabular foundations through deep RL to modern applications (RLHF, game-playing, robotics).

Prerequisites: [[mathematics/probability/index|probability theory]] (at least Phase 1) + [[mathematics/linear-algebra/index|linear algebra]]. For Phase 4 (theory): [[ai/machine-learning/index|ML theory]] Phase 2 (generalization bounds).

## Resources

### Textbooks
| Book | Level | Style | Free? |
|------|-------|-------|-------|
| **Sutton & Barto, *RL: An Introduction*** (2nd ed.) | Intro–intermediate | The standard. Intuitive, broad, well-paced. MDPs, TD, policy gradient, function approximation | [Free PDF](http://incompleteideas.net/book/the-book-2nd.html) |
| **Agarwal, Jiang, Kakade, Sun, *RL: Theory and Algorithms*** | Advanced theory | The most rigorous treatment: PAC bounds, sample complexity, exploration, linear function approximation theory | [Free PDF](https://rltheorybook.github.io/) |
| **Lattimore & Szepesvári, *Bandit Algorithms*** | Advanced | Comprehensive bandits (stochastic, adversarial, linear, combinatorial). Essential for exploration theory | [Free PDF](https://tor-lattimore.com/downloads/book/book.pdf) + [solutions](https://tor-lattimore.com/downloads/book/solutions.pdf) |
| **Szepesvári, *Algorithms for RL*** | Graduate | 100 pages, concise, convergence proofs and sample complexity | [Free PDF](https://sites.ualberta.ca/~szepesva/papers/RLAlgsInMDPs.pdf) |
| **Bertsekas, *A Course in RL*** (2nd ed., 2024) | Intermediate | DP/optimal control perspective, 421 pages | [Free PDF](https://www.mit.edu/~dimitrib/RLCOURSECOMPLETE%202ndEDITION.pdf) |

### Courses

| Course | Instructor | Year | Focus | Video |
|--------|-----------|------|-------|-------|
| **David Silver RL Course** | Silver (DeepMind) | 2015 | Classic conceptual intro: MDPs, DP, MC, TD, FA, policy gradient | [YouTube (10 lec)](https://www.youtube.com/playlist?list=PLqYmG7hTraZDM-OYHWgPebj2MfCFzFObQ) |
| **DeepMind x UCL RL** | van Hasselt et al. | 2021 | Updated: adds deep RL, distributional RL, agents | [YouTube (13 lec)](https://www.deepmind.com/learning-resources/reinforcement-learning-lecture-series-2021) |
| **Stanford CS234** | Brunskill | 2024 | MDPs, TD, policy gradient, exploration, offline RL, DPO | [YouTube](https://youtube.com/playlist?list=PLoROMvodv4rN4wG6Nk6sNpTEbuOSosZdX) |
| **UC Berkeley CS285** | Levine | 2023 | Deep RL focus: actor-critic, model-based, offline RL, RL for LLMs | [YouTube](https://www.youtube.com/playlist?list=PL_iWQOsE6TfX7MaC6C3HcdOf1g337dlC9) |

## Roadmap

### Phase 1: Foundations (Tabular)
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 1 | Markov decision processes: states, actions, rewards, transitions | S&B Ch. 3, Silver lec 2 | |
| 2 | Bellman equations (expectation and optimality) | S&B Ch. 3, Silver lec 2-3 | |
| 3 | Dynamic programming: policy evaluation, policy iteration, value iteration | S&B Ch. 4, Silver lec 3 | |
| 4 | Monte Carlo methods | S&B Ch. 5, Silver lec 4 | |
| 5 | Temporal difference learning: TD(0), SARSA, Q-learning | S&B Ch. 6, Silver lec 4-5 | |
| 6 | n-step methods and eligibility traces | S&B Ch. 7, 12 | |
| 7 | Exploration vs exploitation: ε-greedy, UCB, Thompson sampling | S&B Ch. 2, Lattimore Ch. 1-7 | |

### Phase 2: Function Approximation and Deep RL
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 8 | Value function approximation: linear, neural | S&B Ch. 9-10, Silver lec 6 | |
| 9 | Deep Q-Networks (DQN) and replay buffers | CS285, DeepMind 2021 | |
| 10 | Policy gradient theorem | S&B Ch. 13, Silver lec 7, CS234 | |
| 11 | REINFORCE and variance reduction (baselines) | S&B Ch. 13, CS285 | |
| 12 | Actor-critic methods: A2C, A3C, PPO | CS285, CS234 | |
| 13 | Deterministic policy gradient and DDPG/TD3/SAC | CS285 | |

### Phase 3: Advanced Methods
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 14 | Model-based RL: world models, Dyna, MuZero | S&B Ch. 8, CS285 | |
| 15 | Offline / batch RL: CQL, IQL, decision transformer | CS285, CS234 (2024) | |
| 16 | Inverse RL and reward learning | CS285 | |
| 17 | RLHF and direct preference optimization (DPO) | CS234 (2024), CS336 | Links to [[ai/deep-learning/index|DL Phase 4]] |
| 18 | Multi-agent RL (introduction) | DeepMind 2021 | |

### Phase 4: Theory
| # | Concept | Sources | Concept Notes |
|---|---------|---------|---------------|
| 19 | Sample complexity of tabular RL | AJKS Ch. 1-5 | |
| 20 | PAC bounds for exploration | AJKS Ch. 6-8 | |
| 21 | Linear function approximation theory | AJKS Ch. 9-13, Szepesvári | |
| 22 | Regret bounds for bandits (stochastic and adversarial) | Lattimore Ch. 4-12 | |
| 23 | Contextual bandits and linear bandits | Lattimore Ch. 18-22 | |

## Progress

- [ ] Phase 1: Foundations
- [ ] Phase 2: Function Approximation and Deep RL
- [ ] Phase 3: Advanced Methods
- [ ] Phase 4: Theory
