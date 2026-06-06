---
layout: page
title: Recognition
permalink: /publications/
---

<div class="page-header">
  <h1>Recognition</h1>
</div>

<div class="page-section-label">Awards</div>

{% if site.data.awards.size > 0 %}
<div class="entry-list">
{% for award in site.data.awards %}
<div class="entry-card">
  <h3>{{ award.title }}</h3>
  <div class="entry-meta">{{ award.year }} · {{ award.issuer }}</div>
  {% if award.description %}<p class="entry-desc">{{ award.description }}</p>{% endif %}
  <div class="entry-links">
    {% if award.page %}<a class="entry-link" href="{{ award.page | relative_url }}">Full article →</a>{% endif %}
    {% if award.link %}<a class="entry-link" href="{{ award.link }}" target="_blank" rel="noopener">Credential →</a>{% endif %}
  </div>
</div>
{% endfor %}
</div>
{% endif %}

<div class="page-section-label" style="margin-top:3rem;">In the Press</div>

{% for item in site.data.press %}
<div class="press-project-block">
  <div class="press-project-header">
    <span class="press-project-name"><a href="{{ item.project_url | relative_url }}">{{ item.project }}</a></span>
    <span class="press-project-meta">{{ item.total_outlets }} outlets &nbsp;·&nbsp; {{ item.languages }} &nbsp;·&nbsp; {{ item.year }}</span>
  </div>
  <p class="press-project-summary">{{ item.summary }}</p>
  <div class="press-highlight-list">
    {% for hit in item.highlights %}
    <a class="press-highlight-chip" href="{{ hit.url }}" target="_blank" rel="noopener">
      <span class="press-chip-outlet">{{ hit.outlet }}</span>
      <span class="press-chip-type">{{ hit.type }}</span>
    </a>
    {% endfor %}
  </div>
</div>
{% endfor %}
