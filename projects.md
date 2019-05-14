---
layout: main
title: Proyectos
permalink: /proyectos
---

<h4>
Proyectos recientes:
</h4>
<ul class='big-list'>
    {% for post in site.categories.project limit:5  %}
        {% if post.url%}
        <li><a title='{{post.date}}' href='{{ post.url }}'>{{ post.title }}</a></li>
        {% endif %}
    {% endfor %}
</ul>