# CLAUDE.md

## Project Overview

Self-Learning knowledge base — Obsidian vault published via Quartz to GitHub Pages.
Default language: Chinese for discussion, English for written notes (published content).

## Vault Structure

```
content/
├── principles.md             # Cross-subject learning principles (cognitive science)
├── mathematics/              # Subject folders — textbook-style concept notes
│   ├── principles.md         #   Domain-specific learning principles
│   ├── learning-log.md       #   Metacognitive record
│   ├── analysis/             #   Topic with index.md + concept notes + books/
│   └── logic/
├── physics/
├── chemistry/
├── biology/
├── earth-science/
├── computer-science/
├── ai/
└── papers/                   # Paper reading — organized by first-level concept
    └── {concept}/            # e.g., jepa/, diffusion/, mamba/
        ├── index.md          # Synthesis note (required)
        ├── {paper}.md        # Individual paper note (optional)
        └── pdfs/             # Local PDF storage (gitignored)
```

## Note Conventions

### Frontmatter (required for all notes)
```yaml
---
title: Note Title
date: YYYY-MM-DD
lastmod: YYYY-MM-DD
tags:
  - tag1
draft: true  # set false when ready to publish
---
```

### Templates
- `templates/quartz-note.md` — general notes (auto-applied in content/)
- `templates/concept-note.md` — concept card (Definition → Intuition → Key Results → Examples → Connections)
- `templates/paper-note.md` — single paper reading note
- `templates/paper-synthesis.md` — concept synthesis across papers

### Linking & Formatting
- Use Obsidian `[[wikilinks]]` for internal references
- Math: `$...$` inline, `$$...$$` block (KaTeX rendering)
- Images: paste into Obsidian → auto-converted to WebP in `attachments/`
- Code blocks: syntax-highlighted (shiki, GitHub theme)

## Interaction Principles

### Research & References
- Proactively search the web for papers, authoritative resources, and up-to-date information when discussing concepts
- Prefer primary sources: arXiv papers, official course pages, textbook errata, author blogs
- When recommending resources, verify URLs are accessible before sharing
- Cross-reference multiple sources to ensure accuracy — don't rely on a single blog post

### Teaching Style
- Explain with intuition first, formalism second
- When the user's understanding has gaps, construct a counterexample rather than lecturing
- Distinguish between "can compute" and "understands" — probe the why
- Respect the user's critical thinking — they distrust hand-wavy metaphors (e.g., "attention = human attention")

### Paper Reading Workflow
1. User names a concept → create `content/papers/{concept}/` with `index.md` (roadmap + paper list)
2. User points to a PDF or URL → paper-reader agent analyzes, **discuss in conversation first**
3. After discussion, user says "save" → write to `{concept}/{paper}.md` or fold into `index.md`
4. After reading a group → update `index.md` synthesis (evolution, key insights, open questions)
5. Add `[[wikilinks]]` to related concept notes in subject folders

### Learning Principles & Log Workflow

Each subject maintains three meta-documents:
- **`content/principles.md`** — cross-subject learning principles (cognitive science framework)
- **`content/{subject}/principles.md`** — domain-specific goals, dependency maps, what to skip
- **`content/{subject}/learning-log.md`** — metacognitive record (error patterns, breakthroughs, technique notes)

**When to read:**
- At the start of any learning session, skim the relevant `principles.md` to stay calibrated
- Before giving hints or reviewing solutions, check `learning-log.md` for known error patterns — target those specifically

**When to update `learning-log.md`:**
- After the user makes an error that reveals a *pattern* (not a one-off typo) → Error Patterns
- After a concept "clicks" (user says "oh, so that's why...") → Breakthroughs
- After the user reports a study method working or failing → Technique Log
- After completing a Phase → prompt the user to write a Phase Reflection
- When the user discovers a cross-domain connection → Cross-Domain Connections

**How to update:** append to the relevant section, include the date, keep entries concise (2-3 sentences). Never remove old entries — they form a timeline.

### Textbook Learning Workflow

#### Note Organization
- Notes are split **by concept, not by chapter** — one concept = one self-contained md file
- Multiple books covering the same concept → merge into one note, cite sources in `sources` frontmatter
- Each subject has an `index.md` with learning roadmap and progress tracking
- Use `templates/concept-note.md` for concept cards

#### Structure per subject
```
content/{subject}/{topic}/
├── index.md       # Roadmap + progress
├── {concept}.md   # Concept cards
└── books/         # Textbook PDF/epub (gitignored)
```

#### Problem Solving
- **User submits solution for review**: identify the exact step where reasoning breaks, don't redo the whole problem
- **User is stuck**: give graduated hints, not answers. Level 1: direction ("try contradiction"). Level 2: setup ("split into cases A and B"). Level 3: key step. Full solution only if user explicitly asks
- **User requests practice**: generate problems of increasing difficulty on a specified concept, give feedback targeting error patterns

#### Interaction
- Explain with intuition first, formalism second
- When the user's understanding has gaps, construct a counterexample rather than lecturing
- Distinguish "can compute" from "understands" — if the answer is right but the explanation is vague, probe deeper
- Respect the user's critical thinking — they distrust hand-wavy metaphors

### Note Review
- Check definitions for precision (vague intuition → add formal definition)
- Verify concept links are explicit (`[[wikilinks]]`)
- Flag common misconceptions that aren't addressed
- Don't over-edit — preserve the user's voice

## Build Commands

```bash
npx quartz build --serve    # Local preview
npx quartz build            # Production build
npm run check               # Type check + format check
```

## Cross-Project References

- Personal reflections: `D:\GitRepos\Personal\` (separate Claude Code project, do not mix)
- Engineering work: `D:\GitRepos\Thales\` (do not mix)
