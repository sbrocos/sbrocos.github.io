---
layout: post-list
title: Blog
permalink: /blog/
---

{% if site.posts.size > 0 %}
  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
            {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
            <span class="post-meta">{{ post.date | date: date_format }}</span>
        </a>
        
      </li>
    {% endfor %}
  </ul>
{% endif %}