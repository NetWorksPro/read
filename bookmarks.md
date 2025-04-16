---
layout: page
title: 我的书签集
permalink: /bookmarks/
---

# 收藏夹

{% raw %}{% assign categories = site.data.bookmarks %}
{% for category in categories %}
## {{ category.name }}
<ul class="bookmarks">
  {% for item in category.items %}
  <li>
    <a href="{{ item.url }}" target="_blank" rel="noopener">
      {{ item.title }}
    </a>
    {% if item.desc %} - {{ item.desc }}{% endif %}
  </li>
  {% endfor %}
</ul>
