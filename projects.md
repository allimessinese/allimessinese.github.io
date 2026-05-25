---
layout: page
title: Projects
permalink: /projects/
---

<div class="page-header">
  <h1>Projects</h1>
  <p class="subtitle">A complete log of everything I've worked on — research, engineering, business, leadership, and teaching.</p>
</div>

{% assign sorted = site.projects | sort: "year" | reverse %}
<div class="project-list">
{% for project in sorted %}
<div class="project-card">
  <div class="project-card-meta">
    <span class="year-badge">{{ project.year }}</span>
    {% for tag in project.tags %}<span class="tag">{{ tag }}</span>{% endfor %}
  </div>
  <a class="project-card-title" href="{{ project.url }}">{{ project.title }}</a>
  {% if project.role or project.institution %}
  <div class="project-card-role">{% if project.role %}{{ project.role }}{% endif %}{% if project.role and project.institution %} · {% endif %}{% if project.institution %}{{ project.institution }}{% endif %}</div>
  {% endif %}
  <p class="project-card-summary">{{ project.summary }}</p>
  <a class="read-more" href="{{ project.url }}">Read more →</a>
</div>
{% endfor %}
</div>
