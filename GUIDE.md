# How to Manage Your Hugo Website

## 1. Creating a New Post
To create a new blog post, run the following command in your terminal:
```bash
hugo new posts/my-new-post.md
```
This will create a new file in `content/posts/my-new-post.md`.
Open it and edit the content. The header (front matter) looks like this:
```yaml
---
title: "My New Post"
date: 2026-02-06
draft: true
---
```
Change `draft: true` to `draft: false` when you are ready to publish.

## 2. Adding a Publication
To add a new publication, create a file in `content/publications/`:
```bash
hugo new publications/new-paper.md
```
Then update the fields to include your PDF link and citation:
```yaml
---
title: "Paper Title"
date: 2026-02-06
publication_venue: "Journal Name"
pdf_url: "https://arxiv.org/pdf/..."
citation: "Author list..."
---
```

## 3. Updating Your CV
Edit the file at `content/cv.md` to update your text CV.
If you want to provide a PDF download, place your `cv.pdf` file in the `static/` folder and link to it like this: `[Download PDF](/cv.pdf)`.

## 4. Running Locally
Always preview your changes before deploying:
```bash
hugo server
```
Visit `http://localhost:1313`.

## 5. Deployment
When you are ready, you can deploy your `public/` folder to GitHub Pages or Netlify.
