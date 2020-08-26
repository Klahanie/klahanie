---
layout: default
title: Neighborhoods
date: 2019-07-23 21:12
author: Klahanie
categories: []
show-title: true
---

{% for doc in site.neighborhoods %}
{% if doc.title != "Neighborhoods" %}
<div class="row mb-4">
  <img class="img-thumbnail col-lg-2 col-md-5 col-sm-12" src="{{doc.thumbnail}}">
    <div class="col-lg-10 col-md-7 col-sm-12">
      <h4>
      <a href="{{doc.url}}">{{doc.title}}</a>
      </h4>
      <div>{{doc.description}}
      </div>
    </div>
</div>
{% endif %}
{% endfor %}
