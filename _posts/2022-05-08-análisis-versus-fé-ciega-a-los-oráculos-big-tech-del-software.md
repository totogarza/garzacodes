---
layout: post
title: Análisis versus fé ciega a los oráculos big tech software
date: 2022-05-08 17:32 -0600
categories: programación
---

Es indudable las aportaciones que hacen los grandes corporativos a la industria del software pero sus problemas no son los mismos que los problema de las pequeñas o micro empresas y me refiero a que estas empresas diseñan soluciones con visión de su propia organización interna y si esta es compleja también lo serán sus soluciones y esto es normal y no lo digo a forma de criticarles o juzgarles, más bien todo lo contrario, lo digo a manera de crítica para aquellos de nosotros que no llevamos un análisis para las organizaciones para las que laboramos y no determinamos con base a evidencia cual es el mejor camino a seguir para llevar a cabo un proyecto.

Un análisis profundo arrojará información en torno a los recursos de una empresa y sus características únicas así como sus posibilidades en el futuro y es con esta información que se debe partir para tomar decisiones de qué tecnologías se debierán usar para desarrollar un proyecto para la empresa. El problema es que esto no ocurre con frecuencia y la razón de esto se debe a múltiples posibilidades que van desde la inexperiencia de la persona a cargo, la falta de interés por conocer más la organización y solo enfocarse en lo tecnológico, comodidad por lo que ya se sabe, etc.

A lo que me refiero concretamente es que líderes programadores en pequeñas organizaciones se van más por lo que está de moda, y no necesariamente en tecnología si no también en arquitectura, y un ejemplo de esto es la fragmentación de proyectos en backende para frontends, una arquitectura muy aceptada y ampliamente difundida.

No hay nada malo con la arquitectura antes mencionada, de hecho no hay nada malo con las arquitecturas en general, más bien es cuestión de ver desde la perspectiva del contexto y este es el que nos dice cuando algo está mal o cuando algo esta bien (con sus pro y contras claro está).

El contexto nos arroja luz sobre como es que deberíamos proceder tomando en cuenta los diferentes aspectos enfatizados por los dueños del producto y la organización.

Supongamos una empresa pequeña sin amplio presupuesto para mantener al menos un backend y un frontend, limitada a la contratación de sola una persona ¿qué recomendarías a una empresa así?

Si no se pueden contratar dos personas entonces dirás que se consiga un unicornio, seguro habrá algunos cuanto en algún lado, pero en realidad es que la gestión de un proyecto que ahora serán dos, para una persona y bajo ciertos _deadlines_ no es una buena fórmula y mi punto aquí es defender algo que quizá muchos ya están adiestrados para rechazar y me refiero a otra arquitectura, los __monolitos__.

En este contexto un monolito pueda ser mejor arquitectura dado que es posible mantener un solo proyecto con las características mismas con las que interactuará el usuario lo cual tiene una cierta ventaja ya que no hay que saltar de proyecto en proyecto para los cambios, todo queda en un solo repositorio. Hay muchas más personas muy eficientes en esta arquitectura que en su alternativa de separar la vista de la lógica de negocio, y tal es el caso de las personas que manejan frameworks como __Djnago__, __Ruby on Rails__ o __Laravel__. Estas personas ya están listas para entregar proyectos desplegables en un solo click sin necesidad de más manos.

Una organización pequeña reflejará su estructura en muchas cosas de las que diseña para sí y el software no es la excepión y por ende es muy probable que una organización con las características antes mencionadas no sobrepase su propia complejidad en sus desarrollos y por ende va bien con una persona y arquitectura de monolito.

¿Qué hay de la capa (API) para aplicaciones móviles? ciertamente esta no debe quedar fuera y una arquitectura backend para frontend esta se da naturalmente y es el contra del monolito, pero tampoco es tan complicado agregar progresivamente pero también es cierto que en muchas aplicaciones empresariales el acceso a través de móvil desde app nativa no es tan frecuente (dependiendo la aplicación claro está) y de requerirse siempre está la opción de __aplicaciones web progresivas__.

El enfoque es por supuesto desde el punto de vista de lo que beneficie más a la empresa y por ello la parte personal (sesgo) debería quedar fuera de la fórmula de lo contrario incurriremos en una mala decisión sin duda alguna.



