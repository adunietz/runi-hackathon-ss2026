# RUNI Innovation Hackathon SS2026 — Challenge 3 Prototype

## Event

Innovation Hackathon for Medical Students, hosted by Sheba Medical Center (Tel
HaShomer) and the Reichman University School of Medicine. This repo is the
working directory for **Challenge 3: Patient Experience in the Hospital — From
Today to the Hospital of the Future** (see `00_Overview/challenge3_theask.pdf`
for the original Hebrew brief).

### Challenge brief (translated summary)

- **Background**: The modern hospital is a complex system where patients,
  families, and staff move between many spaces, processes, and services.
  Beyond the medical treatment itself, the experience of the stay — from the
  first moment to discharge — directly shapes the patient's sense of safety,
  understanding, cooperation, and trust in the system.
- **Problem**: Patient experience today is fragmented, not always intuitive,
  and often comes with uncertainty, long waits, difficulty finding your way,
  and no real-time information. The patient journey needs to be redesigned to
  be continuous, clear, personalized, and accessible — even in a complex,
  high-load environment.
- **Stakeholders**: Hospitalized patients, ambulatory patients, family
  members/companions, medical and nursing staff, logistics teams, patient
  experience/service/operations staff, medical information systems, hospital
  management.
- **Why it matters**: Better patient experience isn't just "comfort" — it
  affects care quality, patient compliance with medical instructions, error
  reduction, staff efficiency, and how trustworthy and advanced the hospital
  is perceived to be.
- **Constraints**: Solutions must be workable in a complex real medical
  environment, safe, compliant with regulation and privacy, integrable with
  existing systems, and must not add burden to already-overloaded staff.
- **Challenge question**: How can we redesign the patient's hospital
  experience to be continuous, clear, personalized, and digitally-physically
  integrated — from arrival to end of treatment — building the "hospital of
  the future" already today?

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
`Start → current status → next instruction → unexpected change → resolution → summary`

### Explicitly out of scope — do NOT build

- Authentication / login
- A real database
- Hospital-system integration
- Real patient data
- Production-grade AI
- Complete clinical logic
- Interfaces for every stakeholder type (pick one user, one journey)
- More than one core journey

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
   persona, one specific moment in their hospital journey, what's blocking
   them, what "better" looks like.
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
  edit)
- `01_Ideation/` — ideation workbooks (Google Slides shortcuts)
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

## Live tracking

- `HACKATHON.md` — the live control board: scenario, scope, task ownership,
  decisions, and current blockers. Update it, not this file.
- `DEMO.md` — the presentation script and fallback/recovery plan.

@HACKATHON.md
@DEMO.md
