---
layout: post
title: 'Visualización en R: ¿Cuánto paga tú carrera?'
date: 2018-11-14 11:38 -0700
tags: r shiny flexdashboard
categories: basic
---

<a href="https://datic.shinyapps.io/cuanto-paga-mi-carrera" target="_blank"><img src="https://res.cloudinary.com/yipster/image/upload/v1542222396/cuanto-paga-mi-carrera_zhq91m.png" width="600px" alt="Vista previa - ¿Cuando paga mi carrera?"></a>

R es un lenguaje de programación muy _ad hoc_ para las estadísticas --nació para ello-- y en lo personal es un lenguaje que me es muy gustoso además de que su comunidad, muy científica, es genial y más que nada por la manera en que documentan sus contribuciones --muy profesionales--. Desearía que otras comunidades --como la de javascript-- fuesen igual de meticulosos que la comunidad de R.

Pero el motivo de este post es solo mostrar una de las tantas cosas que pueden lograrse con `R` y algunas de sus librerías.

[__Shiny__](https://shiny.rstudio.com/) es un paquete de R que te ayudará a crear visualizaciones profesionales y sin mucha labor y es con este tipo de proyectos que R destaca puesto que los individuos de esta comunidad sólo quieren ponerse a trabajar en sus investigaciones y este sentimiento se ve reflejado en sus paquetes ya que es meramente cuestión de ensamblar y no de aprender todo un stack y configuraciones; lo que quiero decir es que con R vas a lo que vas sin distracciones --obvimente `R` es genial en su ámbito y no será nada práctico para aplicaciones web sofisticadas ni nada por el estilo--.

Si tu intención es crear dashboards informativos deberías [echarle un vistazo a R](https://www.r-project.org/).

El siguiente vínculo es un dashboard que he creado --obviamente con R y algunos paquetes-- y lo único que pretende mostar es el salario al que un egresado de _x_ carrera podrá tener acceso, junto con su variantes por edad (menor de 30 años o mayor de 30 años) así como para aquellos con posgrado. Los datos los obtuve de __INEGI__ (México) y también de portales de empleo (debo decir que hay muchas discrepancias entre las ofertas y los datos del INEGI 🤔).

[Dashboard creado en R](https://datic.shinyapps.io/cuanto-paga-mi-carrera)

De verdad que R facilita estas tareas de análisis de datos y a diferencia de python -- que también es muy utilizado en este medio-- la herramientas para hacer este análisis ya vienen en el lenguaje predeterminadamente -- no hizo faltas buscar librerías como pandas (en el caso de python) ya que todo estaba ahí--. Después de tener analizado los datos mi intención era mostrarlos de manera atractiva en un dashboard así que recurrí a `shiny` y `flaxdahsboard`, este último te permite hacer dashboards desde un archivo markdown 😲. 

Lo batalloso fue integrar `shiny` con `flexdashboard` para que trabajarán en conjunto y es que a pesar de que `flexdashboard` provee métodos para esta tarea la realidad es que ir a algo medianamente avanzado es un poco más complicado -- mi error fue no haberme percatado antes que `flexdashboard` encapsula en widgets y uno debe generar su propio canal de comunicación para aquellos widgets creados por uno--.

Este sigue siento un __work in progress__ ya que quiero extender la información que se brinda además de corregir algunos detalles como caractéres latinos que me causaron problemas en este proyecto en específico.