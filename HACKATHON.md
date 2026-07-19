# Hackathon Control Board

Live plan, decisions, ownership, and progress for Challenge 2. Update this
file at fixed checkpoints (roughly every 45 min), not after every tiny
change. Static rules live in `CLAUDE.md`; the demo script and fallback plan
live in `DEMO.md`.

## Challenge

**Challenge 2: Smart Management of Ambulatory Patients**
(Hebrew: ניהול חכם של מטופלים אמבולטוריים)

**Description (Hebrew, as agreed for this project):**
כיצד ניתן לייצר מסע חכם, רציף וברור למטופלים אמבולטוריים — משלב ההכנה לפני
ההגעה, דרך ההתמצאות, הרישום, ההמתנה, הבדיקות והטיפול, ועד לשחרור ולהמשך
המעקב — תוך שיפור התיאום בין המטופלים, הצוותים הרפואיים והמערכות
התפעוליות?

**English (working translation):** How can we create a smart, continuous,
and clear journey for ambulatory patients — from pre-arrival preparation,
through wayfinding, registration, waiting, examinations and treatment, to
discharge and follow-up — while improving coordination between patients,
medical teams, and operational systems?

The official brief (`00_Overview/challenge2_theask.pdf`) frames the
challenge as smart prioritization/routing of ambulatory patients; the
description above is how this team has scoped it into a journey for
ideation. See `CLAUDE.md` § Challenge brief for the literal brief text.

## Ambulatory patient journey (candidate touchpoints)

Pick **one** moment from this list to build the prototype around (see
`CLAUDE.md` § Build sequence) — this is the menu to choose from, not the
full scope of the demo:

- הכנה לפני ההגעה — Preparation and instructions before arrival
- תיאום תורים — Appointment coordination
- הגעה ורישום — Arrival and identification, registration and check-in
- התמצאות וניווט — Navigation between clinics, examinations and treatment
  stations
- זמני המתנה — Waiting-time communication
- בדיקות וטיפול — Examinations and treatment, incl. coordination between
  clinical and administrative teams
- שחרור והמשך טיפול — Discharge instructions
- רצף טיפולי — Follow-up and continuity of care

## Target user

_TBD after slide 8._

## Target stakeholders

- מטופלים אמבולטוריים — Ambulatory patients
- Family members and companions
- צוותים רפואיים ומנהליים — Medical teams
- Administrative teams (scheduling/coordination)
- Hospital management
- Health funds and external partners

Pick **one** as the prototype's user — see `CLAUDE.md`'s out-of-scope list
(no interfaces for every stakeholder type).

## Design constraints

- Accessibility
- Privacy and data security
- Clinical safety
- Integration with hospital systems
- Staff workload
- Operational feasibility
- Continuity of care (רצף טיפולי)

## Success criteria

- [ ] One sharp insight is demonstrable in a single click-through
- [ ] The prototype visibly addresses a concrete wait-time, coordination, or
      mismatched-care-level problem for one scenario
- [ ] Judges can restate the value proposition after the demo without
      prompting
- [ ] No real patient data, invented clinical statistics, or measured
      outcomes appear anywhere in the demo or pitch

## Expected hackathon deliverables

- Finalized persona/moment/barrier/outcome (this file, § Core journey)
- Clickable 4–6 screen prototype (see `CLAUDE.md` § What we are building)
- Fallback screenshots/recording (`DEMO.md`)
- 3-minute final pitch deck (`02_Final Deck/`)

## Three-minute final pitch structure

1. **Problem** (~30s) — the ambulatory patient management challenge,
   framed through the one persona/moment this team picked.
2. **Insight** (~30s) — the barrier, and why it's the highest-value moment
   to fix.
3. **Demo** (~90s) — live click-through of the prototype, from the start
   through the unexpected change to resolution.
4. **Impact** (~30s) — expected impact in one sentence, no invented
   statistics (see `CLAUDE.md` § Working notes).

## Hebrew terminology (keep consistent across the project)

| Hebrew | Use for |
|---|---|
| מטופלים אמבולטוריים | Ambulatory patients |
| מסע המטופל | Patient journey |
| הכנה לפני ההגעה | Pre-arrival preparation |
| תיאום תורים | Appointment coordination |
| הגעה ורישום | Arrival and registration |
| התמצאות וניווט | Wayfinding / navigation |
| זמני המתנה | Waiting times |
| בדיקות וטיפול | Examinations and treatment |
| שחרור והמשך טיפול | Discharge and continued care |
| רצף טיפולי | Continuity of care |
| צוותים רפואיים ומנהליים | Medical and administrative teams |

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
- Invented clinical claims, hospital statistics, or measured outcomes

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
- 2026-07-19 — Challenge assignment changed from Challenge 3 (patient
  experience in the hospital) to Challenge 2 (smart management of
  ambulatory patients). Reason: updated challenge assignment for the event.
  All Challenge 3-specific content in `CLAUDE.md`/`HACKATHON.md` has been
  superseded; `00_Overview/Old/` holds the retired brief for reference.
  Persona/moment/barrier/outcome below reset to TBD and need re-filling.

## Current blocker

None.
