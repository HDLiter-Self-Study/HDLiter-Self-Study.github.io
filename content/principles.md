---
title: Self-Learning Principles
date: 2026-04-02
lastmod: 2026-04-02
tags:
  - meta-learning
draft: false
---

General learning principles grounded in cognitive science. These apply across all subjects in this vault. Each subject also has its own `principles.md` with domain-specific guidance.

## Goals

Two motivations that reinforce each other:

1. **Intellectual depth** — build structural understanding from foundations upward, because shallow knowledge decays and genuine comprehension is intrinsically rewarding.
2. **Career preparation (AI direction)** — mathematics, natural sciences, and formal methods form the backbone of modern AI research. Depth in (1) directly serves (2).

The risk to avoid: optimizing for either goal alone. Pure interest drifts into rabbit holes; pure career prep becomes a checklist of half-understood topics. The test: *can I use this knowledge to think, not just to cite?*

## Principles from Cognitive Science

### 1. Generate before you consume (generation effect)
Attempt the problem, proof, or explanation *before* reading the answer. Struggling and failing produces stronger encoding than passive reading, even if the attempt is wrong.

### 2. Test to learn, not to assess (testing effect)
Retrieval practice is not just measurement — it is the most powerful learning event. Formalizing in Lean 4, doing problem sets, explaining to Claude — these are learning, not just evaluation.

### 3. Space and interleave (spaced retrieval + interleaving)
Massing practice on one topic feels productive but produces fragile knowledge. Interleave subjects within the same week. When a Phase is "done," revisit key results during the next Phase.

### 4. Write to connect (elaborative encoding)
A note is not a summary — it is an act of connecting new knowledge to existing knowledge. The `Connections` section in concept notes exists for this reason. Never leave it empty.

### 5. Difficulty is signal, not failure (desirable difficulty)
If everything is easy, you're reviewing, not learning. The optimal zone: you can eventually solve it, but not immediately. Set a struggle threshold (e.g., 20 minutes) before seeking help.

### 6. Explain to expose gaps (Feynman technique)
If you can't explain a concept in plain language without jargon, you don't understand it. Discuss with Claude *before* writing the formal note.

## When to Move On

A topic is "done enough" when you can answer YES to at least two of:

1. **Explain:** Can I explain the core idea without the textbook?
2. **Prove/Verify:** Can I produce a rigorous proof (on paper or in a proof assistant)?
3. **Connect:** Can I relate this to at least two other concepts?
4. **Apply:** Can I use this to solve a problem I haven't seen before?

## Per-Subject Documents

Each subject maintains:
- **`{subject}/principles.md`** — domain-specific goals, dependency maps, what to skip
- **`{subject}/learning-log.md`** — error patterns, breakthroughs, technique notes, phase reflections
- **`{subject}/index.md`** — roadmap and progress tracking
