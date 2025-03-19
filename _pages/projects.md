---
title: "Projects"
permalink: /projects/
layout: single
author_profile: true
---

{% assign sorted_projects = site.projects | sort: "year" | reverse %}

{% for project in sorted_projects %}
### {{ project.year }}

- **[{{ project.title }}]({{ project.url }})**
{% endfor %}
