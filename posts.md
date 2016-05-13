---
layout: page
title: Posts
order: 10
permalink: /posts/
---

{% assign prev = '' %}
{% for post in site.posts %}
    {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
    {% if year != prev %}
### {{ post.date | date: '%Y' }}
    {% endif %}
* <span class="date">{{ post.date | date: "%b %-d, %Y" }}</span>:  [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
    {% assign prev = year %}
{% endfor %}
