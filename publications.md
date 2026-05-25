---
layout: page
title: Publications
permalink: /publications/
---

<div class="page-header">
  <h1>Publications</h1>
  <p class="subtitle">Articles, papers, and reports.</p>
</div>

{% if site.data.publications.size > 0 %}
<div class="entry-list">
{% for pub in site.data.publications %}
<div class="entry-card">
  <h3>{{ pub.title }}</h3>
  <div class="entry-meta">{{ pub.year }}{% if pub.venue %} · {{ pub.venue }}{% endif %}</div>
  {% if pub.description %}<p class="entry-desc">{{ pub.description }}</p>{% endif %}
  <div class="entry-links">
    {% if pub.link %}<a class="entry-link" href="{{ pub.link }}" target="_blank" rel="noopener">Read →</a>{% endif %}
    {% if pub.pdf %}<a class="entry-link" href="{{ pub.pdf }}" target="_blank" rel="noopener">PDF →</a>{% endif %}
  </div>
</div>
{% endfor %}
</div>
{% else %}
<p style="color:#94a3b8;font-size:0.9rem;">Publications will appear here — add entries to <code>_data/publications.yml</code>.</p>
{% endif %}
