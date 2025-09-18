# [jmd-health-and-social-network](https://jmddatasheet-blip.github.io/jmd-health--and-social-network)

If you see a 404 when visiting the GitHub Pages URL above, the site may not be published yet or the Pages build failed.

- Repository (fallback): https://github.com/jmddatasheet-blip/jmd-health--and-social-network
- Check GitHub Pages settings: ensure Pages is enabled for the `main` branch (or the branch you want to publish) and that the site build succeeded.
- If this project uses a static site generator, make sure the build artifacts are in the configured publishing directory (for example, `gh-pages` branch or `docs/`).

If you'd like, I can add a GitHub Action workflow to build and deploy the site automatically — tell me what static site generator or build tool you use (if any), or I can add a generic `jekyll`/`plain` deploy workflow.

This repository uses Hugo. I added a GitHub Actions workflow that builds the site and deploys to GitHub Pages automatically when you push to `main`:

- Workflow file: `.github/workflows/deploy-pages.yml` (builds with Hugo and publishes the generated `public/` folder via the official Pages actions).

To use it:

1. Commit your Hugo site source to this repository (the site root should contain `config.toml`/`config.yaml` and `content/`, `layouts/`, etc.).
2. Push to `main`. The Action will run, build (`hugo --minify`) and publish the `public/` output to GitHub Pages.
3. Check Actions → Workflows in GitHub to see build logs. If the workflow fails, open the run and inspect the 'Build' step logs.

If you prefer a different deployment method or need a specific Hugo version, tell me and I can adjust the workflow.