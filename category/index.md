---
layout: default
title: "Browse by Category"
permalink: /category/
---

<div class="cds--grid cds--grid--condensed cds--grid--full-width">
    <div class="cds--row">
        <div class="cds--col-lg-16 cds--col-md-8 cds--col-sm-4">
            <header style="margin-bottom: 3rem;">
                <h1 class="cds--type-expressive-heading-05" style="color: var(--cds-text-primary); margin-bottom: 1rem;">
                    Browse by Category
                </h1>
                <p class="cds--type-body-long-01" style="color: var(--cds-text-secondary);">
                    Explore posts organized by topic and theme
                </p>
            </header>

            <!-- Category Cards -->
            <div class="cds--row" style="margin-bottom: 3rem;">
                <!-- Manually define categories since posts might be empty -->
                {% assign predefined_categories = "development,architecture-design,ai-ml-data,infrastructure-devops,culture-methods" | split: "," %}
                
                {% for category in predefined_categories %}
                    {% assign category_posts = site.posts | where_exp: "post", "post.categories contains category" %}
                    <div class="cds--col-lg-8 cds--col-md-4 cds--col-sm-4" style="margin-bottom: 2rem;">
                        <div class="blog-card" style="height: 100%; display: flex; flex-direction: column;">
                            <div style="text-align: center; padding: 1rem;">
                                <!-- Category Icon -->
                                <div style="margin-bottom: 1rem;">
                                    {% if category == 'development' %}
                                        <svg width="48" height="48" viewBox="0 0 16 16" fill="#78a9ff" style="display: block; margin: 0 auto;">
                                            <path d="M4.5 3L6 1.5 9.5 5 6 8.5 4.5 7 7 4.5 4.5 2zM11.5 3L10 1.5 6.5 5 10 8.5 11.5 7 9 4.5 11.5 2z"/>
                                        </svg>
                                    {% elsif category == 'architecture-design' %}
                                        <svg width="48" height="48" viewBox="0 0 16 16" fill="#78a9ff" style="display: block; margin: 0 auto;">
                                            <path d="M1 1h14v14H1V1zm1 1v12h12V2H2zm2 2h8v8H4V4zm1 1v6h6V5H5z"/>
                                        </svg>
                                    {% elsif category == 'ai-ml-data' %}
                                        <svg width="48" height="48" viewBox="0 0 16 16" fill="#78a9ff" style="display: block; margin: 0 auto;">
                                            <path d="M8 1a7 7 0 100 14A7 7 0 008 1zM3.5 8a4.5 4.5 0 119 0 4.5 4.5 0 01-9 0z"/>
                                            <circle cx="8" cy="8" r="2"/>
                                        </svg>
                                    {% elsif category == 'infrastructure-devops' %}
                                        <svg width="48" height="48" viewBox="0 0 16 16" fill="#78a9ff" style="display: block; margin: 0 auto;">
                                            <path d="M3 1h10v2H3V1zm0 4h10v2H3V5zm0 4h10v2H3V9zm0 4h10v2H3v-2z"/>
                                            <path d="M1 2h1v12H1V2z"/>
                                        </svg>
                                    {% elsif category == 'culture-methods' %}
                                        <svg width="48" height="48" viewBox="0 0 16 16" fill="#78a9ff" style="display: block; margin: 0 auto;">
                                            <path d="M8 1a2.5 2.5 0 100 5 2.5 2.5 0 000-5zM3 7a1 1 0 011-1h8a1 1 0 011 1v6a1 1 0 01-1 1H4a1 1 0 01-1-1V7z"/>
                                            <path d="M6 9h4v1H6V9zm0 2h4v1H6v-1z"/>
                                        </svg>
                                    {% endif %}
                                </div>
                                
                                <h3 class="cds--type-productive-heading-03" style="color: var(--cds-text-primary); margin-bottom: 1rem;">
                                    {% if category == 'development' %}Development
                                    {% elsif category == 'architecture-design' %}Architecture & Design
                                    {% elsif category == 'ai-ml-data' %}AI, ML & Data Engineering
                                    {% elsif category == 'infrastructure-devops' %}Infrastructure & DevOps
                                    {% elsif category == 'culture-methods' %}Culture & Methods
                                    {% endif %}
                                </h3>
                        
                                
                                <div style="margin-bottom: 1rem;">
                                    <span class="cds--tag cds--tag--blue">
                                        {{ category_posts.size }} post{% if category_posts.size != 1 %}s{% endif %}
                                    </span>
                                </div>
                                
                                <a href="/category/{{ category | slugify }}/" class="bx--btn bx--btn--ghost" style="color: var(--cds-link-primary);">
                                    <svg class="bx--btn__icon" width="16" height="16" viewBox="0 0 16 16" fill="currentColor" style="margin-right: 0.5rem;">
                                        <path d="M11 8l-5 5-1.5-1.5L8 8 4.5 4.5 6 3l5 5z"/>
                                    </svg>
                                    View Posts
                                </a>
                            </div>
                        </div>
                    </div>
                {% endfor %}
            </div>

            <!-- Quick Stats -->
            <section class="blog-card" style="text-align: center; margin-bottom: 3rem;">
                <h2 class="cds--type-expressive-heading-04" style="color: var(--cds-text-primary); margin-bottom: 1rem;">
                    Content Overview
                </h2>
                <div class="cds--row">
                    <div class="cds--col-lg-5 cds--col-md-3 cds--col-sm-2">
                        <div style="padding: 1rem;">
                            <div style="font-size: 2rem; font-weight: 600; color: var(--cds-link-primary); margin-bottom: 0.5rem;">
                                {{ site.posts.size }}
                            </div>
                            <div class="cds--type-body-short-01" style="color: var(--cds-text-secondary);">
                                Total Posts
                            </div>
                        </div>
                    </div>
                    <div class="cds--col-lg-6 cds--col-md-2 cds--col-sm-2">
                        <div style="padding: 1rem;">
                            <div style="font-size: 2rem; font-weight: 600; color: var(--cds-link-primary); margin-bottom: 0.5rem;">
                                {{ all_categories.size }}
                            </div>
                            <div class="cds--type-body-short-01" style="color: var(--cds-text-secondary);">
                                Categories
                            </div>
                        </div>
                    </div>
                    <div class="cds--col-lg-5 cds--col-md-3 cds--col-sm-2">
                        <div style="padding: 1rem;">
                            <div style="font-size: 2rem; font-weight: 600; color: var(--cds-link-primary); margin-bottom: 0.5rem;">
                                {{ site.posts | map: 'tags' | join: ',' | split: ',' | uniq | size }}
                            </div>
                            <div class="cds--type-body-short-01" style="color: var(--cds-text-secondary);">
                                Tags
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Navigation -->
            <div style="text-align: center;">
                <a href="{{ "/blog/" | relative_url }}" class="bx--btn bx--btn--primary" style="margin-right: 1rem;">
                    <svg class="bx--btn__icon" width="16" height="16" viewBox="0 0 16 16" fill="currentColor" style="margin-right: 0.5rem;">
                        <path d="M4 3h8v1H4V3zm0 3h8v1H4V6zm0 3h6v1H4V9zm0 3h4v1H4v-1zM2 3v10h12V3H2zm11 9H3V4h10v8z"/>
                    </svg>
                    View All Posts
                </a>
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