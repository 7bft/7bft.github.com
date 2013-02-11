---
layout: page
title: Hannes Gruber
tagline: Teamlead @ bwinparty, Skiing, MTB, Hiking, Father, Husband
---
{% include JB/setup %}

 
<ul class="posts square">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

#### To-Do

This page is still unfinished. 


