# SQUADRON

A character-driven space military science-fiction novel — and the working
environment built to write it coherently.

**Development phase:** `FOUNDATION v0.2 — DECISION PASS`
**Status:** building the archive and reference site. The prose of Book One is **not** being written yet.

> A squadron is not defined by the ships flying in formation.
> It is defined by who chooses to come back for the others.

---

## What this repository is

This repo — **not** PDFs or chat transcripts — is the single source of truth for
SQUADRON. It holds the story bible, world history, character histories, master
chronology, the Book One treatment, chapter cards, and (eventually) the manuscript.

Markdown is authoritative. Everything else (the website, and any PDF / DOCX / EPUB)
is an **output** built from these files:

```
Canonical Markdown  →  repository  →  Cloudflare Pages reading site  →  exports
```

## Canon status system

Every significant story fact belongs to one of four states:

| Badge | State | Meaning |
|-------|-------|---------|
| ● | **CANON** | Accepted and authoritative |
| ◆ | **PROVISIONAL** | Current preferred direction, still changeable |
| ○ | **OPEN** | Intentionally undecided |
| × | **REJECTED** | Considered and abandoned |

Do not silently convert ideas into canon. If something isn't decided, mark it
`OPEN` or `PROVISIONAL`. Don't invent lore just to fill a file.

## Where things live (`docs/`)

| Path | Contents |
|------|----------|
| `docs/index.md` | Homepage dashboard |
| `docs/CANON_LEDGER.md` | Fast index of what is currently true |
| `docs/DECISIONS.md` | Why each architectural decision was made |
| `docs/CHANGELOG.md` | Meaningful changes over time |
| `docs/foundation/` | Premise, themes, narrative rules, current foundation, open questions |
| `docs/characters/` | Character bibles |
| `docs/world/` | Colony world, wars, Continuity, factions, military structure |
| `docs/history/` | Master timeline and the historical episodes |
| `docs/mystery/` | The White Ship and its clue ledger (no solved answers) |
| `docs/novel/book_01/` | Treatment, chronology, arcs, prose bible, pacing, chapter cards, manuscript |
| `docs/scenes/` | Free-standing scene development |
| `docs/audits/` | Continuity audits, revision queue, rejected concepts |
| `docs/game/`, `docs/art/`, `docs/exports/` | Adaptation, illustration briefs, export notes |

Book One lives entirely under `docs/novel/book_01/`.

## The reading site

Built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and
deployed on **Cloudflare Pages**, which rebuilds automatically when `main` changes.

**Build locally:**
```bash
pip install -r requirements.txt
mkdocs serve          # live preview at http://127.0.0.1:8000
mkdocs build --strict # produce ./site
```

**Cloudflare Pages build settings:**
- Build command: `pip install -r requirements.txt && mkdocs build`
- Build output directory: `site`
- Environment variable: `PYTHON_VERSION = 3.11`

See `DEPLOY.md` for the full first-deploy walkthrough (including drag-and-drop
direct upload of a pre-built site).

## Proposing changes

For any meaningful story change:

1. Update the relevant Markdown.
2. Update `docs/CANON_LEDGER.md`.
3. Append to `docs/DECISIONS.md` if it changes story architecture.
4. Update `docs/CHANGELOG.md`.
5. Check that dependent pages stay consistent.
6. Commit with a descriptive message — `story: revise Markus origin and colony childhood`, not `updates`.

Never overwrite established canon silently. Mark superseded decisions as
superseded; don't delete them.

## The questions this repo exists to answer

- What is currently true in SQUADRON?
- Why did we decide it?
- What does the reader know at this point?
- What does this character want?
- What happens next?
