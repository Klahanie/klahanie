---
layout: default
title: Clubs and Groups
date: 2019-06-10 07:55
author: Klahanie
comments: true
categories: [clubs]
show-title: true
---
{% for doc in site.clubs %}
{% if doc.link == true %}
<div class="row mb-4">
  {% if doc.thumbnail != nil %}
    <img class="img-thumbnail col-md-2" src="{{doc.thumbnail}}">
  {% endif %}
    <div class="col-md-10">
      <h4>
      <a href="{{doc.url}}">{{doc.title}}</a>
      </h4>
      <div>{{doc.description}}
      </div>
    </div>
</div>
{% endif %}
{% endfor %}
