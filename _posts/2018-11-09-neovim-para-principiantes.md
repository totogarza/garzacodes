---
layout: post
title: NeoVim para principiantes
---

<iframe width="501" height="282" src="https://www.youtube.com/embed/KDqxGuULOyQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

En el comienzo estaba VIM pero luego algunos desarrolladores comenzaron a tener descontento con la comunidad y con el dictador de por vida (el creador de VIM) y uno de ellos decidió hacer un fork y refactorizar todo VIM (esa es una de las metas) y así es como surge **NeoVim**.

Lo anterior es una sobresimplificación de lo que sucedió pero estoy seguro hay mucho más en esta historia de lo que el parrafo anterior le hace honor pero nuestra intención no es escribir esa historia en este post ya que lo que realmente nos interesa es comenzar a escribir en NeoVim.

¿Por que NeoVim y no VIM? 

La razón principal es que si nos aclimatamos a este editor con el tiempo querremos desarrollar nuestros propios plugins o agregar mejoras a NeoVim y la comunidad de NV es más amigable y esto nos ayudará en nuestro camino de aprendizaje y desarrollo de herramientas para este ecositema.

Antes de comenzar es bueno aclarar que VIM y NeoVIM son de alguna manera lo mismo, no pienses que por ser Neo será más fácil de utilizar que el viejo VIM así que no te hagas ilusiones con eso.

Para aprender NV (o VIM) en mi caso la mejor estrategia ha sido no querer aprender todo de una y lo que hago es que primero me familiarizo con unos cuantos comandos y trabajo con ellos por un tiempo hasta sentir que ya los tengo dominados, a partir de ese momento comienzo a agregar nuevos comandos los cuales elijo por gusto o necesidad.

Obviamente los más importante al comienzo son los comandos que te ayudarán a entrar, salir, guardar, editar y moverte en el editor.

```{bash}

nvim #Para entrar al editor

nvim archivo.txt #Para editar un archivo específico

```

![Meme: "Como salir de VIM"](https://pics.onsizzle.com/just-memorize-these-fourteen-contextually-dependant-instructions-exiting-vim-eventually-3125824.png)

Son clásicos los memes sobre lo "difícil" que es salir de la interfaz de VIM pero creo que ese problema no es en realidad un problema de VIM si no de nuestra mente y el miedo que tenemos a VIM (este miedo en parte es culpa de aquellos programadores que han ayudado a fomentar el mito). Pero no temas pues en realidad es muy fácil y lo único que deberás hacer es eliminar de tu mente (o olvidarte por un momento) todo aquello que sabes sobre editores.

Ya que te has olvidado de como funcionan los otros editores ahora piensa en vim de manera diferente, no te acerques a este de la misma manera que con otros editores, vim es como el agua y los estados de la materia, líquido, sólido y gaseoso, cada estado puede servir a distintos propósitos, así vim tiene distintos estados que sirven para distintas tareas, por ejemplo el estado de inserción el cual te servirá para escribir tu contenido ya sea código o texto, el modo visual que te servirá para seleccionar el contenido que has escrito (ya sea porciones o el todo) y por último un estado inactivo que es el estado en que puedes ejecutar comandos para las tareas que tu quieras (guardar, salir, abrir otros archivo, buscar, etc).

El estado de __Inserción__ y lo activas con la tecla __i__, sí, así  de simple. Si VIM no está en modo de inserción lo notarás ya que no podrás escribir nada, parecerá que el editor está congelado o infuncional (al menos esa es la sensación que me daba viniendo de un mundo de IDEs).

Si deseas dejar de escribir por cualesquier razón (quizá deseas guardar tu trabajo) es muy simple, solo teclea **ESC** y entrarás en un modo neutral o inactivo.  

El modo neutral no es más que VIM esperando que le digas que hacer, si deseas continuar editando tu trabajo o si ejecutarás algún comando.

Estamos en estado neutral y queremos salvar nuestro trabajo así que para hacer eso tenemos que teclear **:w**. 

Ok genial hemos guardado correctamente y seguimos en el estado neutral, ¿quieres seguir editando tu trabajo o desear salir?

Digamos que quieres salir, entonces para ello tecleamos **:q** y listo, estaremos de vuelta en nuestra línea de comandos.

Hay otras maneras de guardar y salir como el comando **:wq** o este otro comando, que te parecerá raro **ZZ** (sí, zetas mayúsculas).

Digamos que hemos regresado a editar nuestro documento y hay varias líneas de código en este pero queremos continuar en la parte baja del mismo, con lo que sabes hasta ahora te percatarás que es muy tedioso navegar hasta el final línea por línea ¿sabes que VIM tiene un comando para eso verdad? y sí, es **G** (_SHIFT + g_).

Pero tal vez quieras ir párrafo por párrafo y para ello tecleas **{** para ir para arriba y **}** para ir para abajo.

A estas alturas ya habrás comprendido la mecánica en la que funciona VIM y tú mismo te estarás preguntando ¿si quiero ir al final o comienzo de una línea qué comando tendrá VIM? y eso es bueno ya que tú mismo buscarás los comandos que te urgen y los pondrás en práctica poco a poco y eventualmente ya estarás escribiendo todo en VIM. Ah por cierto, esos comandos que buscas son **0** para el, sí acertaste, comienzo de la línea y **$** para el final.

Por cierto, no quieras aprenderte todos los comandos ya que con toda seguridad solo usarás unos cuantos y esto dependerá del workflow que adoptes.

No he olvidado esas teclas básicas para moverte en vim, me refiero a __l__ para ir a la izquierda, __k__ para ir hacia arriba, __j__ para ir hacia abajo y __h__ para ir a la derecha. Sí, estas son una alternativa a las flechas de nuestro teclado. La razón de estas se debe a que te permitirá ahorrar movimientos y sí te costará un poco acostumbrarte.  
