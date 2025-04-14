---
layout: page
title: 标签
permalink: /tag/
---

<div id="tag">
  <div class="post post-archive">
  {% for tag in site.tags %}
  <h3 id="{{ tag | first }}">{{ tag | first }}</h3>
  
    
    <!-- tags -->
    {% for tag in page.tags %}
  <a href="/tag/{{ tag | slugify }}/" class="tag tag-{{ tag | slugify }}">{{ tag }}</a>
{% endfor %}

  <ul>
      {% for post in tag.last %}
          <li><span class="date">{{ post.date | date: "%B %e, %Y" }}</span><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></li>
      {% endfor %}
  </ul>
  {% endfor %}
    
  </div>
</div>
