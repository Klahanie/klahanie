---
layout: default
title: Announcements
date: 2019-07-01 04:30
author: Klahanie
show-title: true
is_index: true
permalink: /announcements/
pagination: 
  enabled: true
  collection: announcements
  permalink: '/page:num/'
---

{% for doc in paginator.posts %}
{% if doc.is_index != true %}
<div class="mb-4">
<h2><a href="{{site.url}}{{ doc.url }}">{{ doc.title }}</a></h2>
<small>{{doc.date | date: "%B %d, %Y" }}</small>
    
{{ doc.excerpt }}

<a href="{{ site.url }}{{ doc.url }}">Read more</a>
</div>
{% endif %}
{% endfor %}

{% if paginator.total_pages > 1 %}
<div class="row">
<div class="pagination mt-4 mx-auto">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path | prepend: site.url | replace: '//', '/' }}">&laquo; Prev</a>
  {% else %}
    <span>&laquo; Prev</span>
  {% endif %}

  {% for page in (1..paginator.total_pages) %}
    {% if page == paginator.page %}
      <span class="webjeda">{{ page }}</span>
    {% elsif page == 1 %}
      <a href="{{ paginator.first_page_path | prepend: site.url }}">{{ page }}</a>
    {% else %}
      <a href="{{ paginator.first_page_path | prepend: site.url | append: '/page:num/' | replace: ':num', page | replace: '//', '/' }}">{{ page }}</a>
    {% endif %}
  {% endfor %}

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path | prepend: site.url | replace: '//', '/' }}">Next &raquo;</a>
  {% else %}
    <span>Next &raquo;</span>
  {% endif %}
</div>
{% endif %}
</div>
