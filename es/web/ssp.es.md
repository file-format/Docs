---
date: 2021-07-05
keywords: ssp, .ssp, formato de archivo ssp, cómo abrir archivos ssp, Página del servidor Scala
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "SSP - Formato de archivo de páginas del servidor Scala"
linktitle: SSP
description: "Obtenga información sobre qué es un formato de archivo SSP y las API que pueden crear y abrir archivos SSP."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## ¿Qué es un archivo SSP?

Un archivo con extensión .ssp es una página web creada con código Scala para expresiones en lugar de solo HTML simple. Actúa como un script del lado del servidor usando la combinación de HTML y Scala. Estos archivos residen en el servidor y se utilizan para crear páginas web estáticas para servir a los usuarios. Scala en sí mismo es un lenguaje de programación de propósito general cuya sintaxis es familiar para los usuarios que han trabajado con Velocity, JSP o Erb. Los archivos SSP se pueden analizar y evaluar mediante [Scalate](https://scalate.github.io/scalate/), que es un motor de plantillas basado en Scala para generar texto y marcas.

## Formato de archivo SSP: más información

Los archivos SSP se guardan en un archivo de texto sin formato y se pueden evaluar con Scalate. Una plantilla Ssp consta de texto sin formato, que suele ser el documento HTML. Tiene etiquetas Ssp incrustadas que hacen que los motores de renderizado rendericen dinámicamente diferentes partes del documento. Las etiquetas comienzan y terminan con la secuencia <% ... %> y ${ ... } y todo lo que esté fuera de estos se considera texto literal.

### Ejemplo de SSP

El siguiente ejemplo muestra el código SSP y su salida cuando lo procesa el motor de procesamiento.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
La salida es la siguiente.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Referencias

- [Referencia SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

