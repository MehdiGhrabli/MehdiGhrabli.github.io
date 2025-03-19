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
    <h3 style="color: gray; font-weight: bold; font-size: 1.4em; margin-top: 20px;">
      {{ project.year }}
    </h3>
  {% assign current_year = project.year %}
  {% endif %}

  - **[{{ project.title }}]({{ project.url }})**
{% endfor %}
