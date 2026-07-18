# Hackathon Control Board

Live plan, decisions, ownership, and progress for Challenge 3. Update this
file at fixed checkpoints (roughly every 45 min), not after every tiny
change. Static rules live in `CLAUDE.md`; the demo script and fallback plan
live in `DEMO.md`.

## Challenge

Redesign the patient's hospital experience to be continuous, clear,
personalized, and digitally-physically integrated — from arrival to end of
treatment.

## Target user

_TBD after slide 8._

## Core journey

_TBD after slide 8 — fill in once persona/moment/barrier/outcome are picked._

- **User / persona**:
- **Moment in their journey**:
- **Barrier**:
- **Desired outcome**:
- **The interaction that proves the insight**:

1. User enters...
2. User sees...
3. User takes action...
4. Unexpected change / intervention...
5. Resolution...
6. Summary...

## Definition of done

- [ ] Main journey works end to end, screen to screen
- [ ] Demo uses realistic fictional data (no real patient data)
- [ ] Value can be explained in one sentence
- [ ] Prototype can be reset quickly between run-throughs
- [ ] Backup screenshots/video exist (see `DEMO.md`)

## Scope

### Must have

- _(fill in once screen list is finalized)_

### Nice to have

- _(only if must-haves are done early and demo time allows)_

### Not building

- Authentication / login
- A real database
- Hospital-system integration
- Real patient data
- Production-grade AI
- Complete clinical logic
- Interfaces for every stakeholder type (one user, one journey only)
- More than one core journey

## Task board

| Task | Owner | Deadline | Status |
|---|---|---:|---|
| Finalize problem/persona (slides 1–8) | Everyone | | Not started |
| Give Claude Code the screen-by-screen spec | | | Not started |
| Build core flow | | | Not started |
| Take fallback screenshots | | | Not started |
| Prepare presentation | | | Not started |
| Test and rehearse | Everyone | | Not started |

## Branch convention

- `main` — always demo-able; merge into this only when a flow works end to end.
- `feature/person-short-task` — everything else, e.g. `feature/anna-screen2-status`.

## Decisions

_Log each non-obvious decision with a timestamp and the reason — this is
what protects the team from re-litigating choices under time pressure._

- 2026-07-18 — Tech stack: plain HTML/CSS/JS, no framework. Reason: keeps
  install/run to zero dependencies, matches `CLAUDE.md`'s fallback option.
- 2026-07-18 — Prototype code will live in a top-level `prototype/` folder
  (README's run command assumes this path). Reason: needed a concrete path
  to document `README.md`'s run command before build actually starts.
- 2026-07-18 — Branch convention: `main` + `feature/person-short-task`.
  Reason: simple enough to not need explaining mid-hackathon.

## Current blocker

None.
