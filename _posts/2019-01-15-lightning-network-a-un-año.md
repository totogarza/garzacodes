---
layout: post
title: Lightning Network a un año
date: 2019-01-15 09:45 -0700
categories: basic
---

Ya es un poco más de un año desde el lanzamiento de __LN__ a la _mainnet_ de __Bitcoin__ y es impresionante todo el trabajo que programadores por todo el mundo han estado realizando para mejorar el protocolo y también construyendo encima de este.

Yo mismo no pude esperar a realizar pruebas con LN y Bitcoin y la sensación que a uno le deja el resultado (poder operar todo un sistema de procesamiento de pagos desde casa) es empoderante.

Sobra decir que fue tanta la emoción que tuve que grabarlo y a pesar de que ya ha pasado un año desde mi primera prueba (el video captura a esa prueba) aún me sigue impresionando el potencial que yace en Bitcoin y LN.

 <video width="100%"  controls>
  <source src="https://res.cloudinary.com/yipster/video/upload/v1547571266/starblocks-ln_zrcmgm.mov" type="video/mp4">
Your browser does not support the video tag.
</video>

Lo que sucede en este video es una transacción de LN. Starblocks es una compañía falsa que vende café y su única opción de pago es Bitcoin (por medio de LN). Así que cuando uno elige el producto que desea comprar el sistema de Starblocks le genera un código el cual uno escanea con aplicación compatible con LN; si el cliente tiene fondos en su cartera LN la transacción se realizará con éxito y sin espera (a diferencia de lo que sucede con Bitcoin por sí solo). En mi caso no usé ninguna aplicación móvil ni de escritorio si no que lo hice directamente a través de LND (Lightning Network Daemon) la cual es una implementación de Lightning Network programada en el lenguaje de programación __Go__.

Todos estos protocolos son la infraestructura que permitirán construir toda clase de servicios financieros (Bitcoin no es solamente un token, puede serlo pero puede ser más que eso). Por ejemplo, la compañía detrás de Starblocks (la cafetería falsa lanzada para probar LN), [Acinq](https://acinq.co), creó una alternativa a Stripe (el servicio que permite a individuos y empresas realizar y recibir pagos en línea), esta alternativa (que corre en LN - Bitcoin) es [Strike](https://strike.acinq.co/).

Lo que permite _Strike_ es tener todo un sistema de pago (en Bitcoin-LN ) sin tener que mantener un nodo de Bitcoin y todo el trabajo que implica eso. Pero si deseas tu ser el propio manejador del sistema  (que tiene la ventaja de no pagar comisiones a un tercero) existen otras alternativas como [BTCPay](https://btcpayserver.org) que es open source y que tú mismo alojas (lo cual puede ser un fastidio ya que tú mismo lo tendrás que mantener) y así te convertirás en el propio dueño del procesador de pagos; además podrías realizar ajustes  para proveer a otros del servicio y generar un ingreso extra de las comisiones de venta de otros.

Muchas más cosas interesantes están sucediendo en este sector y solamente en Bitcoin pero eso tema para otro post.