---
layout: page
title: Projects
permalink: /projects/
---

{% assign sorted_projects = site.projects | sort: "year" | reverse %}
{% for project in sorted_projects %}
## [{{ project.title }}]({{ project.url }})
**{{ project.year }}** {% if project.tags %} · {{ project.tags | join: ", " }}{% endif %}

{{ project.summary }}

---
{% endfor %}
