---
layout: page
title: Publications
permalink: /publications/
---

{% for pub in site.data.publications %}
### {{ pub.title }}
**{{ pub.year }}** · {{ pub.venue }}

{{ pub.description }}

{% if pub.link %}[Read →]({{ pub.link }}){% endif %}
{% if pub.pdf %}[PDF →]({{ pub.pdf }}){% endif %}

---
{% endfor %}
