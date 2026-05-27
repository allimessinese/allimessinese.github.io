---
layout: page
title: Patents
permalink: /patents/
---

<div class="page-header">
  <h1>Patents</h1>
  <p class="subtitle">Patent filings and grants.</p>
</div>

<div class="entry-list">
{% for patent in site.data.patents %}
<div class="entry-card">
  <h3>{{ patent.title }}</h3>
  <div class="entry-meta">{{ patent.year }}{% if patent.number %} · {{ patent.number }}{% endif %}{% if patent.status %} · <em>{{ patent.status }}</em>{% endif %}</div>
  {% if patent.description %}<p class="entry-desc">{{ patent.description }}</p>{% endif %}
  <div class="entry-links">
    {% if patent.link %}<a class="entry-link" href="{{ patent.link }}" target="_blank" rel="noopener">View filing →</a>{% endif %}
    {% if patent.pdf %}<a class="entry-link" href="{{ patent.pdf | relative_url }}" target="_blank" rel="noopener">Patent (PDF) ↓</a>{% endif %}
    {% if patent.pdf_figures %}<a class="entry-link" href="{{ patent.pdf_figures | relative_url }}" target="_blank" rel="noopener">Figures (PDF) ↓</a>{% endif %}
    {% for proj in patent.projects %}
    <a class="entry-link" href="/projects/{{ proj }}/">Related project →</a>
    {% endfor %}
  </div>
</div>
{% endfor %}
</div>
