---
layout: post
title: Modelado del esquema para tu base de datos NOSQL
---

En el mundo relacional el propio sistema es que que te forza a modelar tus datos pero en el mundo NOSQL tu como desarrollador es el que tiene esa tarea y es que este tipo de base de datos te permite almacenar tus datos como lo desees pero esto no es necesariamente bueno para tu aplicación.

Los modelos de datos pueden evolucionar conforme la marcha.


## Retos de modelado

Las dudas más comunes son en torno a:

- Relaciones de los datos
- Normalization vs denormalization
- Homogeneo vs heterogeneo

## Relaciones

Modelar tus datos para acceder a las relaciones entre estos hay dos dos métodos que puedes utilizar  para modelar tus datos y estos son:

    - Referenciar
    - Embeber

Cada uno tiene sus ventajas y desventajas así como sus casos de uso, depende de tu necesidad será mejor usar uno sobre otro.

Pero que es aquello que nos dice cuando usar uno u otro.

Cuando requieres acceder a información la cual debe ir junta esto es un indicio de que tu modelado debe ser enbebido.

La volatidad es otro signo y si esta es baja eso nos dice que debemos embeber los datos. La volatilidad alta quiere decir que habrá actualizaciones constantes de esa información y por tanto haremos muchas solicitudes a ese documento y por cuestión de eficiencia no queremos traernos todo un documento con datos que no necesitamos para llevar a cabo esa actualización.

Un conjunto de valores o subdocumentos están ligados al documento principal.

El embebido es eficiente ya que  para acceder a la información que necesitamos solo es necesario hacer un viaje al servidor para obtener los datos.

El método por referencia es bueno cuando:

- Relaciones uno a muchos
- Relaciones muchos a muchos

Memoria --- Eficiencia

## Casos de uso

- Árbol jerárquico
- Keyword search
- Telemetry
- Logging