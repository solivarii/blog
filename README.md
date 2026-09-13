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

Put image files in `assets/images/`, then reference them from a post with markdown, prefixed with `{{ site.baseurl }}`:

```markdown
![Alt text]({{ site.baseurl }}/assets/images/your-image.jpg)
```

The `{{ site.baseurl }}` prefix matters because this site is served from `solivarii.com/blog` rather than the domain root (see `baseurl` in `_config.yml`) — a plain `/assets/images/your-image.jpg` path would resolve to `solivarii.com/assets/images/your-image.jpg` and 404.

## Previewing locally

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000/blog/` (note the `/blog/` path — it matches `baseurl`).

## Deployment

This site is served at `solivarii.com/blog`. It's set up for GitHub Pages, which builds and hosts Jekyll sites automatically with no CI configuration needed:

1. Push this repository to GitHub (or push to `main` if it's already there).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch," and pick the `main` branch, `/ (root)` folder.
4. Save. GitHub will build and publish the site within a minute or two, and rebuild it automatically on every push.
5. Point `solivarii.com/blog` at this site (however the rest of solivarii.com is hosted — e.g. a reverse proxy rule, or your host's path-based routing).

No servers, containers, or third-party services to maintain.
