---
title: "My Blog"
permalink: /blog/
layout: single
author_profile: true
---

## Blog Posts

{% assign sorted_posts = site.myposts | sort: "date" | reverse %}
{% for post in sorted_posts %}
- **[{{ post.title }}]({{ post.url }})** ({{ post.date | date: "%B %d, %Y" }})
{% endfor %}
