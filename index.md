---
layout: main
class: "post"
title: "Tanoshii"
---

<h4>
Escritos recientes:
</h4>
<ul class='big-list'>
    {% for post in site.categories.basic limit:5 %}
        {% if post.url %}
        <li><a title='{{post.date}}' href='{{ post.url }}'>{{ post.title }}</a></li>
        {% endif %}
    {% endfor %}
    {% if site.categories.basic.size > 5 %}
    <li><em><a href='/archivo'>Hay {{ site.categories.basic.size | minus: site.categories.project.size  }} más en el archivo…</a></em></li>
    {% endif %}

</ul>
