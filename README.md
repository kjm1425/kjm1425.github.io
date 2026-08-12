# kyliemoden.com

Personal website of Kylie Moden — a splashy landing page plus a home for
personal projects. Built with [Jekyll](https://jekyllrb.com) and hosted on
GitHub Pages at [kyliemoden.com](https://kyliemoden.com).

## How the site is organized

| Path | What it is |
| --- | --- |
| `index.html` | Landing page (hero, featured projects, idea garden, "currently") |
| `projects.html` | The `/projects/` grid page |
| `_projects/*.md` | One markdown file per project — **add a file here to add a project** |
| `about.md` | The `/about/` page |
| `writing.md` + `_posts/` | Legacy blog posts, kept as a low-key archive at `/writing/` |
| `_layouts/` | Page templates (`default`, `page`, `post`, `project`) |
| `style.scss` | All styles in one file; palette lives in the `:root` variables |

## Adding a project

Create `_projects/my-thing.md`:

```yaml
---
title: My New Thing
blurb: One-sentence teaser shown on the project card.
emoji: 🚀
color: var(--teal)   # terracotta, orange, gold, sage, teal, or plum
status: In progress  # short label shown on the card pill
order: 7             # controls sort order in the grid
---

Body text in markdown — this becomes the project's page.
```

That's it — the card and page are generated automatically.

## Running locally

```bash
gem install jekyll jekyll-sitemap jekyll-feed
jekyll serve
```

Then open `http://localhost:4000`.
