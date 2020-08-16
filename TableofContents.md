---
layout: page
title: Blog ToC
permalink: /tableofcontents/
---

<div>
  <p><i>More Notes to be Updated <br> More Notes to be Updated </i></p>
</div>

<ul>
  {% for post in site.posts %}
    <li>
      {{ post.date | date: '%Y-%m-%d'}}
      <a href="{{ post.url }}" title="{{ post.excerpt | remove: '<p>' | remove: '</p>' }}">{{ post.title }}</a>
      {% if post.update %}
          [{{ post.update }}]
      {% endif %}
    </li>
  {% endfor %}
</ul>
