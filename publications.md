---
layout: page
title: Publications & Recognition
permalink: /publications/
---

<div class="page-header">
  <h1>Publications &amp; Recognition</h1>
  <p class="subtitle">Papers, articles, and awards.</p>
</div>

<div class="page-section-label">Publications</div>

{% if site.data.publications.size > 0 %}
<div class="entry-list">
{% for pub in site.data.publications %}
<div class="entry-card">
  <h3>{{ pub.title }}</h3>
  <div class="entry-meta">{{ pub.year }}{% if pub.venue %} · {{ pub.venue }}{% endif %}{% if pub.authors %} · {{ pub.authors }}{% endif %}</div>
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

{% if site.data.awards.size > 0 %}
<div class="page-section-label" style="margin-top:3rem;">Awards &amp; Recognition</div>
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
