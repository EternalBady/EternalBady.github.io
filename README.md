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
