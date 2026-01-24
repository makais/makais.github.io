# Digiplasty Site – Hugo + GitHub Pages Deployment

This repo uses a **two-branch workflow** for maintaining the Hugo source and deploying the compiled site via GitHub Pages. The PaperMod theme is managed as a **Git submodule**.

---

## Branches

- `main` — contains all Hugo **source files** (`content/`, `layouts/`, `themes/`, etc.)
- `gh-pages` — contains the compiled **static site** (`public/`) served by GitHub Pages

---

## Deployment Summary

This project uses a **Git worktree** to connect the `public/` directory with the `gh-pages` branch. This keeps the source and generated output cleanly separated.

---

## Initial Setup

### First-Time Clone

```bash
# Clone repo with submodules included
git clone --recurse-submodules https://github.com/makais/makais.github.io.git
cd makais.github.io

# If already cloned without submodules, initialize them
git submodule update --init --recursive
```

### Worktree Setup (one-time)

```bash
# Create and push empty gh-pages branch
git branch gh-pages
git push -u origin gh-pages
git branch -d gh-pages

# Link public/ directory to gh-pages branch
rm -rf public
git worktree add -B gh-pages public origin/gh-pages
```

---

## Theme Customizations

This site uses the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme with the following customizations:

**Layout Overrides** (`/layouts/partials/`)
- **head.html** - Custom SEO meta tags, CSS bundling, search integration
- **footer.html** - Scroll-to-top button, code copy functionality, theme toggle
- **single.html** - Custom post layout with breadcrumbs, TOC, and metadata display

**Custom Shortcodes** (`/layouts/shortcodes/`)
- **center.html** - Centers content blocks: `{{< center >}}content{{< /center >}}`

**Styling** (`/assets/css/extended/custom.css`)
- Everforest-inspired dark color scheme
- Custom profile image styling (no border-radius)
- Figure/image centering with `!important` overrides
- Custom spacing for horizontal rules and captions

**Configuration** (`hugo.yaml`)
- Forced dark theme (no toggle)
- Profile mode enabled with custom branding
- Google Analytics via Hugo's standard `services.googleAnalytics`
- Custom menu structure (Projects, Posts, About)

---

## Regular Workflow

### 1. Edit the Site (on `main`)
Make any changes to:
- `content/`
- `layouts/`
- `config` files, etc.

### 2. Commit Source Changes
```bash
git add .
git commit -m "Update source content"
git push origin main
```

### 3. Build the Site
```bash
hugo
```
This regenerates the static site into the `public/` directory (which is the checked-out gh-pages branch).

### 4. Deploy the Site
```bash
cd public
git add .
git commit -m "Publish site"
git push origin gh-pages
cd ..
```

---

## Theme Submodule Management

The PaperMod theme is managed as a Git submodule at `themes/PaperMod/`.

### Check Submodule Status
```bash
# View current submodule commit
git submodule status

# Check for updates available from theme repo
cd themes/PaperMod
git fetch
git log HEAD..origin/master --oneline
cd ../..
```

### Update Theme to Latest Version
```bash
# Update submodule to latest commit
git submodule update --remote themes/PaperMod

# Commit the submodule update
git add themes/PaperMod
git commit -m "Update PaperMod theme to latest version"
git push origin main
```

**Important:** When updating the PaperMod theme, review the 3 partial overrides in `/layouts/partials/` for potential conflicts. Test locally with `hugo server` before deploying.

---

## Notes

- `public/` is a Git worktree linked to the `gh-pages` branch and must not be committed to `main`
- `.gitignore` includes `public/` to enforce separation
- GitHub Pages is configured to serve from the root of `gh-pages`
- If using a custom domain, ensure `public/CNAME` contains: "digiplasty.com"
- As a free user, note that the site source resides in a public repo

### Check Live Site
- GitHub Pages URL: `https://<username>.github.io/<reponame>/` (if project page)
- Custom domain: `https://digiplasty.com` (if DNS is configured)
- Local testing: `hugo server --bind 0.0.0.0 --baseURL http://192.168.1.9:1313`