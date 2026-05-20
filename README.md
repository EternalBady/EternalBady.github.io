# SZiiN Lab

A GitHub Pages + Jekyll personal engineering logbook for AI Infra learning notes, CUDA experiments, LLM deployment logs, and project writeups.

## Structure

- `index.md` — home page with clear sections and recent notes.
- `blog.md` — reverse chronological post list.
- `articles.md` — planned long-form article tracks.
- `projects.md` — project board for experiments and tools.
- `archives.md`, `categories.md`, `tags.md` — browse pages for long-term content growth.
- `_posts/` — Markdown blog posts using Jekyll's `YYYY-MM-DD-title.md` format.

## Writing a new post

Create a Markdown file in `_posts/`:

```md
---
title: "My CUDA Note"
description: "A short summary for previews."
categories: [CUDA]
tags: [CUDA, GPU, Profiling]
reading_time: "5 min read"
---

Write the note here.
```

## Local preview

If Ruby and Jekyll are installed:

```bash
bundle exec jekyll serve
```

Built with curiosity, music, and late-night debugging.

## Why the website may not change after commit

If `https://eternalbady.github.io/` still shows old content, it is usually one of these deployment issues:

1. **Changes are not on the branch GitHub Pages is publishing** (often `main`).
2. **GitHub Pages source is not configured correctly** (`Settings -> Pages`).
3. **Jekyll build failed** in Actions, so old content is still served.

This repository now includes `.github/workflows/pages.yml`, so pushes to `main`, `master`, or `work` trigger a Pages build.

### Quick verification checklist

1. Push your latest commit.
2. Open `Actions` tab and ensure workflow **Deploy Jekyll site to Pages** is green.
3. In `Settings -> Pages`, confirm source is **GitHub Actions**.
4. Hard refresh browser (`Ctrl/Cmd + Shift + R`) after deployment.
