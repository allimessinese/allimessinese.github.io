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
<div class="project-grid">
{% for project in sorted %}
<a class="project-card" href="{{ project.url }}">
  <div class="card-image {% if project.image == blank or project.image == nil %}{{ project.gradient | default: 'grad-1' }}{% endif %}"
       {% if project.image %}style="background-image: url('{{ project.image | relative_url }}')"{% endif %}>
    {% if project.image %}<img src="{{ project.image | relative_url }}" alt="{{ project.title }}">{% endif %}
    <div class="card-image-overlay"></div>
    <span class="card-year">{{ project.year }}</span>
  </div>
  <div class="card-body">
    <div class="card-tags">
      {% for tag in project.tags limit:3 %}<span class="tag">{{ tag }}</span>{% endfor %}
    </div>
    <div class="card-title">{{ project.title }}</div>
    {% if project.role or project.institution %}
    <div class="card-role">{% if project.role %}{{ project.role }}{% endif %}{% if project.role and project.institution %} · {% endif %}{% if project.institution %}{{ project.institution }}{% endif %}</div>
    {% endif %}
    <p class="card-summary">{{ project.summary }}</p>
    <span class="card-cta">Read more →</span>
  </div>
</a>
{% endfor %}
</div>
