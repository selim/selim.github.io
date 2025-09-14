---
layout: default
title: "All Blog Posts"
permalink: /blog/
---

<div class="cds--grid cds--grid--condensed cds--grid--full-width">
    <div class="cds--row">
        <div class="cds--col-lg-16 cds--col-md-8 cds--col-sm-4">
            <header style="margin-bottom: 3rem;">
                <h1 class="cds--type-expressive-heading-05" style="color: var(--cds-text-primary); margin-bottom: 1rem;">
                    All Blog Posts
                </h1>
                <p class="cds--type-body-long-01" style="color: var(--cds-text-secondary);">
                    Explore all articles and insights from my blog
                </p>
            </header>

            <!-- All Posts -->
            <div class="blog-posts">
                {% for post in site.posts %}
                    <article class="blog-card">
                        <div style="display: flex; flex-direction: column; height: 100%;">
                            <div class="blog-post-meta">
                                <time class="cds--type-caption-01" style="color: var(--cds-text-secondary);">
                                    {{ post.date | date: "%B %d, %Y" }}
                                </time>
                                {% if post.author %}
                                <span class="cds--type-caption-01" style="color: var(--cds-text-secondary);"> • by {{ post.author }}</span>
                                {% endif %}
                                {% if post.categories %}
                                <span class="cds--type-caption-01" style="color: var(--cds-text-secondary);"> • in 
                                    {% for category in post.categories %}
                                        <a href="/category/{{ category | slugify }}/" style="color: var(--cds-link-primary);">{{ category }}</a>{% unless forloop.last %}, {% endunless %}
                                    {% endfor %}
                                </span>
                                {% endif %}
                            </div>
                            
                            <h2 class="blog-post-title">
                                <a href="{{ post.url | relative_url }}" style="color: var(--cds-text-primary); text-decoration: none;">
                                    {{ post.title }}
                                </a>
                            </h2>
                            
                            <div class="blog-post-excerpt" style="flex-grow: 1;">
                                <p class="cds--type-body-long-01" style="color: var(--cds-text-secondary);">
                                    {{ post.excerpt | strip_html | truncatewords: 30 }}
                                </p>
                            </div>
                            
                            <div style="margin-top: auto; padding-top: 1rem;">
                                {% if post.categories %}
                                <div style="margin-bottom: 1rem;">
                                    {% for category in post.categories %}
                                        <span class="cds--tag cds--tag--blue" style="margin-right: 0.5rem; margin-bottom: 0.5rem;">
                                            {{ category }}
                                        </span>
                                    {% endfor %}
                                </div>
                                {% endif %}
                                
                                <a href="{{ post.url | relative_url }}" class="bx--btn bx--btn--ghost" style="color: var(--cds-link-primary);">
                                    <svg class="bx--btn__icon" width="16" height="16" viewBox="0 0 16 16" fill="currentColor" style="margin-right: 0.5rem;">
                                        <path d="M11 8l-5 5-1.5-1.5L8 8 4.5 4.5 6 3l5 5z"/>
                                    </svg>
                                    Read More
                                </a>
                            </div>
                        </div>
                    </article>
                {% endfor %}
            </div>

            <!-- Navigation -->
            <div style="text-align: center; margin-top: 3rem;">
                <a href="{{ "/" | relative_url }}" class="bx--btn bx--btn--secondary">
                    <svg class="bx--btn__icon" width="16" height="16" viewBox="0 0 16 16" fill="currentColor" style="margin-right: 0.5rem;">
                        <path d="M8 1L1 6v9h4V9h6v6h4V6L8 1zm0 2.53L13 8v5h-2V9H5v4H3V8l5-4.47z"/>
                    </svg>
                    Back to Home
                </a>
            </div>
        </div>
    </div>
</div>