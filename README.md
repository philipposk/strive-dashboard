# strive-dashboard

Live status page for the Strive Nordic company-mining pipeline (Denmark · Norway · Sweden).

- **Live:** https://2.6x7.gr
- Static HTML on Vercel; data in `data/*.json` is refreshed by the local miner's
  monitor (`~/strive-monitor/publish_dashboard.sh`) via `git push` — the page
  reads those JSON files from GitHub raw, so updates need no redeploy.

## Data files
- `data/status.json` — current snapshot (totals, per-country counts + enrichment coverage, workers)
- `data/history.json` — time series for the charts
- `data/events.json` — timeline events (restarts, milestones)
