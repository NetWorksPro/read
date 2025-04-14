---
layout: page
title: 标签
permalink: /tag/
---

<div id="tag">
  <div class="post post-archive">
  {% for tag in site.tags %}
  <h3 id="{{ tag | first }}">{{ tag | first }}</h3>

  <ul>
    {% for tag_name in page.tags %}
  {% assign tag = site.data.tags[tag_name] %}
  <span class="tag" style="background-color: {{ tag.color }}">{{ tag.name }}</span>
{% endfor %}
    
      {% for post in tag.last %}
          <li><span class="date">{{ post.date | date: "%B %e, %Y" }}</span><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
      {% endfor %}
  </ul>
  {% endfor %}
    
  </div>
</div>
