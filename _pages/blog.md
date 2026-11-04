---
layout: page
permalink: /blog/
title: blogs
description: Research notes, disclosures, and payment protocol analysis.
nav: true
nav_order: 3
---

<ul class="post-list" style="list-style: none; padding-left: 0;">
{% for post in site.posts %}
  {% assign read_time = post.content | number_of_words | divided_by: 180 | plus: 1 %}
  <li class="mb-4 pb-4" style="border-bottom: 1px solid var(--global-divider-color, #eaecef);">
    <h3 class="mb-2" style="font-size: 1.25rem; font-weight: 600;">
      <a href="{{ post.url | relative_url }}" style="color: var(--global-theme-color);">
        {{ post.title }}
      </a>
    </h3>
    <div class="text-muted mb-2" style="font-size: 0.85rem;">
      <span><i class="fa-regular fa-calendar fa-sm mr-1"></i> {{ post.date | date: "%B %d, %Y" }}</span>
      <span class="mx-2">&middot;</span>
      <span><i class="fa-regular fa-clock fa-sm mr-1"></i> {{ read_time }} min read</span>
      {% if post.categories.size > 0 %}
        <span class="mx-2">&middot;</span>
        <span class="text-uppercase" style="font-size: 0.75rem; letter-spacing: 0.5px; font-weight: 600; color: var(--global-theme-color);">{{ post.categories | first }}</span>
      {% endif %}
    </div>
    {% if post.description %}
    <p class="mb-2 text-secondary" style="font-size: 0.95rem; line-height: 1.55;">
      {{ post.description }}
    </p>
    {% endif %}
    <div>
      <a href="{{ post.url | relative_url }}" style="font-size: 0.85rem; font-weight: 500;">
        Read article &rarr;
      </a>
    </div>
  </li>
{% else %}
  <p class="text-muted">No posts published yet.</p>
{% endfor %}
</ul>
