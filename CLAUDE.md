# RUNI Innovation Hackathon SS2026 — Challenge 2 Prototype

## Event

Innovation Hackathon for Medical Students, hosted by Sheba Medical Center (Tel
HaShomer) and the Reichman University School of Medicine. This repo is the
working directory for **Challenge 2: Smart Management of Ambulatory Patients**
(Hebrew: ניהול חכם של מטופלים אמבולטוריים; see
`00_Overview/challenge2_theask.pdf` for the original Hebrew brief).

### Challenge brief (translated summary)

- **Background**: Hospitals are treating a growing number of ambulatory
  (outpatient) patients, while clinic resources, staffing, and appointment
  availability remain limited.
- **Problem**: Not every patient needs the same level of care or the same
  visit format, yet most currently go through a similar process. This creates
  overload, long wait times, and suboptimal use of clinic resources.
- **Stakeholders (per brief)**: Patients, physicians, nurses,
  scheduling/coordination teams, and hospital management.
- **Why it matters**: Better patient prioritization can shorten wait times,
  reduce overload, improve patient experience, make better use of staff
  availability, and increase the number of patients treated without a
  significant increase in resources.
- **Constraints (per brief)**: Solutions must preserve patient safety,
  information privacy, regulatory compliance, integration with existing
  information systems, and be feasible without a significant increase in
  staff or budget.
- **Challenge question**: How can we intelligently prioritize, route, and
  manage ambulatory patients so that each patient receives the most
  appropriate level of care, while making optimal use of the hospital's
  existing resources?

### Journey framing for ideation

The official brief above is framed around prioritization/routing. This team
has chosen to explore it through the lens of the ambulatory patient's
end-to-end journey — pick **one** touchpoint below to focus the prototype on
(see Build sequence):

- הכנה לפני ההגעה — Preparation and instructions before arrival
- תיאום תורים — Appointment coordination
- הגעה ורישום — Arrival, identification, registration and check-in
- התמצאות וניווט — Navigation between clinics, exams, and treatment stations
- זמני המתנה — Waiting-time communication
- בדיקות וטיפול — Examinations and treatment, incl. coordination between
  clinical and administrative teams
- שחרור והמשך טיפול — Discharge instructions
- רצף טיפולי — Follow-up and continuity of care

**Relevant users/stakeholders for ideation** (broader than the brief's core
list above): ambulatory patients, family members/companions, medical teams,
administrative teams, hospital management, health funds and external
partners. Pick **one** for the prototype.

**Additional design constraints to weigh alongside the brief's**:
accessibility, staff workload, operational feasibility, and continuity of
care (רצף טיפולי).

## What we are building

A **browser-based, mobile-sized clickable prototype** — not a real product.
The whole point is to demonstrate one sharp insight through one journey, not
to build broad functionality.

**Scope:**
- 4–6 screens
- One fictional patient scenario
- One complete workflow / journey
- Real navigation between screens (not just static mockup images)
- One memorable change or intervention partway through the journey
- Hardcoded demonstration data (no real backend)

**Example flow shape** (not the literal content — the actual journey gets
picked at the hackathon):
`Pre-arrival prep → check-in/arrival → wait for exam → unexpected change (e.g. reprioritization/delay) → resolution → follow-up summary`

Note: the redesigned experience does not have to be a purely digital/app
solution — it may include physical, process, or staffing changes. The
clickable prototype only needs to dramatize the one moment that proves the
insight; other parts of the concept can be explained narratively in the
pitch.

### Explicitly out of scope — do NOT build

- Authentication / login
- A real database
- Hospital-system integration
- Real patient data
- Production-grade AI
- Complete clinical logic
- Interfaces for every stakeholder type (pick one user, one journey)
- More than one core journey
- Invented clinical claims, hospital statistics, or measured outcomes not
  present in the challenge brief

Anything in this list gets described in the pitch as "future integration,"
not built.

## Technical approach

- **React/Vite** if someone on the team is comfortable with frontend dev.
  **Plain HTML/CSS/JS** if not — don't reach for a framework just because.
- Hardcode the scenario data in a local JSON file (e.g. `src/data/scenario.json`
  or similar) — screens read from it, nothing is computed from real logic.
- Design and test in a **mobile viewport** the whole time; this is what will
  be presented.
- Only deploy (Vercel/Netlify/etc.) once the local flow is reliable end to
  end. Don't burn time on deployment before the demo actually works.
- **Take screenshots of every screen once the flow works**, as a fallback in
  case the live demo breaks during presentation.

## Language

Demo language is **not finalized — leaning Hebrew**. Whichever is chosen:

- If Hebrew: build with `dir="rtl"` on the relevant containers/`<html>`, and
  sanity-check that navigation, back buttons, and any directional UI (arrows,
  progress indicators) are mirrored correctly. Test with real Hebrew scenario
  copy early, not lorem-ipsum placeholders — RTL layout bugs show up with
  real text and real names.
- If English: no special handling needed beyond normal responsive/mobile
  layout.
- Whichever language is picked, keep the scenario JSON's text fields in that
  one language only — don't build bilingual toggling, it's out of scope.

## Build sequence — do not skip ahead

This is a hackathon with a structured pitch deck; **building only starts
after slide 8**. Before writing any prototype code, the team should have
already nailed down, in order:

1. **Identify the highest-value problem** within the challenge brief above.
2. **Define the user, moment, barrier, and desired outcome** — one specific
   persona, one specific moment in their ambulatory patient journey, what's
   blocking them, what "better" looks like.
3. **Choose the interaction that proves the insight** — the one moment in the
   flow that makes the audience get it. This is usually the "unexpected
   change / intervention" screen.
4. **Give the coding tool (Claude Code) a tightly bounded specification** —
   concrete screen list, concrete scenario data, concrete copy. Vague specs
   burn hackathon time.
5. **Build only that flow.** No extra screens, no extra states, no "while
   we're at it."

When the team is ready to build, fill in the `## Core journey` and `## Scope`
sections of `HACKATHON.md` (or hand the concrete answers to Claude Code
directly) with the answers to steps 1–3, then ask for the screen-by-screen
spec before generating code.

## Scenario

Live scenario details (persona, moment, barrier, desired outcome, screen
list) are tracked in `HACKATHON.md`, not here — that file is the one to
update once slide 8 is done. This file stays static.

## Repo layout

- `00_Overview/` — challenge brief and event materials (reference only, don't
  edit). `00_Overview/Old/` holds superseded material from the previous
  challenge assignment.
- `01_Ideation/` — ideation workbooks (Google Slides/Docs shortcuts)
- `02_Final Deck/` — final pitch deck (Google Slides shortcut)
- Prototype code goes in a new top-level folder created at build time (e.g.
  `prototype/` or `src/`) — keep it separate from the overview/ideation
  materials above

## Working notes for Claude Code

- This is a time-boxed hackathon build. Optimize for a reliable demo, not
  production readiness.
- Keep implementation minimal and literal to the agreed screen list — this
  document's "do NOT build" list is a hard boundary, not a suggestion.
- Prefer finishing a rough end-to-end click-through over polishing any single
  screen — a complete ugly flow beats a beautiful incomplete one for the demo.
- Don't add tests, CI, linting setup, or tooling scaffolding — there's no time
  budget for it and it's not what's being judged.
- Don't add features or screens beyond what's recorded in `HACKATHON.md`'s
  scope section — if it's not on the "must have" list, it's not in scope.
- Before declaring a build task complete, run the app and click through the
  demo journey — don't rely on a type check or a glance at the code.
- Preserve working functionality when making changes late in the build —
  a regression right before the demo is worse than a missing nice-to-have.
- Don't assume the solution has to be an app or purely digital — the
  prototype demonstrates one moment of a broader concept that may include
  physical/process changes; don't force every stakeholder interaction into
  a screen just because the deliverable is a clickable prototype.
- Don't invent clinical claims, hospital statistics, or measured outcomes.
  If a number or claim isn't in the challenge brief or `HACKATHON.md`, leave
  it out or mark it as illustrative/fictional in the copy.

## Live tracking

- `HACKATHON.md` — the live control board: scenario, scope, task ownership,
  decisions, and current blockers. Update it, not this file.
- `DEMO.md` — the presentation script and fallback/recovery plan.

@HACKATHON.md
@DEMO.md
