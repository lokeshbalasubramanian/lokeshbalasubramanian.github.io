# Guide: How to Write & Publish Blog Posts

This guide explains how to add, preview, and publish new blog posts on your Hugo website.

---

## 1. Creating a New Post

### Method A: Using Hugo CLI (Recommended)
Run the following command in your project directory:

```bash
hugo new posts/my-new-post.md
```

This creates a new file at `content/posts/my-new-post.md` with pre-filled metadata.

### Method B: Creating a File Manually
Simply create a new `.md` file inside `content/posts/` (e.g., `content/posts/my-new-post.md`).

---

## 2. Formatting Your Post

Every post starts with **front matter** (metadata enclosed between `---` lines). Here is a complete example:

```markdown
---
title: "My Research on Machine Learning"
date: 2026-10-02T12:00:00+05:30
draft: false
summary: "A brief summary of the post that will appear on the index page."
tags: ["Machine Learning", "Physics", "Data Science"]
---

Write your post content here using standard **Markdown**.

### Subheading

You can write code blocks, bullet points, and math equations:

```python
import torch
print("Hello World")
```

For inline math, use `\( E = mc^2 \)`, or display math:
$$
\mathcal{L} = \mathcal{L}_{\text{data}} + \lambda \mathcal{L}_{\text{physics}}
$$
```

> **Important**: Ensure `draft: false` when you want the post to be published publicly. If `draft: true`, Hugo will hide it during production builds.

---

## 3. Previewing Changes Locally

To see how your post looks before publishing, run the local development server:

```bash
hugo server
```

Open your browser and visit:  
**http://localhost:1313/posts/**

Hugo automatically reloads the page whenever you save changes to your markdown files.

---

## 4. Publishing to GitHub Pages

Once you are satisfied with your new post, run the following git commands to push it live:

```bash
git add .
git commit -m "Publish new post: My Research on Machine Learning"
git push origin master
```

GitHub Actions will automatically build the site and deploy your post live to your website within 1–2 minutes!

---

## 5. Updating Your CV / Resume

If you update your resume in the future:
1. Replace `static/resume.pdf` with your new PDF file named `resume.pdf`.
2. Commit and push:
   ```bash
   git add static/resume.pdf
   git commit -m "Update resume PDF"
   git push origin master
   ```
