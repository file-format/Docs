---
date: 2019-12-13
keywords: m3u, formato de archivo m3u, extensión .m3u, lista de reproducción multimedia m3u, formato de lista de reproducción m3u
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo M3U y las API que pueden crear y abrir archivos M3U."
title: Formato de archivo M3U
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## ¿Qué es un archivo M3U? ##

M3U (URL MP3) es un archivo de lista de reproducción de audio almacenado con la extensión .m3u. M3U no es un archivo de audio real, solo apunta a archivos de audio y, a veces, de video. M3U fue desarrollado para ser utilizado con el software Winplay3 por Fraunhofer. También es compatible con varios reproductores multimedia y software.

## Formato de archivo M3U

No existe una especificación oficial para el formato de archivo M3U, es un estándar de facto. M3U es un archivo de texto sin formato que usa la extensión .m3u si el texto está codificado en la codificación no Unicode predeterminada del sistema local o con la extensión .m3u8 si el texto está codificado en UTF-8. Cada entrada en el archivo M3U puede ser una de las siguientes:

- Ruta absoluta al archivo
- Ruta del archivo relativa al archivo M3U.
- URL

### M3U extendido ###

En el M3U extendido, se introducen directivas adicionales que comienzan con "#" y terminan con dos puntos (:) si tienen parámetros. A continuación se muestra una lista de directivas para M3U extendido.

- **#EXTM3U** - Es el encabezado del archivo que indica M3U extendido y debe ser la primera línea del archivo.
- **#EXTENC:** - Codificación de texto. Debe ser la segunda línea del archivo.
- **#EXTINF:** - Se utiliza para información de seguimiento y otras propiedades adicionales.
- **#PLAYLIST:** - El título de la lista de reproducción
- **#EXTGRP:** - Comenzar la agrupación de nombres
- **#EXTALB:** - Información del álbum
- **#EXTART:** - Artista del álbum
- **#EXTGENRE** - Género del álbum
- **#EXTM3A** - Lista de reproducción de un solo archivo para pistas o capítulos de álbumes.
- **#EXTBYT:** - Tamaño del archivo en bytes.
- **#EXTBIN:** - Siguen los datos binarios.
- **#EXTIMG:** - Logo, Portada u otras imágenes.

### HLS M3U ###

Apple creó HLS (HTTP Live Streaming) para transmitir audio y radio a dispositivos iOS. Se basa en el M3U extendido codificado en UTF-8. Fue estandarizado como RFC 8216 en 2017 por IETF. Las etiquetas de la lista de reproducción HLS comienzan con "#EXT-X-". A continuación se muestra una lista de etiquetas para HLS

- **EXT-X-VERSION**: indica la versión de compatibilidad del archivo según el medio y su servidor.
- **#EXT-X-START:** - Indica el punto de inicio preferido para la lista de reproducción.
- **#EXT-X-PLAYLIST-TYPE:** - Proporciona el tipo de lista de reproducción (EVENTO o VOD).
- **#EXT-X-TARGETDURATION:** - Especifica la duración máxima del Segmento.
- **#EXT-X-MEDIA-SEQUENCE:** - Indica el Número de Secuencia del Medio.
- **#EXT-X-INDEPENDENT-SEGMENTS**: indica que todas las muestras de medios son independientes y se pueden decodificar sin otros segmentos.
- **#EXT-X-MEDIA:** - Se utiliza para relacionar Media Playlists que contienen Versiones alternativas del mismo contenido.
- **#EXT-X-STREAM-INF:** - Especifica un Flujo Variante que forma parte de las Representaciones.
- **#EXT-X-BYTERANGE:** - Indica que el segmento de medios es un subrango del recurso identificado por su URI.
- **#EXT-X-DISCONTINUITY**: indica discontinuidad entre los segmentos de medios anteriores y posteriores.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Permite la sincronización entre diferentes versiones del mismo Variant Stream o Variant Streams diferentes.
- **#EXT-X-KEY:** - Especifica cómo descifrar segmentos de medios.
- **#EXT-X-MAP:** - Especifica cómo obtener la sección de inicialización de medios. Es necesario analizar los segmentos de medios aplicables.
- **#EXT-X-PROGRAM-DATE-TIME:** - Asocia la primera muestra del Segmento de Medios a una fecha y/u hora absoluta.
- **#EXT-X-DATERANGE:** - Asocia un Rango de Datos.
- **#EXT-XI-FRAMES-ONLY**: indica que cada segmento de medios en la lista de reproducción describe un solo cuadro I.
- **EXT-XI-FRAME-STREAM-INF** - Indica que el archivo de la lista de reproducción contiene I-frames de presentación Multimedia.
- **#EXT-X-SESSION-DATA:** - Permite que datos de sesión arbitrarios sean
transportado en una lista de reproducción maestra.
- **#EXT-X-SESSION-KEY:** - Permite cifrar claves. El cliente puede precargar estas claves sin leer primero la lista de reproducción.
- **#EXT-X-ENDLIST** - Indica que no se agregarán más segmentos de medios al archivo.

La siguiente es la lista de tipos de medios de Internet utilizados por M3U:

- **application/vnd.apple.mpegurl**: es el único tipo de medio registrado (registrado en 2009) para M3U que se utiliza para hacer referencia a las listas de reproducción en las aplicaciones HLS.
- Los siguientes tipos de medios de Internet son utilizados por aplicaciones que no son HLS.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## Ejemplo M3U ##

Este es un ejemplo del archivo M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Referencias ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [Transmisión en vivo HTTP](https://tools.ietf.org/html/rfc8216)

