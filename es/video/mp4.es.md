---
date: 2019-10-11
keywords: MP4, archivo, extensión, formato, formato de video, MPEG-4
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo MP4 y las API que pueden crear y abrir archivos MP4."
title: Formato de archivo MP4
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## ¿Qué es un archivo MP4? ##

MP4 (abreviatura de MPEG-4 Parte 14) es un formato de archivo basado en ISO/IEC 14496-12:2004 que se basa en el formato de archivo QuickTime pero especifica formalmente la compatibilidad con los descriptores de objetos iniciales (IOD) y otras funciones de MPEG. Se usa principalmente para almacenar video y audio, pero también se puede usar para almacenar subtítulos e imágenes fijas. Los archivos MP4 se almacenan con la extensión .mp4. MP4 es un estándar internacional de codificación audiovisual. Al igual que la mayoría de los formatos de contenedores modernos, MP4 admite la transmisión por Internet. Debido a la alta compresión utilizada en MP4, los archivos resultantes son más pequeños y conservan casi toda la calidad original.

## Breve historia ##

La especificación MP4 fue desarrollada por Moving Picture Experts Group (MPEG) y se basó en el formato QuickTime [MOV](/es/video/mov/) que se publicó en 2001. La primera versión (ISO/IEC 14496-1:2001) de MP4 fue una revisión de MPEG-4 Parte 1: Especificación de sistemas publicada en 1999. El formato de archivo MP4 se generalizó a ISO Base Media File Format ISO/IEC 14496-12:2004 que definió la estructura general para archivos multimedia basados en tiempo. Como resultado, se utiliza como base para otros formatos de archivo.

## Estructura de archivos MP4 ##

MP4 es un archivo contenedor extensible, lo que significa que no define una estructura estricta y permite una estructura y jerarquía personalizadas para cada tipo de medio. Los datos del archivo MP4 se dividen en dos secciones, la primera que contiene los datos relacionados con los medios y la segunda que contiene los metadatos. Los datos multimedia contienen audio o video y los metadatos indican indicadores para acceso aleatorio, marcas de tiempo, etc.
Las estructuras en MP4 generalmente se denominan átomos o cajas. El tamaño mínimo de un átomo es de 8 bytes (los primeros 4 bytes especifican el tamaño y los siguientes 4 bytes especifican el tipo). Aquí hay una lista de los átomos de nivel raíz contenidos en los archivos MP:

- **ftyp**: contiene el tipo de archivo, la descripción y las estructuras de datos comunes utilizadas.
- **pdin**: Contiene información de carga/descarga progresiva de video.
- **moov**: Contenedor para todos los metadatos de la película.
- **moof**: Contenedor con fragmentos de video.
- **mfra**: El contenedor con acceso aleatorio al fragmento de video
- **mdat**: Contenedor de datos para medios.
- **stts**: tabla muestra-tiempo.
- **stsc**: tabla sample-to-chunk.
- **stsz**: tamaños de muestra (encuadre)
- **meta**: El contenedor con la información de los metadatos.

Aquí hay una lista de átomos de segundo nivel utilizados en MP4:

- **mvhd**: contiene la información del encabezado del video con todos los detalles del video.
- **trak**: Contenedor con la pista individual.
- **udta**: El contenedor con la información del usuario y del track.
- **iods**: descriptor de archivo MP4

## Referencias ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

