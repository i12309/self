---
layout: page
title: "Список"
permalink: /stories/
---

{% assign stories_with_order = site.stories | where_exp: "s", "s.order != nil" | sort: "order" %}
{% assign stories_without_order = site.stories | where_exp: "s", "s.order == nil" | sort: "title" %}
{% assign stories = stories_with_order | concat: stories_without_order %}
{% if stories.size > 0 %}
<ul>
{% for story in stories %}
  <li><a href="{{ story.url | relative_url }}">{{ story.title | default: story.basename }}</a></li>
{% endfor %}
</ul>
{% else %}
<p>Пока нет историй.</p>
{% endif %}
