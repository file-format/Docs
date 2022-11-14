---
date: 2022-01-06
keywords: vtt, .vtt, formato de archivo vtt, formato de archivo .vtt, extensión .vtt, extensión vtt
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Obtenga información sobre el archivo .vtt y las API que pueden crear y abrir archivos VTT."
title: "Formato de archivo VTT: archivo de pistas de texto de video web"
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## ¿Qué es un archivo VTT?

Un archivo VTT es un archivo de texto que contiene información para mostrar pistas de texto cronometradas (como subtítulos o subtítulos) usando el formato de pistas de texto de video web (WebVTT). Las pistas de texto cronometradas incluyen información como subtítulos o subtítulos. El propósito del archivo VTT es agregar superposiciones de texto a un<video> . El formato es algo similar a los archivos SRT. Los archivos de texto basados en WebVTT se codifican con UTF-8. Un archivo VTT contiene información como subtítulos, descripciones, subtítulos, descripciones, capítulos y metadatos. Al ser archivos de texto sin formato, los archivos VTT se pueden abrir con editores de texto como Microsoft Notepad, Apple TextEdit y Notepad ++.

## Formato de archivo VTT - Más información

Los archivos VTT usan el formato de archivo WebVTT para guardar información de pistas de texto secuencial. Cada pista de texto cronometrada consta de una sola línea o de varias líneas, también conocidas como `cue`, como se muestra en el siguiente ejemplo.

### Ejemplo de archivo VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Estructura del archivo VTT

Los siguientes son los requisitos de estructura de un archivo VTT.

* Una marca de orden de bytes (BOM) opcional.
* La cadena "WEBVTT".
* Un encabezado de texto opcional a la derecha de WEBVTT.
* Una línea en blanco, que equivale a dos saltos de línea consecutivos.
* Cero o más pistas o comentarios.
* Cero o más líneas en blanco.

## Referencias

* [VTT - Escuelas W3](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

