# Blog

An ultra-minimalist blog built with [Jekyll](https://jekyllrb.com/). Set in Helvetica Neue (system font, no external font loading), no JavaScript, no build tooling beyond Jekyll itself.

## Writing a post

Create a new file in `_posts/` named `YYYY-MM-DD-title-of-post.md`:

```markdown
---
layout: post
title: "Your Post Title"
date: 2026-01-15
---

Write your post here in plain markdown.
```

Commit and push — that's it.

## Editing a post

Open the corresponding file in `_posts/` and edit it directly.

## Adding images

Put image files in `assets/images/`, then reference them from a post with standard markdown:

```markdown
![Alt text](/assets/images/your-image.jpg)
```

## Previewing locally

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Deployment

This site is set up for GitHub Pages, which builds and hosts Jekyll sites automatically with no CI configuration needed:

1. Push this repository to GitHub (or push to `main` if it's already there).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch," and pick the `main` branch, `/ (root)` folder.
4. Save. GitHub will build and publish the site within a minute or two, and rebuild it automatically on every push.

No servers, containers, or third-party services to maintain.
