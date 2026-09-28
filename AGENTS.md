# AGENTS.md

Single-page static dashboard (SpaceX / SPCX tracker) deployed via GitHub Pages.

## Rules
- `index.html` is the entire site. It is generated: do not hand-edit the deployed copy; edit the source artifact and re-export.
- Deploy = overwrite `index.html` on the `main` branch root. GitHub Pages serves from `main` / `(root)`. No build step.
- Keep the page self-contained (inline CSS/JS, data URIs). No external JS libraries.
- Live quotes: client-side fetch of the stooq CSV quote endpoint (delayed ~15 min). Never claim tick-level real time.
- Borrow fee / utilization: no free public source exists. The page shows FINRA short interest (measured) plus a clearly labeled heuristic borrow-difficulty estimate. Never present the estimate as a measured rate.
- Page copy in Chinese; code, comments, and commit messages in English.
- Cite every data point with source link and date. Distinguish verified facts, estimates, and unverifiable items; never merge conflicting calibers into one "certain" value.
- No secrets in the repo. No destructive git operations (no hard reset, no force push).
