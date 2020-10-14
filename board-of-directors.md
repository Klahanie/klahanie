---
layout: default
title: Board of Directors
date: 2015-03-12 14:10
author: Klahanie
categories: [board, association]
show-title: true
---
Our Klahanie Board of Directors each serve three-year terms. They meet remotely via Zoom on the last Tuesday of each month at 7:00 p.m. All meetings are open to Klahanie residents. Please feel free to [email the board](mailto:board@klahanie.com) with any questions or comments.

{% for director in site.board %} <!-- this sorts by date, so you can tweak the date for each director page to tweak the order -->
<div class="director-row row mb-4">
    <img class="img-thumbnail col-md-2" src="{{site.url}}/{{director.thumbnail}}">
    <div class="col-md-10">
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
