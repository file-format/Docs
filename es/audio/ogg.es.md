---
date: 2019-12-13
keywords: ogg, formato de archivo ogg, extensión .ogg, formato de audio ogg
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo OGG y las API que pueden crear y abrir archivos OGG."
title: Archivo OGG - Archivo de audio Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## ¿Qué es un archivo OGG?

OGG es un archivo de audio comprimido Ogg Vorbis que se guarda con la extensión .ogg. Los archivos OGG se utilizan para almacenar datos de audio y también pueden incluir metadatos e información de artistas y pistas. OGG es un formato de contenedor abierto y gratuito mantenido por la Fundación Xiph.Org.

## Breve historia del formato de archivo OGG

El proyecto Ogg comenzó como parte de un proyecto más grande en 1993 y se llamó Squish, pero debido a una marca registrada existente, se le cambió el nombre a OggSquish. Se describió como un intento de crear un formato de audio comprimido flexible para aplicaciones de audio modernas. La referencia OGG se separó de Vorbis el 2 de septiembre de 2000.

OGM se creó en 2002 debido a la falta de soporte de video formal en OGG. Esto permitió incrustar video del marco Microsoft DirectShow en un contenedor basado en OGG. Para 2006, OGG era compatible con muchos motores de videojuegos y se usaba comúnmente para codificar contenido gratuito. La Free Software Foundation inició una campaña el 15 de mayo de 2007 para aumentar el uso de Vorbis como una alternativa superior a MP3. El 30 de junio de 2009, OGG era el único formato de contenedor compatible con la implementación HTML5 de Firefox 3.5.

## Formato de archivo OGG

El formato OGG consta de fragmentos de datos. Cada fragmento se denomina página Ogg. Cada página comienza con "OggS" para identificar el formato Ogg. El encabezado contiene el número de serie y el número de página que identifica cada página como parte de una serie. La página consta de los siguientes componentes.

- **Encabezado de página**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| poco | Valor | Descripción |
| --- | --- | --- |
| 0 | 0x01 | Indica que el primer paquete de la página es la continuación del paquete anterior en el flujo de bits lógico. |
| 1 | 0x02 | Indica que esta página es la primera en el flujo de bits lógico. |
| 2 | 0x04 | Indica que esta página es la última en el flujo de bits lógico. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadatos**: VorbisComment es el mecanismo más compatible para almacenar metadatos. Otros mecanismos incluyen los siguientes:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Referencias ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

