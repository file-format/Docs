---
date: 2019-10-11
keywords: srt, .srt, formato de archivo srt, formato de archivo .srt, extensión .srt, extensión srt
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo SRT y las API que pueden crear y abrir archivos SRT."
title: Formato de archivo SRT
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## ¿Qué es un archivo SRT? ##

SRT (formato de archivo SubRip) es un archivo de subtítulos simple guardado en el formato de archivo SubRip con la extensión .srt. Contiene un número secuencial de subtítulos, marcas de tiempo de inicio y finalización y texto de subtítulos. Los archivos SRT permiten agregar subtítulos al contenido de video después de que se produce.

## Estructura del archivo SRT ##

Cada subtítulo tiene cuatro partes en el archivo SRT.

1. Un contador numérico que indica el número o la posición del subtítulo.
1. Hora de inicio y finalización del subtítulo separadas por --> caracteres
1. Texto del subtítulo en una o más líneas.
1. Una línea en blanco que indica el final del subtítulo.

### Ejemplo de SRT ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Para especificar la hora se utiliza el formato *horas:minutos:segundos,milisegundos (00:00:00,000)*.

## Formateo de archivos SRT ##

El formato de los archivos SRT se deriva de las etiquetas HTML. Las etiquetas de formato para el archivo SRT se enumeran a continuación.

| Efecto | Etiquetas |
| --- | --- |
|Negrita|**\ <b>...\</b> ** o {b}...{/b}|
|Cursiva|**\ <i>...\</i> ** o **{i}...{/i}**|
|Subrayado|**\ <u>...\</u> ** o **{u}...{/u}**|
|Color de fuente|**\ <font color="white">...\</font> **|
|Posición de línea|**{\a3}** (indica que el texto debe comenzar a aparecer en la línea 3)

## Software SubRip ##

SubRip es un programa de software gratuito que se ejecuta en Windows. Extrae subtítulos y sus tiempos de diferentes formatos de video y guarda los subtítulos en formato SRT. SubRip utiliza el reconocimiento óptico de caracteres para extraer subtítulos de video en vivo, otros archivos de video y DVD.

## Referencias ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
