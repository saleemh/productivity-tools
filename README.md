# Productivity Tools

Static documentation site mirroring my current productivity tools list, published at `https://saleem.net/productivity-tools/`.

## Overview

- Built with MkDocs + Material theme
- Deployed via GitHub Actions to my server using rsync over SSH
- Served under Nginx at the `/productivity-tools/` path prefix

## Local Development

Requirements:

- Python 3.9+
- `pip install -r requirements.txt`

Commands:

- `mkdocs serve` — run locally at `http://127.0.0.1:8000`
- `mkdocs build` — build static site into `site/`

## Content

Start with a single page mirroring the Notion content in `docs/index.md`.

## Deployment (GitHub Actions)

The workflow in `.github/workflows/deploy.yml` builds the site and deploys it via rsync over SSH using repository secrets:

- `SSH_HOST` — e.g., `saleem.net`
- `SSH_USER` — deploy user with write access to target dir
- `SSH_KEY` — private key for the deploy user (PEM format)
- `SSH_TARGET_DIR` — e.g., `/var/www/productivity-tools/`

## Nginx

Serve the built site at the desired path prefix using an alias location block:

```
location ^~ /productivity-tools/ {
    alias /var/www/productivity-tools/;
    index index.html;
    try_files $uri $uri/ =404;
    autoindex off;
}
```

Reload Nginx after updating the config.

