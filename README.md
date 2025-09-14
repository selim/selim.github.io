# Selim's Blog (Jekyll + Carbon)

Welcome to your personal blog repository! This README will guide you through setting up Jekyll, integrating the Carbon Design System, deploying to GitHub Pages, and writing blog posts.

---

## 🚀 Getting Started

### 1. Install Jekyll

Jekyll requires Ruby. On macOS, you can install Jekyll with:

```sh
# Install Ruby (if not already installed)
brew install ruby
# Add Ruby to your PATH (if needed)
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
# Install Jekyll and Bundler
gem install jekyll bundler
```

### 2. Create Jekyll Structure

Jekyll uses these folders:
- `_layouts` (HTML templates)
- `_includes` (reusable HTML)
- `_posts` (your blog posts)
- `index.md` or `index.html` (homepage)

To scaffold a new site:

```sh
jekyll new .
```

### 3. Integrate Carbon Design System

Add Carbon CSS/JS to your main layout (`_layouts/default.html`):

```html
<!-- In the <head> section -->
<link rel="stylesheet" href="https://unpkg.com/carbon-components/css/carbon-components.min.css">
<script src="https://unpkg.com/carbon-components/scripts/carbon-components.min.js"></script>
```

Use Carbon classes in your HTML for strict dark theme compatibility. Example:

```html
<section class="bx--grid bx--grid--condensed bx--grid--full-width bx--theme--g100">
  <!-- ... -->
</section>
```

### 4. Write a Blog Post

Create a new file in `_posts` with this format:

```
YYYY-MM-DD-title.md
```

Example:

```
2025-09-14-my-first-post.md
```

Inside, use:

```
---
layout: default
title: My First Post
---
<section class="bx--grid bx--theme--g100">
  <article class="bx--card bx--card--dark">
    <h2>{{ page.title }}</h2>
    <p>Welcome to my blog!</p>
  </article>
</section>
```

### 5. Preview Locally

Run Jekyll locally to preview your site:

```sh
bundle exec jekyll serve
```

Visit `http://localhost:4000` in your browser.

### 6. Deploy to GitHub Pages

1. Push your code to a GitHub repository (e.g., `selim.github.io`).
2. In your repo settings, enable GitHub Pages (choose branch: `master` or `main`).
3. GitHub will build and deploy your site automatically.

---

## ✍️ How to Write and Add New Posts

### Step 1: Create a New Post File

Create a new file in the `_posts` directory with this naming format:

```
_posts/YYYY-MM-DD-title-with-hyphens.md
```

Example: `_posts/2025-09-14-my-awesome-new-post.md`

### Step 2: Add Front Matter

Start your post with YAML front matter:

```yaml
---
layout: post
title: "My Awesome New Post"
date: 2025-09-14 15:30:00 -0400
categories: [technology, tutorial]
tags: [jekyll, carbon, web-development]
author: Selim
---
```

### Step 3: Write Your Content

Write your post content in Markdown below the front matter:

```markdown
# This is a heading

This is a paragraph with **bold** and *italic* text.

- List item 1
- List item 2

```code blocks are supported```

[Links work too](https://example.com)
```

### Step 4: Preview Locally (Optional)

Test your post locally before publishing:

```sh
bundle exec jekyll serve
```

Visit `http://localhost:4000` to see your changes.

### Step 5: Publish to GitHub Pages

1. **Stage your changes:**
   ```sh
   git add .
   ```

2. **Commit your post:**
   ```sh
   git commit -m "Add new post: My Awesome New Post"
   ```

3. **Push to GitHub:**
   ```sh
   git push origin master
   ```

4. **Automatic deployment:** GitHub Pages will automatically build and deploy your site within 1-2 minutes.

## 🚀 How to Update GitHub Pages

### Initial Setup

1. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click "Settings" tab
   - Scroll down to "Pages" section
   - Under "Source", select "Deploy from a branch"
   - Choose "master" branch and "/ (root)" folder
   - Click "Save"

2. **Custom Domain (Optional):**
   - Add a `CNAME` file with your domain name
   - Configure your DNS to point to GitHub Pages

### Making Updates

Any changes you push to the master branch will automatically trigger a rebuild:

1. **Make your changes** (new posts, design updates, etc.)
2. **Commit and push:**
   ```sh
   git add .
   git commit -m "Description of changes"
   git push origin master
   ```
3. **GitHub automatically builds and deploys** your site
4. **Check deployment status** in the "Actions" tab of your repository

### Deployment Status

- **Build time:** Usually 1-2 minutes
- **Check status:** Repository → Actions tab
- **View live site:** `https://yourusername.github.io`
- **Troubleshooting:** Check the Actions tab for build errors

---

## 📚 Resources
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Guide](https://pages.github.com/)
- [Carbon Design System](https://v10.carbondesignsystem.com/)

---

If you need help, open an issue or ask for guidance!
