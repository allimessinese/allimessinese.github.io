---
layout: page
title: Projects
permalink: /projects/
---

<div class="page-header">
  <h1>Projects</h1>
  <p class="subtitle">A complete log — research, engineering, business, leadership, teaching</p>
</div>

{% assign sorted = site.projects | sort: "year" | reverse %}
<div class="article-grid">
{% for project in sorted %}
<a class="article-card{% if project.featured %} feature{% endif %}" href="{{ project.url }}">
  <div class="article-image {{ project.gradient | default: 'grad-1' }}">
    {% if project.image %}<img src="{{ project.image | relative_url }}" alt="{{ project.title }}">{% endif %}
  </div>
  <div class="article-body">
    <span class="article-kicker">{{ project.tags | first }}</span>
    <h2 class="article-title">{{ project.title }}</h2>
    <div class="article-byline">{{ project.role }}{% if project.institution %} · {{ project.institution }}{% endif %} · {{ project.year }}</div>
    <p class="article-summary">{{ project.summary }}</p>
    <span class="article-read-more">Read article</span>
  </div>
</a>
{% endfor %}
</div>
