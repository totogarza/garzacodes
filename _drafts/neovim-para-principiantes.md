---
layout: post
title: NeoVim para principiantes
---

![Neovim primeros pasos](https://youtu.be/KDqxGuULOyQ)

En el comienzo estaba VIM pero luego algunos desarrolladores comenzaron a tener descontento con la comunidad y con el dictador de por vida (el creador de VIM) y uno de ellos decidió hacer un fork y refactorizar todo VIM y así es como surge **NeoVim**.

Lo anterior es una sobresimplificación de lo que sucedió pero estoy seguro hay mucho más en esta historia de lo que el parrafo anterior le hace honor pero nuestra intención no esescribir esa historia en un post ya que lo que realmente nos interesa es comenzar a escribir es NeoVim.

¿Por que NeoVim y no VIM? 

La razón principal es que si nos aclimatamos a este editor con el tiempo querremos desarrollar nuestros propios plugins o agregar mejoras a NeoVim y la comunidad de NV es más amigable y esto nos ayudará en nuestro camino de aprendizaje y desarrollo de herramientas para este ecositema.

Antes de comenzar es bueno aclarar que VIM y NeoVIM son de alguna manera lo mismo, no pienses que por ser Neo será más fácil de utilizar que el viejo VIM así que no te hagas ilusiones con eso.

NV es lo mismo pero mejorado, pero podrás utilizar los plugins de VIM sin problema (en su mayoría). 

Y pues manos a la obra.

Para aprendir NV (o VIM) en mi caso la mejor estrategia ha sido no querer aprender todo de una y lo que hago es que primero me familiarizo con unos cuantos comandos y trabajo conellos por un tiempo hasta sentir que ya los tengo dominados, a partir de ese momento comienzo a agregar nuevos comandos los cuales elijo por gusto (aquellas que sentí he necesitado previamente).

Obviamente los más importante al comienzo son los comandos que te ayudarán a entrar, salir, guardar, editar y moverte en el editor.

```{bash}

nvim #Para entrar al editor

nvim archivo.txt #Para editar un archivo específico

```

Estos comando son fuera de VIM, y los utilizas en el contexto de tu aplicación de línea de comandos, pero a continuación veremos algunos comandos específicos de NV (todo aplica a VIM).

![Meme: "Como salir de VIM"](https://pics.onsizzle.com/just-memorize-these-fourteen-contextually-dependant-instructions-exiting-vim-eventually-3125824.png)

Son clásicos los memes sobre lo "difícil" que es salir de la interfaz de VIM pero creo que ese problema no es en realidad un problema de VIM si no de nuestra mente y el miedo que tenemos a VIM (este miedo en parte es culpa de aquellos programadores que han ayudado a fomentar el mito). Pero no temas pues en realidad es muy fácil (bueno no muy fácil pero tampoco tan difícil) y lo único que deberás hacer es eliminar de tu mente (o olvidarte por un momento) todo aquello que sabes sobre editores.

Piensa que en NV hay 2 estados activo, que es dónde escribes, y comandos, que es dónde ejecutas comandos para cualesquier tarea que deseas realizar.

El primer estado es el de Inserción y lo activas con la tecla **i**, sí, así  de simple. Si VIM no está en modo de inserción lo notarás ya que no puedes escribir nada, pareciera que el editor está congelado o infuncional (al menos esa es la sensación que me daba viniendo de un mundo de IDEs). Teclea la **i** y VIM te permitirá escribir.

Si deseas dejar de escribir por cualesquier razón (quizá deseas guardar tu trabajo) es muy simple, solo teclea **ESC** y entrarás en un modo neutral (si debí haber comentado antes que hay un modo neutral) 

El modo neutral no es más que VIM esperando que le digas que hacer, si deseas continuar editando tu trabajo o si ejecutarás algún comando y eso es lo que aprenderemos a continuación.

Estamos en estado neutral y queremos salvar nuestro trabajo así que para hacer eso tenemos que teclear **:** VIM sabe que quieres ejecutar un comando pero los **:** por sí solos no son suficientes y necesita saber que comando (o que tarea deseas realizar), así que guardaremos nuestro trabajo y el comando para ello es **w**.

Ok genial hemos guardao correctamente y VIM nos regreso al estado neutral, ¿quieres seguir editando tu trabajo o desear salir?

Digamos que quieres salir, entonces para ello tecleamos **:q** y listo, estaremos de vuelta en nuestra línea de comandos.

Hay otras maneras de guardar y salir como el comando **:wq** o este otro comando, que te parecerá raro **ZZ** (sí, zetas mayúsculas).

Ahora regresaremos a editar nuestro documento y hay varias líneas de código en este pero queremos continuar en la parte baja del mismo, con lo que sabes hasta ahora te percatarás que es muy tedioso navegar hasta el final línea por línea ¿sabes que VIM tiene un comando para eso verdad? y sí, es **G**.

Pero tal vez quieras ir párrafo por párrafo y para ello tecleas **{** para ir para arriba y **}** para ir para abajo.

A estas alturas ya habrás comprendido la mecánica en la que funciona VIM y tú mismo te estarás preguntando ¿si quiero ir al final o comienzo de una línea que comando tendrá VIM? y eso es bueno ya que tú mismo buscarás los comandos que te urgen y los pondrás en práctica poco a poco y eventualmente ya estarás escribiendo todo en VIM. Ah por cierto, esos comandos que buscas son **0** para el, sí acertaste, comienzo de la línea y **$** para el final.

Por cierto, no quieras aprenderte todos los comandos ya que con toda seguridad solo usarás unos cuantos y esto dependerá del workflow que adoptes.


