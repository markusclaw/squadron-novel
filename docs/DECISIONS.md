---
title: Decisions
status: living-log
updated: 2026-09-04
---

# Decisions

<span class="sq-status">What we decided, and — more importantly — why. Old decisions are never deleted; they are marked superseded.</span>

---

## 2026-09-04 — Repository content lives under `docs/` for the build

**STATUS:** CANON

**Decision:**
The canonical Markdown is organized under `docs/`, preserving the conceptual
organization from the build spec (foundation/, characters/, world/, history/,
mystery/, novel/, scenes/, audits/, game/, art/, exports/). The three top-level
ledgers (Canon Ledger, Decisions, Changelog) live at `docs/` root so they are
both git-visible and rendered on the site.

**Reason:**
MkDocs (and Cloudflare Pages building it) expects a single content directory.
Using `docs/` keeps the build low-maintenance and avoids fragile root-level
excludes. The spec explicitly permits adjusting technical folders while
preserving conceptual organization.

---

## 2026-09-04 — Deploy target is Cloudflare Pages; site is public-safe

**STATUS:** CANON

**Decision:**
The reading site deploys via Cloudflare Pages. Because a Cloudflare Pages URL is
public, **no genuine author-only secret answers are stored anywhere in the repo.**
Author-only material is limited to structural rules.

**Reason:**
Public exposure risk (spec §29). The White Ship's true nature does not exist as a
solved answer anyway, so nothing is lost by this constraint.

---

## 2026-09-03 — Devastation and Frontier are separate wars

**STATUS:** PROVISIONAL (→ CANON once chronology is finalized)

**Decision:**
The Devastation War occurred first and ended in an unstable armistice. The
Frontier War occurs later and forms the primary conflict of Book One.

**Reason:**
This lets Devastation function as generational trauma and creates causal
political history behind the current conflict.

**Supersedes:**
Earlier versions where the present conflict and the Devastation War were
potentially the same war.

---

## 2026-09-03 — Continuity is born from Devastation, and is not evil

**STATUS:** PROVISIONAL

**Decision:**
Continuity is a survival-outcome calculation system developed *after* Devastation,
to reduce dependence on emotion, fatigue, bias, panic, and incomplete human
judgment. It can be correct. It genuinely saves lives. It is not equivalent to
Markus.

**Reason:**
Makes the antagonistic philosophy defensible and morally serious, rather than a
"kill the evil AI" plot. Continuity opposes Greg's operational-autonomy conviction
on principle, not villainy.

**Supersedes:**
Any framing in which Continuity *caused* Devastation Day, or is an evil AI.

---

## 2026-09-03 — Markus origin: substrate, not miracle

**STATUS:** CANON

**Decision:**
Markus emerges from an ordinary written-off utility robot plus a saved legacy
runtime (M.A.R.K.U.S.), then accumulates experience and eventually self-authors.
There is no single instant of "becoming alive," and M.A.R.K.U.S. is not secretly
sentient — it is a substrate.

**Reason:**
Keeps the story out of mystical-consciousness territory and grounds Markus's
personhood in lived history and self-authorship. Also seeds the recovery motif.

---

## 2026-09-03 — The older man is admired, not a "best friend"; family is not a conspiracy

**STATUS:** CANON

**Decision:**
The young man at the House on the Hill is several years older than Greg and treats
him and Markus graciously. Greg admires him and likely overestimates the closeness.
The family is wealthy and connected but is **not** a secret conspiracy family.

**Reason:**
Preserves the "acceptance without ceremony" memory and keeps the family's warmth
un-explained rather than sinister. Prevents an over-plotted conspiracy backstory.

---

## 2026-09-03 — Young Greg and Young Markus characterization

**STATUS:** CANON

**Decision:**
Childhood Greg is a curious, earnest, gentle, socially inexperienced tween — not a
smaller cynical adult. Young Markus is not mischievous or delinquent; he trusts
Greg enormously and follows him because Greg is his social anchor. Neither yet
speaks or behaves like their adult selves.

**Reason:**
Supersedes any earlier "mini-adult" or "mischievous sidekick" writing. Sets up the
later adolescent trouble (Greg challenging rules; Markus's excessive trust) as
development, not baseline.

**Supersedes:**
Earlier drafts where childhood characters read as their adult versions.
