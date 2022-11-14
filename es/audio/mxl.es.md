---
date: 2022-03-20
keywords: mxl, formato de archivo Musepack, extensión .mxl
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo MXL y las API que pueden crear y abrir archivos MXL."
title: Formato de archivo MXL - Archivo MusicXML comprimido
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## ¿Qué es un archivo MXL?

Un archivo MXL es la forma comprimida del formato de archivo MusicXML que es un formato estándar abierto para el intercambio de partituras digitales. Los archivos MusicXML de texto sin formato son de gran tamaño y el uso de dichos archivos como formato de distribución de hojas se vio afectado por el gran tamaño del archivo. Este problema se trató con [MusicXML](https://www.musicxml.com/) 2.0 mediante la introducción del formato de archivo MXL que comprime los archivos lo suficiente como para reducir el tamaño del archivo de forma similar al de los archivos MIDI originales. El tipo de medio recomendado para los archivos MXL es application/vnd.recordare.musicxml.

## Formato de archivo MXL

Los archivos MXL se almacenan como archivos [ZIP](/es/compression/zip/) comprimidos [XML](/es/web/xml/) con la extensión de archivo .mxl. Los archivos MXL se comprimen con el algoritmo DEFLATE como se especifica en [RFC 1951] (https://www.ietf.org/rfc/rfc1951.txt).

### Estructura del archivo MXL

Cada archivo MXL tiene un formato XML basado en ZIP que debe tener un archivo META-INF/container.xml que describe el punto de partida de la versión MusicXML del archivo. No hay un archivo .xsd correspondiente definido para el formato de archivo MXL.

Un archivo container.xml simple tiene el siguiente contenido. Este ejemplo está tomado del archivo Dichterliebe01.mxl disponible en el sitio web de MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
En este ejemplo, el<container> elemento es el elemento del documento. los<rootfiles> elemento puede contener uno o más<rootfile> elementos, con el primero<rootfile> elemento que describe la raíz MusicXML. Un archivo MusicXML utilizado como<rootfile> puede tener<score-partwise> ,<score-timewise> , o<opus> como su elemento de documento.

## Referencias

* [Archivos MXL comprimidos](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951] (https://www.ietf.org/rfc/rfc1951.txt)

