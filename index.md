---
layout: main
class: "post"
---

<h4>
Escritos recientes:
</h4>

<ul class='big-list'>
    {% for post in site.posts limit:5 %}
    <li><a title='{{post.date}}' href='{{ post.url }}'>{{ post.title }}</a></li>
    {% endfor %}
    {% if site.posts.size > 5 %}
    <li><em><a href='/archivo'>Hay {{ site.posts.size | minus:5 }} más en el archivo…</a></em></li>
    {% endif %}
</ul>

