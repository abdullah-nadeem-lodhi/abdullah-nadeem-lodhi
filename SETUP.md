# Setup Checklist

Follow these steps in order — most badges will work immediately, a couple need one-time setup.

## 1. Create the special profile repository
GitHub only renders a profile README if the repo is:
- **Public**
- Named **exactly** your username → `abdullah-nadeem-lodhi/abdullah-nadeem-lodhi`

If it doesn't exist yet, create it at `https://github.com/new` using that exact name, then
upload everything in this package (`README.md`, `assets/`, `.github/`) to the repo root.

## 2. Works immediately, no setup required
These all pull live data purely from your public GitHub username — nothing to configure:
- Animated typing intro (readme-typing-svg)
- Tech stack icons (skillicons.dev)
- GitHub Stats & Top Languages (github-readme-stats)
- GitHub Streak (streak-stats)
- Activity Graph (github-readme-activity-graph)
- GitHub Trophies (github-profile-trophy)
- Visitor counter (komarev)
- Custom banner.svg / waves.svg (local files, no dependencies)

## 3. Contribution Snake — needs the workflow to run once
`.github/workflows/snake.yml` is already wired up.
1. Push this repo to GitHub.
2. Go to the **Actions** tab → run **"Generate Snake Animation"** manually the first time
   (`workflow_dispatch`), or just wait for the next scheduled run.
3. This creates an `output` branch containing the SVG/GIF files that `README.md` already
   references — no README edits needed.

## 4. Extended Metrics — optional, needs a token
`.github/workflows/metrics.yml` and the collapsible "Extended Metrics" section in
`README.md` are **optional**. To enable:
1. Create a classic Personal Access Token with `read:user` and `repo` scopes.
2. In this repo: **Settings → Secrets and variables → Actions → New repository secret**,
   name it `METRICS_TOKEN`, paste the token.
3. Run the **"Generate Profile Metrics"** workflow once manually.

If you'd rather skip this, delete `.github/workflows/metrics.yml` and the "Extended
Metrics" `<details>` block in `README.md` — nothing else depends on it.

## 5. Fill in the TODOs
Search `README.md` for `TODO` — there are placeholders for:
- Your email address (2 spots)
- Portfolio URL / Twitter handle (or delete the badges you don't use)
- AI Engineering project (currently a tasteful placeholder — no AI/ML repos were public
  at generation time)
- Deployment platform, once you deploy a project
- Figma/design links, if you formalize a design workflow

## 6. Optional polish
- Swap `theme=github_dark` / `theme=github-compact` params on the stats/activity-graph
  URLs if you want a different look — full theme lists are in each project's own docs
  (github-readme-stats, github-readme-activity-graph).
- Trophy `theme=algolia` can be swapped for `onedark`, `dracula`, etc.
