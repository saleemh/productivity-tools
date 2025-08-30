# Repository Guidelines

## Project Structure & Organization
- `docs/`: Markdown content (add pages here). Use `docs/assets/` for images.
- `mkdocs.yml`: Site configuration, theme, and navigation.
- `.github/workflows/deploy.yml`: CI build and rsync deploy.
- `deploy/nginx/`: Example Nginx location config.
- `requirements.txt`: Python deps for MkDocs/Material.
- `site/`: Build output (generated; do not commit).

## Build, Serve, and Deploy
- Install: `python -m pip install -r requirements.txt`
- Serve locally: `mkdocs serve` (open http://127.0.0.1:8000)
- Build: `mkdocs build --strict` (outputs to `site/`)
- CI deploy: pushes to `main`/`master` build and rsync to `${SSH_TARGET_DIR}` using secrets (`SSH_HOST`, `SSH_USER`, `SSH_KEY`, `SSH_TARGET_DIR`, optional `SSH_PORT`).
- Manual test deploy (optional): `rsync -az --delete site/ user@host:/var/www/productivity-tools/`

## Content Style & Naming
- Write in clear, concise Markdown. Prefer sentence‑case headings.
- One `# H1` per page; subsequent sections use `##`/`###`.
- Use relative links and paths under the `/productivity-tools/` prefix.
- Place images in `docs/assets/`; name files with kebab‑case (e.g., `keyboard-shortcuts.png`).
- Page filenames: kebab‑case (e.g., `index.md`, `shortcuts.md`).
- Keep navigation in `mkdocs.yml` in logical reading order.

## Testing & Quality
- Local gate: `mkdocs build --strict` (fails on broken links/TOC issues).
- Preview changes with `mkdocs serve` and verify the nav matches `mkdocs.yml`.
- Optional link check: use `lycheeverse/lychee-action` or run `lychee docs/**/*.md`.

## Commit & Pull Requests
- Commits: imperative mood, short subject (<= 50 chars), informative body (what/why), reference issues (e.g., `Fixes #12`).
- PRs: concise description, screenshots/GIFs of changed pages, mention affected paths (`docs/...`, `mkdocs.yml`), and deployment notes if the path prefix changes.

## Security & Config Tips
- Never commit secrets. Configure deploy secrets in GitHub Actions settings.
- Nginx must serve under `/productivity-tools/` with `alias` (see `deploy/nginx/`).
- When adding pages, ensure links are relative so they resolve under the subpath.

