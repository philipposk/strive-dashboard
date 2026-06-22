# strive-dashboard

Live status page for the Strive Nordic company-mining pipeline (Denmark · Norway · Sweden).

- **Live:** https://2.6x7.gr (served by **GitHub Pages** from `main`)
- Static HTML; data in `data/*.json` is refreshed by the local miner's
  monitor (`~/strive-monitor/publish_dashboard.sh`) via `git push` — the page
  reads those JSON files from GitHub raw, so updates need no redeploy.
- Note: a Vercel project (`strive-dashboard`) is also wired to this repo but is
  unused (2.6x7.gr is GitHub Pages). `vercel.json` skips Vercel builds on
  data-only pushes so they don't burn the account-wide daily deploy limit.

## Data files
- `data/status.json` — current snapshot (totals, per-country counts + enrichment coverage, workers)
- `data/history.json` — time series for the charts
- `data/events.json` — timeline events (restarts, milestones)
