# lucasdemacedo.com

Personal site of Lucas de Macedo. Plain static files, no build step.

Everything that gets published lives in `public/`:

- `public/index.html`: home page (story, work, side projects, kitchen)
- `public/racetrac.html`: RaceTrac summer 2026 case studies
- `public/apps/`: offline demos of JARVIS and the Remaining Spend dashboard (sample data, no API calls)
- `public/img/`: screenshots and kitchen photos (location data stripped)
- `public/404.html`: shown for any missing page

Hosted as a Cloudflare Worker with static assets (`wrangler.jsonc`). Every push to `main`
deploys automatically through Cloudflare's Git integration (deploy command `npx wrangler deploy`).
Only `public/` is served, so `.git`, this README and the config never reach the site.
