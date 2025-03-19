---
title: "My Blog"
permalink: /blog/
layout: single
author_profile: true
---

## Blog Posts

{% for post in site.myposts %}
- **[{{ post.title }}]({{ post.url }})** ({{ post.date | date: "%B %d, %Y" }})
{% endfor %}
