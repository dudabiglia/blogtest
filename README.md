# Maria's Blog

A minimal Jekyll blog for GitHub Pages, editable with [Pages CMS](https://pagescms.org).

## Structure

```
_config.yml          Jekyll settings (permalinks, defaults)
_data/settings.yml   Site title, description, author  ← editable in Pages CMS
_posts/              Blog posts (Markdown)             ← editable in Pages CMS
_layouts/            HTML templates
assets/style.css     Styles
assets/images/       Uploaded images (via Pages CMS)
.pages.yml           Pages CMS configuration
```

## Publish to GitHub Pages

1. Create a new repository on GitHub (e.g. `blog`, or `<username>.github.io`).
2. Push this folder to it:
   ```sh
   git init
   git add .
   git commit -m "Initial blog"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
4. If the repo is *not* named `<username>.github.io`, set `baseurl: "/<repo>"` in `_config.yml`.

The site will be live in a minute or two at the URL shown on that page.

## Connect Pages CMS

1. Go to <https://app.pagescms.org> and sign in with GitHub.
2. Pick this repository and the `main` branch.
3. You'll see **Posts** and **Settings**. Every save is a commit, and GitHub Pages rebuilds automatically.

## Write a post manually

Add a file to `_posts/` named `YYYY-MM-DD-slug.md`:

```markdown
---
title: My post
date: 2026-10-11
---

Post content in Markdown.
```
