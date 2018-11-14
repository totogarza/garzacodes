---
layout: post
title: Construcción de este sitio
date: 2018-07-17 18:00 -0600
categories: static
tags: jekyll
---


La verdad es que no hay mucho que decir ya que como podrás darte cuenta este sitio es muy sencillo y esto es intencional.

Las páginas web actuales se han tornado muy saturadas y esto me ha hecho extrañar los primeros días del internet, cuando todo era simplemente texto y vínculos; esta sencillez hacía muy fácil navegar y consumir información y eso es lo que quería para mi sitio personal así que con esto en mente enlisté algunos sitios muy sencillos que me hacían sentir casi como en los 90´s.

Debo confesar que este sitio es el clon de uno de estos sitios (pero solamente su caparazón):

- [https://macwright.org/](https://macwright.org/) 😅
- [https://pfrazee.hashbase.io/](https://pfrazee.hashbase.io/)

Estoy casi seguro que el sitio de (MacWright) es estático y que para manejarlo usa [Jekyll](https://jekyllrb.com/) (un generador de sitios estáticos creado por **GitHub**) y esto lo espéculo debido a que en su post [https://macwright.org/2016/05/03/the-featherweight-website.html](https://macwright.org/2016/05/03/the-featherweight-website.html) en el que explica detallitos de su sitio web, hace mención de esta herramienta pero sin dar más detalles.

Sí, mi sitio es un clon en lo visual pero detrás la funcionalidad en **Jekyll** es una ingienrería inversa (no fue nada difícil) y a continuación te explico que es lo que sucede tras bambalinas.

Primero veamos su página de inicio (sí, la de MacWright), si te fijas bien el muestra una sub sección en la que enlista sus últimas 5 entradas y después una línea que muestra un vínculo cuyo texto te dice cuantas entradas más tiene en su blog:

<img src="https://res.cloudinary.com/dfhxsuwjv/image/upload/v1531873702/Captura_de_pantalla_2018-07-17_a_la_s_18.25.06_n2glap.png" alt="Captura de sitio clonado" width="80%" class="image-border"/>

Dos cosas están sucediendo aquí:

1. El **bucle** de Jekyll para colocar las **entradas** recibe un **comando** para limitar la cantidad de estaas `limit:5`
2. Y para poder descontar de las **entradas** totales las 5 entradas más recientes usamos el comando `minus:5` y esta línea solamente la mostraremos en caso de haber 6 o más entradas 



Y así es como se vería el código:

{% highlight html %}
{% raw %}
<ul class='big-list'>
    
    {% for post in site.posts limit:5 %}
    <li><a title='{{post.date}}' href='{{ post.url }}'>{{ post.title }}</a></li>
    {% endfor %}

    {% if site.posts.size > 5 %}
    <li><em><a href='/archive'>And {{ site.posts.size | minus:5 }} more in the archive…</a></em></li>
    {% endif %}

</ul>
{% endraw %}    
{% endhighlight %}

La misma mecánica puede usarse en el resto de las subsecciones.

Y aquí lo dejaré para este post y en el siguiente veremos cómo recrear la sección de **topics** en el sitio de MacWright la cual  organiza las entradas de acuerdo a algún tema.