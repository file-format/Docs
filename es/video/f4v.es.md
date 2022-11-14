---
date: 2019-10-11
keywords: f4v, .f4v, formato de archivo f4v, formato de archivo .f4v, extensión .f4v, extensión f4v, formato de video f4v, cómo abrir archivos f4v, qué son los archivos f4v
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo F4V y las API que pueden crear y abrir archivos F4V"
title: Formato de archivo F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## ¿Qué es un archivo F4V? ##

F4V (Flash MP4 Video File) es un archivo de video guardado con la extensión .f4v. Se basa en el formato de archivo de medios base ISO (MPEG-4 Parte 12). Es muy similar a [MP4](/es/video/mp4/), por lo que también se le conoce informalmente como Flash MP4. [FLV](/es/video/flv/) tenía limitaciones al transmitir contenido H.264/ACC, lo que resultó en que Adobe Systems creara el nuevo formato F4V. Flash Player puede reproducir archivos F4V desde el lanzamiento de Flash Player 9 Update 3.

## Estructura de los archivos F4V ##

El formato de archivo F4V se basa en el formato de archivo multimedia base ISO (MPEG-4 Parte 12) y es muy similar al formato MP4. Para obtener detalles sobre la estructura, consulte la página [MP4](/es/video/mp4/). La principal diferencia entre F4V y MP4 son los formatos de metadatos que F4V puede almacenar. A continuación se muestra la lista de los formatos de metadatos admitidos por el formato F4V.

- **Cuadro de etiquetas**: Cuatro cuadros de etiquetas opcionales adicionales (auth, title, dscp, cprt) dentro del cuadro Película (moov).
- **Cuadro de metadatos XMP**: este cuadro se encuentra justo después del cuadro Película (moov). Con esto, el archivo puede comunicar metadatos XMP a una película SWF a través de ActionScript.
- **cuadro ilst**: este cuadro se encuentra dentro del cuadro Meta (meta) y puede contener varias etiquetas de metadatos. Los tipos de datos admitidos se indican a continuación.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Cuadro de metadatos de pista de texto**: las muestras de texto (texto o tx3g) dentro del cuadro de datos multimedia (mdat). Puede contener los siguientes cuadros de metadatos.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Referencias ##

- [Video Flash - Wikipedia] (https://en.wikipedia.org/wiki/Flash_Video)

