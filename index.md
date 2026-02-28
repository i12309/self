---
layout: page
title: "Главная"
permalink: /
---

{% assign stories = site.stories | sort: "path" | reverse %}
{% if stories.size > 0 %}
<ul>
{% for story in stories %}
  <li><a href="{{ story.url | relative_url }}">{{ story.title | default: story.basename }}</a></li>
{% endfor %}
</ul>
{% else %}
<p>Пока нет историй.</p>
{% endif %}
