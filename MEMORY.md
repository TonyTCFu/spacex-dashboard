# MEMORY.md

## Project
SpaceX (SPCX) tracking dashboard.
Fixed public URL: https://tonytcfu.github.io/spacex-dashboard/
Repo: https://github.com/TonyTCFu/spacex-dashboard (public, `main` branch, root `index.html`)

## Facts
- SpaceX listed on Nasdaq as SPCX on 2026-06-12 (per in-conversation web research on 2026-09-27).
- The page is a static research snapshot; everything except the quote-refresh button updates on a fixed schedule (Tue–Sat ~07:40 Asia/Shanghai).
- The "refresh quote" button fetches a stooq delayed quote (~15 min) client-side and auto-refreshes once on load during NYSE hours (Mon–Fri 09:30–16:00 ET).
- FINRA Equity Short Interest is the source for short data (latest settlement at time of writing: 2026-09-15, 162.25M shares, -6.55% vs prior period).
- Caution: before 2026-06-15 the SPCX symbol belonged to "The SPAC and New Issue ETF"; older FINRA short-interest history is not comparable.
- Borrow fee / utilization have no free public source; the page shows a heuristic "easy to borrow" estimate, explicitly labeled as an estimate.

## Decisions
- The muse.ai PWA shell controls the add-to-homescreen icon; page-level manifest cannot override it. The GitHub Pages URL is the canonical fixed link.
- Every data value stays cited; unverified items stay labeled and are never merged into single "certain" values.
