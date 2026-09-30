# joe.wadcan.com — GitHub Pages

A Jekyll-based rebuild of [joe.wadcan.com](https://joe.wadcan.com/), ready for GitHub Pages deployment.

## Quick start

### 1. Create a GitHub repository

Create a new repo (e.g. `joewadcan.github.io` for a user site, or any name for a project site).

### 2. Push this folder

```bash
cd gh-pages-site
git init
git add .
git commit -m "Initial Jekyll site"
git remote add origin git@github.com:YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

### 3. Enable GitHub Pages

Go to **Settings → Pages** in your repo, set the source to the `main` branch, root folder, and save.

Your site will be live at `https://YOUR_USERNAME.github.io/` (user site) or `https://YOUR_USERNAME.github.io/YOUR_REPO/` (project site).

> **If using a project site**, update `baseurl` in `_config.yml` to `/YOUR_REPO`.

### 4. Custom domain (optional)

To use `joe.wadcan.com`:

1. Add a `CNAME` file to the repo root containing `joe.wadcan.com`
2. Configure DNS: add a CNAME record pointing `joe.wadcan.com` to `YOUR_USERNAME.github.io`
3. Update `url` in `_config.yml` to `https://joe.wadcan.com`

## Local development

```bash
gem install bundler
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000`.

## Structure

```
├── _config.yml                  # Site settings & navigation
├── _layouts/
│   ├── default.html             # Base shell (header, footer)
│   ├── home.html                # Blog listing (homepage)
│   ├── page.html                # Static pages
│   └── post.html                # Single blog post
├── _posts/
│   └── 2019-07-05-time-management-interviewing.md
├── assets/css/
│   └── style.css                # All styles
├── index.md                     # Homepage → uses home layout
├── about-me.md                  # /about-me/
├── teaching.md                  # /teaching/
├── contact.md                   # /contact/
├── Gemfile                      # Ruby dependencies
└── .gitignore
```

## Adding new posts

Create a file in `_posts/` named `YYYY-MM-DD-title.md` with front matter:

```yaml
---
layout: post
title: "Your post title"
date: 2026-01-15
tag: topic
read_time: "5 min read"
hero_image: "https://example.com/image.jpg"
excerpt: "A short summary."
---

Your post content in Markdown...
```
