# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static documentation site built with MkDocs and Material theme that mirrors a productivity tools list. The site is deployed to `https://saleem.net/productivity-tools/` via GitHub Actions using rsync over SSH.

## Development Commands

**Setup:**
```bash
pip install -r requirements.txt
```

**Local development:**
```bash
mkdocs serve  # Serves at http://127.0.0.1:8000
```

**Build (with strict validation):**
```bash
mkdocs build --strict  # Outputs to site/ directory
```

**Manual deployment test:**
```bash
rsync -az --delete site/ user@host:/var/www/productivity-tools/
```

## Architecture & Key Files

- **`docs/`**: Markdown content directory
  - `docs/index.md`: Main page content (mirrors Notion)
  - `docs/assets/`: Images and media files
- **`mkdocs.yml`**: Site configuration, theme settings, and navigation structure
- **`requirements.txt`**: Python dependencies (MkDocs + Material theme)
- **`.github/workflows/`**:
  - `deploy.yml`: Builds and deploys via rsync on push to main/master
  - `validate.yml`: Validates build and checks links on PRs
- **`deploy/nginx/`**: Example Nginx configuration for serving under `/productivity-tools/` subpath

## Deployment Configuration

The site deploys automatically via GitHub Actions when pushing to `main` or `master` branches. Required repository secrets:

- `SSH_HOST`: Deploy target (e.g., saleem.net)
- `SSH_USER`: Deploy user with write access
- `SSH_KEY`: Private SSH key (PEM format)
- `SSH_TARGET_DIR`: Target directory (e.g., /var/www/productivity-tools/)
- `SSH_PORT`: Optional custom SSH port

## Content Guidelines

- Content should mirror the Notion productivity tools list
- Use relative links and paths (no leading `/` to work under subpath)
- Images go in `docs/assets/` with kebab-case names
- One `# H1` per page, use `##`/`###` for subsequent sections
- Navigation is defined in `mkdocs.yml`

## Testing & Validation

- Always run `mkdocs build --strict` before committing (catches broken links)
- The validate workflow includes link checking via lycheeverse/lychee-action
- Preview changes locally with `mkdocs serve`

## Server Configuration

The site is served via Nginx under the `/productivity-tools/` path prefix using an alias location block. The example configuration is in `deploy/nginx/productivity-tools.conf`.