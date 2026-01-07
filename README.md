

# LDHF-001 — AI + Money: Physical Rules (Experiment)

## Experiment ID
LDHF-001

## Experiment period
10 days (Day 1 – Day 10)
⚠️ Timebox: End at Day 10. No extensions.

## Goal (one sentence)
Within 10 days, deliver a public document titled "AI + Money: 5 Incidents → 10 Physical Rules" and have it seen by at least one external person.

## Unique deliverable (third-party visible, independently hostable, allowed to be rough)
- A single public document: `README.md` (root) + supporting files under `docs/`.
- Final public URL must exist on GitHub (repo public) by Day 1 and updated every day by commit.

## Allowed failure conditions (still count as experiment success)
- The document is messy or incomplete.
- No stars/likes/comments on GitHub.
- Personal judgment: "it's ugly" or "not ready".

---

## Where to store content
- Root README contains experiment metadata and link to `docs/`.
- Accident descriptions and extracted rules go under `docs/` as separate markdown files (one file per incident).
  - `docs/the_dao_en.md`
  - `docs/flashloan_en.md`
  - `docs/governance_attack_en.md`
  - `docs/liquidation_chain_en.md`
  - `docs/agent_misdecision_en.md`

**Do NOT** keep the full accident narrative only inside README. README is orchestration & index; accident bodies live in `docs/` files.

---

## Publishing rules (must obey)
1. Repository MUST be public on Day 1.
2. Commit at least once per day. Commit message must include `Day X` (e.g., "Day 2 — add The DAO rules translation").
3. Do not postpone publishing until "better". Publish the rough version immediately.
4. Do not expand scope (no extra incidents, no structural changes).
5. No rewriting entire history—use forward commits only.

---

## Daily MDP (30–60 minutes)
Each day, perform exactly one Minimal Doable Product (MDP) action and commit:
- Day 1: Create repo + push initial `README.md` minimal (link to docs folder).
- Day 2: Add `docs/the_dao_en.md` (translation + extracted rules) and commit.
- Day 3–9: Add each incident file or rules increments.
- Day 10: Consolidate into final `README.md` and publish final link.

Checkboxes (manually tick in README after commit):
- [ ] Day 1
- [ ] Day 2
- ...
- [ ] Day 10

---

## Day 10 mandatory closeout (must complete)
1. Public deliverable URL (paste below).
2. Short facts-only record of what happened and whether anyone saw it.
3. Keep improvement small: change only one parameter next run.

---

## Acceptance criterion (single rule)
- If there exists a public deliverable URL (repo + docs), experiment succeeded.
- Feelings, judgments, and perceived quality are irrelevant.

---

## Minimal repo structure (do not change)
