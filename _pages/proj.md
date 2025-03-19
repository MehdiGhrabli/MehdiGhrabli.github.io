---
title: "My projects"
permalink: /projects/
layout: single
author_profile: true
---

## Blog Posts

{% assign sorted_posts = site.myprojects | sort: "date" | reverse %}
{% for post in sorted_posts %}
  {% if post.date <= site.time %}
  - **[{{ post.title }}]({{ post.url }})** ({{ post.date | date: "%B %d, %Y" }})
  {% endif %}
{% endfor %}
