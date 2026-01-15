# Digiplasty Site – Hugo + GitHub Pages Deployment

This repo uses a **two-branch workflow** for maintaining the Hugo source and deploying the compiled site via GitHub Pages.

---

## Branches

- `main` — contains all Hugo **source files** (`content/`, `layouts/`, `themes/`, etc.)
- `gh-pages` — contains the compiled **static site** (`public/`) served by GitHub Pages

---

## Deployment Summary

This project uses a **Git worktree** to connect the `public/` directory with the `gh-pages` branch. This keeps the source and generated output cleanly separated.

---

## Initial Setup (already done)

```bash
# Create and push empty gh-pages branch (one-time)
git branch gh-pages
git push -u origin gh-pages
git branch -d gh-pages

# Link public/ directory to gh-pages branch
rm -rf public
git worktree add -B gh-pages public origin/gh-pages
```

---

## Regular Workflow

1. Edit the site (on `main`)
Make any changes to:
`content/`
`layouts/`
`themes/`
`config` files, etc.

2. Commit source changes
```bash
git add .
git commit -m "Update source content"
git push origin main
```

3. Build the site
```bash
hugo
```
This regenerates the static site into the `public/` directory (which is the checked-out gh-pages branch).

4. Deploy the site
```bash
cd public
git add .
git commit -m "Publish site"
git push origin gh-pages
cd ..
```

### Notes
`public/` is a Git worktree linked to the `gh-pages` branch and must not be committed to `main`.

`.gitignore` includes `public/` to enforce separation.

GitHub Pages is configured to serve from the root of `gh-pages`.

If using a custom domain, ensure `public/CNAME` contains: "digiplasty.com" file

As a free user, note that the site source resides in a public repo.

To Check Live Site
GitHub Pages URL: `https://<username>.github.io/<reponame>/` (if project page)
Or: `https://digiplasty.com` if custom domain and DNS is set
Run: `hugo server --bind 0.0.0.0 --baseURL http://192.168.1.9:1313`