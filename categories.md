---
layout: page
title: Categories
order: 20
permalink: /categories/
---

{% for category in site.categories %}
### {{ category | first }} ({{ category | last | size }})
  {% for post in category.last %}
* <span class="date">{{ post.date | date: "%b %-d, %Y" }}</span>:  [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
  {% endfor %}
{% endfor %}
