---
layout: default
title: Announcements
date: 2019-07-01 04:30
author: Klahanie
show-title: true
---
<ul>
    {% for doc in site.announcements reversed %}
    {% if doc.url != 'index.html' %}
        <li><a href="{{ doc.url }}">{{doc.date | date: "[%B %d, %Y]" }} {{ doc.title }}</a></li>
    {% endif %}
    {% endfor %}
</ul>


