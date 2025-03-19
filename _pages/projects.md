---
title: "Projects"
permalink: /projects/
layout: single
author_profile: true
---

{% assign sorted_projects = site.projects | sort: "year" | reverse %}
{% assign current_year = "" %}

{% for project in sorted_projects %}
  {% if project.year != current_year %}
  <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ project.year }}</h2>
  {% assign current_year = project.year %}
  {% endif %}

  - **[{{ project.title }}]({{ project.url }})**
{% endfor %}
