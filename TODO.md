# Productivity Tools – Completion Checklist

Use this checklist to finish setup, deploy safely, and verify the docs site at `https://saleem.net/productivity-tools/`.

## 1) GitHub Repo
- [ ] Set remote to your repo
  - SSH: `git remote set-url origin git@github.com:saleemh/productivity-tools.git`
  - or HTTPS: `git remote set-url origin https://github.com/saleemh/productivity-tools.git`
- [ ] Choose default branch
  - Use `main`: `git branch -M main`
  - or keep `master` (workflow supports both)
- [ ] Push code
  - `git push -u origin main` (or `master`)

## 2) GitHub Actions Secrets (Settings → Secrets and variables → Actions)
- [ ] `SSH_HOST` = `saleem.net`
- [ ] `SSH_USER` = deploy user on server (e.g., `deploy`)
- [ ] `SSH_KEY` = private key (PEM) for `SSH_USER`
- [ ] `SSH_TARGET_DIR` = `/var/www/productivity-tools/`
- [ ] (Optional) `SSH_PORT` = custom SSH port if not 22

## 3) Server Prep (run on saleem.net)
- [ ] Create deploy user (skip if exists)
  - `sudo adduser deploy`
- [ ] Allow SSH key auth for deploy user
  - Place public key matching `SSH_KEY` into `/home/deploy/.ssh/authorized_keys`
  - Test: `ssh deploy@saleem.net 'echo ok'`
- [ ] Create target directory and set perms
  - `sudo mkdir -p /var/www/productivity-tools`
  - `sudo chown -R deploy:www-data /var/www/productivity-tools`
  - `sudo chmod -R 755 /var/www/productivity-tools`

## 4) Nginx Location Block (in saleem.net server block)
Add a dedicated prefix location that won’t interfere with other routes:

```
location ^~ /productivity-tools/ {
    alias /var/www/productivity-tools/;
    index index.html;
    try_files $uri $uri/ =404;
    autoindex off;
}
```

- [ ] Add the above to your existing `server { ... }` for saleem.net
- [ ] Validate and reload
  - `sudo nginx -t && sudo systemctl reload nginx`

## 5) First Deploy via GitHub Actions
- [ ] Push a commit to trigger workflow (e.g., edit README)
- [ ] Watch Actions → `Deploy` job; confirm build + rsync succeed

## 6) Verify Live Site
- [ ] Check directory on server: `ls -la /var/www/productivity-tools | head`
- [ ] Browse: `https://saleem.net/productivity-tools/`
- [ ] Spot-check links and assets load correctly

## 7) Mirror Notion Content (initial manual step)
- [ ] Export or copy content from Notion: `http://notion.saleem.net/productivity-tools`
- [ ] Paste into `docs/index.md` (replace placeholder sections)
- [ ] Commit and push to deploy

## 8) Optional Quality Gates (recommended)
- [ ] Add link checker job (lychee)
  - Install in workflow: `lycheeverse/lychee-action@v1` or `cargo install lychee`
  - Run: `lychee --no-progress --verbose docs/**/*.md`
- [ ] Add Markdown lint (markdownlint-cli)
  - `npm i -D markdownlint-cli` and a simple job to run `npx markdownlint .` (or use Docker action)

## 9) Optional Staging Flow
- [ ] Create `/var/www/productivity-tools-test/` and add a temp location `^~ /productivity-tools-test/`
- [ ] Point `SSH_TARGET_DIR` to test path for first deploy
- [ ] Verify, then switch back to `/productivity-tools/`

## 10) Future: Notion Sync Automation
- [ ] Choose language (Python or Node) for a small sync script
- [ ] Create Notion integration + database/page ID(s)
- [ ] Map Notion fields → Markdown in `docs/index.md` (or per-category pages later)
- [ ] Add scheduled GitHub Action to fetch + open PR with changes

## Troubleshooting
- Build fails with `--strict`: fix broken links/headings in `docs/index.md`
- 404s under subpath: ensure no leading `/` in links/images; keep them relative
- Wrong route served: confirm Nginx block uses `^~` and correct `alias`
- Permission denied on deploy: check owner/group and `SSH_KEY` correctness

## Reference Commands
- Local dev: `pip install -r requirements.txt && mkdocs serve`
- Build locally: `mkdocs build --strict`
- Manual rsync (for testing):
  - `rsync -az --delete site/ deploy@saleem.net:/var/www/productivity-tools/`
