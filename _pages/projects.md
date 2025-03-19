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
  <h2 id="{{ project.year | slugify }}" class="archive__subtitle">{{ project.year }}</h2>
  ## {{ project.year }}
  {% assign current_year = project.year %}
  {% endif %}

  - **[{{ project.title }}]({{ project.url }})**
{% endfor %}
