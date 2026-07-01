# Notes & Paintings — a Jekyll site

A small personal site for blog posts and a paintings gallery, hosted free on
GitHub Pages. Themed to match my main portfolio.



## Publish it on GitHub Pages

1. Create a new repository on GitHub (e.g. `creative`) and push these files to it.
2. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, choose `main` and `/ (root)`, save.
3. Wait ~1 minute. Your site appears at `https://USERNAME.github.io/REPO/`.

### ⚠️ One setting to get right: `baseurl`

In `_config.yml`:

- If the repo is named anything **other** than `USERNAME.github.io` (e.g. `creative`),
  set `baseurl: "/creative"` (match the repo name). **← most likely your case**
- If the repo **is** named `USERNAME.github.io`, leave `baseurl: ""`.

Getting this wrong is the #1 reason the CSS/images "don't load," so double-check it.

---

## Add a blog post

Create a file in `_posts/` named `YYYY-MM-DD-title.md`, for example
`_posts/2026-07-10-a-good-day.md`:

```markdown
---
layout: post
title: "A good day"
date: 2026-07-10
tags: [life]
---

Write your post here in Markdown.
```

Commit and push — it's live in a minute. To put an image in a post, drop the file
in `assets/images/` and reference it like:

```markdown
![alt text]({{ "/assets/images/myphoto.jpg" | relative_url }})
```

## Add a painting

1. Put the image in `assets/images/` (e.g. `painting4.jpg`).
2. Add a few lines to `_data/paintings.yml`:

```yaml
- image: /assets/images/painting4.jpg
  title: "Morning light"
  caption: "Watercolour, 2026"
```

The gallery updates automatically. That's it.

---

## File guide

```
_config.yml            # site title, your name, baseurl
_layouts/default.html  # nav + footer wrapper for every page
_layouts/post.html     # blog post template
index.html             # home page
blog.html              # list of all posts  (/blog/)
paintings.html         # gallery            (/paintings/)
about.md               # about page         (/about/)
_posts/                # your blog posts (Markdown)
_data/paintings.yml    # the list of paintings
assets/css/style.css   # all styling
assets/images/         # your images
```

## Preview locally (optional)

Not required — GitHub builds it for you. But if you want to see changes before
pushing, install Ruby + Bundler, then:

```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

---

## Customise

- **Colours / fonts:** edit the `:root` variables at the top of `assets/css/style.css`.
- **Nav links / portfolio link:** edit `_layouts/default.html` and `portfolio_url` in `_config.yml`.
- **Replace the placeholder images** in `assets/images/` with your real paintings
  (keep the filenames, or update `_data/paintings.yml` to match new names).
