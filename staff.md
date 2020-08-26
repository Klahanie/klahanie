---
layout: default
title: Staff
date: 2020-08-25 00:00
author: Klahanie
comments: true
show-title: true
categories: []
---
{% for staff in site.staff %}
{% if staff.title != "Staff" %}
<div class="director-row row mb-4">
  <div class="col-md-4 col-sm-6">
{% if staff.thumbnail != nil %}
  <img class="img-thumbnail img-fluid" src="{{site.url}}/{{staff.thumbnail}}" alt="{{staff.title}}">
    {% endif %}
    </div>
    <div class="col-md-8 col-sm-12">
      <h4>
      <a href="mailto:{{staff.email}}">{{staff.title}}</a>
      </h4>
      <h5>{{staff.position}}</h5>
      <div>{{staff.content}}
      </div>
    </div>
</div>
{% endif %}
{% endfor %}

