# runi-hackathon-ss2026

Prototype for Challenge 2 — smart management of ambulatory patients,
across the pre-arrival-to-follow-up journey. Built at the RUNI Innovation
Hackathon SS2026.

## Installation

No installation or dependencies required. The prototype is plain
HTML/CSS/JS — no npm, no build step, no package manager.

## Run

From the repo root, serve the `prototype/` folder with a local static
server (opening `index.html` directly via `file://` will break the
scenario-data fetch — see Troubleshooting):

```
python3 -m http.server 5173 --directory prototype
```

Then open http://localhost:5173/ in a browser. Use the browser's
device toolbar / responsive mode to preview at mobile width, since the
demo is designed and presented as a mobile-sized prototype.

## Required software versions

- Python 3.8+ (ships with macOS/Linux; used only to run the local static
  server above — `python3 --version` to check)
- Any current evergreen browser (Chrome, Safari, or Edge, last 2 major
  versions)

## Important links

- Challenge brief (Hebrew, original): `00_Overview/challenge2_theask.pdf`
- Live control board (scenario, scope, task board, decisions): `HACKATHON.md`
- Presentation script and fallback plan: `DEMO.md`
- Static build rules and scope boundaries: `CLAUDE.md`
- Repo: https://github.com/adunietz/runi-hackathon-ss2026

## Troubleshooting

**Scenario data doesn't load / screens render blank.** This almost
always means the app was opened directly from disk (double-clicked
`index.html`, or a `file://...` URL in the address bar) instead of
through the local server. Browsers block `fetch()` of local JSON files
under `file://` due to CORS, so the scenario JSON silently fails to
load. Fix: stop, then re-open via `http://localhost:5173/` using the
`python3 -m http.server` command above.
