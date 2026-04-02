# CLAUDE.md

## Project Overview

Self-Learning knowledge base — Obsidian vault published via Quartz to GitHub Pages.
Default language: Chinese for discussion, English for written notes (published content).

## Vault Structure

```
content/
├── mathematics/          # Subject folders — textbook-style concept notes
├── physics/
├── ai/
├── psychology/
├── creative-writing/
└── papers/               # Paper reading — organized by first-level concept
    └── {concept}/        # e.g., jepa/, diffusion/, mamba/
        ├── index.md      # Synthesis note (required) — concept overview, paper relationships
        ├── {paper}.md    # Individual paper note (optional) — only for complex papers
        └── pdfs/         # Local PDF storage (gitignored)
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
