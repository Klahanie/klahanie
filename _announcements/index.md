---
layout: default
title: Announcements
date: 2019-07-01 04:30
author: Klahanie
show-title: true
---
    {% for doc in site.announcements reversed %}
    {% if doc.url != 'index.html' %}
        <h2><a href="{{site.url}}{{ doc.url }}">{{doc.date | date: "[%B %d, %Y]" }} {{ doc.title }}</a></h2>
        {{doc.excerpt}}
        <p><a href="{{site.url}}{{doc.url}}">Read more</a></p>
    {% endif %}
    {% endfor %}


