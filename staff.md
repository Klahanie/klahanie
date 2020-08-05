---
layout: default
title: Staff
date: 2019-05-19 06:19
author: Klahanie
comments: true
categories: []
---
<img src="{{site.url}}/images/staff/Staff-Group-Shot-larger.jpg" class="img-fluid">

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
      <div>{{staff.description}}
      </div>
    </div>
</div>
{% endif %}
{% endfor %}

