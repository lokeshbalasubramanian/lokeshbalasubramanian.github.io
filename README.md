# lokeshbalasubramanian.github.io

Personal website and blog, built with [Hugo](https://gohugo.io/) on a customized
[hugo-paper](https://github.com/nanxiaobei/hugo-paper) theme.

## Structure

```
content/      Pages (about, publications, CV) and blog posts (content/posts/)
layouts/      Template overrides for the theme
assets/       custom.css (site and blog styling)
static/       Files served as-is (resume PDF, images, icons)
archetypes/   Front-matter templates for `hugo new`
themes/       hugo-paper (vendored)
```

## Local development

```bash
hugo server -D        # http://localhost:1313, live reload, includes drafts
```

## Writing a post

```bash
hugo new posts/my-post.md
```

Front matter:

```toml
+++
date = '2026-10-03T00:00:00-04:00'
draft = false
title = 'My Post'
description = 'One or two sentences shown under the title and in the blog index.'
tags = ['ml']
+++
```

Math is rendered with KaTeX: inline `$...$` or `\(...\)`, display `$$...$$` or `\[...\]`.

## Deployment

Pushing to `master` triggers `.github/workflows/hugo.yml`, which builds the site
and deploys it to GitHub Pages. To update the CV, replace `static/resume.pdf`.
