---
layout: page
title: Patents
permalink: /patents/
---

{% for patent in site.data.patents %}
### {{ patent.title }}
**{{ patent.year }}** · {{ patent.number }}{% if patent.status %} · *{{ patent.status }}*{% endif %}

{{ patent.description }}

{% if patent.link %}[View filing →]({{ patent.link }}){% endif %}

---
{% endfor %}
