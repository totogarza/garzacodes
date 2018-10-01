---
layout: post
title: Generando música aleatoriamente con JavaScript y GaragBand
---


Hace tiempo que dejé de tocar música con mis amigos e incluso para mí mismo pero tarde o temprano, cuando lo has dejado por tanto tiempo, regresa esa necesidad de tocar de nuevo y así ha sido en mi caso. Ya he pasado por esto otras veces y he logrado vencer la tentación, ya saben, uno debe enfocarse en lo que le produce a uno beneficio ¿no es cierto? !No!

Ya he ignorado muchas ocaciones esa necesidad y no lo haré de nuevo pero solo que en esta ocasión quiero integrar la música con uno de mis mayores placeres, programar 😎.

Hace tiempo que me percate de un movimiento creativo en el que se utiliza la programación para generar arte, algunos le llaman #CreativeCoding, otros #GenerativeArt; y lo he practicado un poco en la parte visual pero ahora quise probar con música, por lo que comenté antes y por que es, a mi manera de ver, un reto mayor.

Generar arte visual "atractivo" es más fácil que generar música armoniosa y es precisamente esta parte lo que es el truco y mi reto. Podemos generar música programáticamente pero no será música del todo ya que sin un orden y atención a las notas nuestra creación será solamente ruido.

## ¿Cómo hacemos entonces?

Esa es mi meta y en una serie de publicaciones en este blog iré dándo a conocer mis resultados; pero debo decir que ya muchos otros me llevan delantera en esto puesto que se han creado montones de liberías para facilitarnos el proceso creativo musical.

En mi caso he recurrido a [#Scribbletune](https://scribbletune.com) (la cual depende de [#Tonal](https://github.com/danigb/tonal)).

Scribbletune es todo un motor musical para JavaScript la cual nos coloca muy adelante en nuestro objetivo pero aún debemos hacer nuestro trabajo en la parte de generación musical sin interacción humana; y es que Scribbletune te brinda un montón de funcionalidades para que tú manualmente generes tus propias melodías.

Antes de proceder con Scribbletune y la generacion aleatoria te dejo una muestra del audio generado. Esta pieza (no esperes mucho) fue construida con múltiples archivos midi generados con Scribbletune (de manera aleatoria). Estos archivos fueron importados a GarageBand y luego en este elegí los instrumentos que sonaron mejor, a mi gusto, para cada archivo. Así de simple y sin más ni más. 

<audio src="https://res.cloudinary.com/yipster/video/upload/v1538356341/Proyecto_2_-_30_09_18_18.32_itmali.mp3" controls preload></audio>

```


```