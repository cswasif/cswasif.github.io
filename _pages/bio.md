---
layout: page
permalink: /bio/
title: bio
description:
nav: true
nav_order: 1
---

## Education

{% for edu in site.data.bio.education %}
<p class="mt-3 mb-1">
  <strong>{{ edu.institution }}</strong>{% if edu.degree %}, <em>{{ edu.degree }}</em>{% endif %}
  {% if edu.date %} <span class="text-muted">({{ edu.date }})</span>{% endif %}
</p>
{% if edu.details.size > 0 %}
<ul class="mb-2">
{% for line in edu.details %}
  <li>{{ line }}</li>
{% endfor %}
</ul>
{% endif %}
{% endfor %}

<div class="mt-5"></div>

## Experience

{% for exp in site.data.bio.experience %}
<p class="mt-3 mb-1">
  <strong>{{ exp.role }}</strong> @ {{ exp.institution }}{% if exp.extra %}, {{ exp.extra }}{% endif %}
  {% if exp.date %} <span class="text-muted">({{ exp.date }})</span>{% endif %}
</p>
{% if exp.items.size > 0 %}
<ul class="mb-2">
{% for item in exp.items %}
  <li>{{ item.text }} <span class="text-muted">({{ item.date }})</span></li>
{% endfor %}
</ul>
{% endif %}
{% endfor %}

<div class="mt-5"></div>

## Leadership & Activities

<ul class="mb-2">
{% for award in site.data.bio.award %}
  <li>{{ award.detail }} <span class="text-muted">({{ award.date }})</span></li>
{% endfor %}
</ul>

<div class="mt-4"></div>

<p>
  <a class="btn btn-sm z-depth-0" href="{{ '/assets/pdf/wasif_faisal_cv.pdf' | relative_url }}" target="_blank" rel="noopener noreferrer">
    <i class="fa-solid fa-file-pdf"></i> Download Full CV (PDF)
  </a>
</p>

