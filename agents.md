# Selim's Blog Agents

Welcome to my personal blog! This site is built with **Jekyll** to leverage GitHub Pages' default support, and is designed using the [Carbon Design System v10](https://v10.carbondesignsystem.com/) with a fully dark-themed layout for optimal readability and style.

---

## 📝 About This Blog

This blog is a space for sharing insights, tutorials, and thoughts on technology, design, and personal growth. It is developed using **Jekyll** for seamless GitHub Pages deployment. Every element is crafted to be 1:1 compatible with the Carbon Design System, ensuring a modern, accessible, and visually appealing experience.

---

## 🌑 Dark Theme

The entire blog uses Carbon's dark theme. All components, typography, and colors strictly follow the [Carbon dark theme guidelines](https://v10.carbondesignsystem.com/guidelines/themes/#dark-theme).

---

## 🏗️ Jekyll Implementation

- The blog is structured using Jekyll's default folders: `_layouts`, `_includes`, `_posts`, and a root `index.md` or `index.html`.
- Carbon Design System v10 CSS/JS is included via CDN in Jekyll layouts.
- All UI components and layouts use Carbon classes and markup for strict compatibility.
- Liquid templating is used for dynamic content and posts.
- The site is fully compatible with GitHub Pages for easy deployment.

---

## 🚀 Blog Layout

- **Header:** Navigation bar styled with Carbon's dark theme, including links to Home, Blog, About, and Contact.
- **Main Content:** Posts are displayed in Carbon cards, with clear typography and spacing.
- **Sidebar:** Optional sidebar for categories, tags, and recent posts, using Carbon's UI Shell components.
- **Footer:** Simple, dark-themed footer with social links and copyright.

---

## 🧩 Implementation Notes

- All UI components (buttons, cards, navigation, etc.) must use Carbon Design System classes and markup.
- Use Carbon's grid system for responsive layouts.
- Ensure accessibility by following Carbon's ARIA and contrast guidelines.
- Reference [Carbon Design System documentation](https://v10.carbondesignsystem.com/components/overview/) for all design and implementation details.
- Use Jekyll's Liquid templating for posts and dynamic content.

---

## 🧩 Implementation Notes

- All UI components (buttons, cards, navigation, etc.) must use Carbon Design System classes and markup.
- Use Carbon's grid system for responsive layouts.
- Ensure accessibility by following Carbon's ARIA and contrast guidelines.
- Reference [Carbon Design System documentation](https://v10.carbondesignsystem.com/components/overview/) for all design and implementation details.

---

## 📚 Example Post (Jekyll + Carbon)

```
---
layout: default
title: My First Blog Post
---
<section class="bx--grid bx--grid--condensed bx--grid--full-width bx--theme--g100">
  <div class="bx--row">
    <div class="bx--col-lg-8 bx--col-md-6 bx--col-sm-4">
      <article class="bx--card bx--card--dark">
        <h2 class="bx--type-expressive-heading-04">{{ page.title }}</h2>
        <p class="bx--type-body-long-01">{{ page.content }}</p>
      </article>
    </div>
  </div>
</section>
```

---

## 🛠️ How to Contribute

If you'd like to suggest improvements or contribute, please follow the Carbon Design System guidelines and submit a pull request. Jekyll structure and Carbon compatibility are required for all contributions.

---

© 2025 Selim. Powered by Carbon Design System v10. All rights reserved.
