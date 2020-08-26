---
layout: default
title: Board of Directors
date: 2015-03-12 14:10
author: Klahanie
categories: [board, association]
show-title: true
---
The board meets every last Tuesday evening at 7:00 in the office. All meetings are open to members.

* [Email the Board](mailto:board@klahanie.com)

{% for director in site.board %} <!-- this sorts by date, so you can tweak the date for each director page to tweak the order -->
<div class="director-row row mb-4">
<div class="col-md-4 col-sm-6">
    {% if director.thumbnail != nil %}
    <img class="img-thumbnail img-fluid" src="{{director.thumbnail}}" alt="{{director.title}}">
    {% endif %}
    </div>
    <div class="col-md-8 col-sm-12">
    <h4 class="director-name">
      {{director.title}}
      </h4>
      {% if director.position != nil %}
        <h6>{{director.position}}</h6>
      {% endif %}
      <div class='director-bio'>
      {{director.bio}}
      </div>
    </div>
  </div>
{% endfor %}
