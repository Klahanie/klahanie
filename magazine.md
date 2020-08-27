---
layout: default
title: Klahanie Magazine
date: 2019-06-10 04:37
author: Klahanie
comments: true
categories: [magazine]
show-title: true
---

{% for doc in site.magazine reversed %}
{% if doc.title != "Klahanie Magazine" %}

<div class="row mb-4">
  <img class="img-thumbnail col-md-2" src="{{site.url}}/magazine/{{doc.filename}}.jpg">
    <div class="col-md-10">
      <h4>
      <a href="{{site.url}}/magazine/{{doc.filename}}.pdf">{{doc.title}}</a>
      </h4>
      <div>{{doc.description}}
      </div>
    </div>
</div>
{% endif %}
{% endfor %}
