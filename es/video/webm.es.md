---
date: 2019-10-11
keywords: WEBM, ¿Qué es un archivo WEBM? Formato de archivo WEBM
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo WEBM y las API que pueden crear y abrir archivos WEBM."
title: WEBM - Formato de archivo de vídeo WebM
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## ¿Qué es un archivo WEBM?

Un archivo con una extensión .webm es un archivo de video basado en el formato de archivo WebM abierto y libre de regalías. Ha sido diseñado para compartir videos en la web y define la estructura del contenedor de archivos, incluidos los formatos de video y audio. WebM es 100 % gratuito e implementa alta calidad basada en tecnologías abiertas como HTML, HTTP y TCP/IP que están abiertas a cualquiera para su implementación. WebM ha sido diseñado específicamente para servir video en la web, lo que lo optimiza para la transmisión con una huella computacional baja. Esto lo hace adecuado para la reproducción de videos en cualquier dispositivo, especialmente netbooks, dispositivos portátiles y tabletas de bajo consumo.

## Formato de archivo WEBM

La estructura de archivos WebM se basa en un subconjunto del formato de archivo contenedor Matroska [MKV](/es/video/mkv/). Los flujos de video disponibles en un archivo WebM se comprimen utilizando las tecnologías de compresión VP8 o VP9 que son altamente eficientes en la compresión. De manera similar, las transmisiones de audio en un archivo WebM se comprimen utilizando los códecs Vorbis u Opus que fueron desarrollados por [Xiph Foundation](https://www.xiph.org/). Todos estos videos y códecs de audio están libres de regalías y se pueden usar sin cargo.

Las siguientes son las especificaciones resumidas para el formato de archivo WebM.

|Campo|Descripción|
---|---|
|tipo MIME |video/webm|
|Solo audio tipo MIME |audio/webm|
|Identificador de tipo uniforme| org.proyectowebm.webm|
|Nombre del códec de vídeo| VP8 o VP9|
|Nombre del códec de audio| Vorbis u Opus|

### Elementos WebM

WebM, al ser un subconjunto de las especificaciones de Matroska, brinda soporte para algunas de las funciones de Matroska. A continuación, se incluye una descripción de los elementos admitidos.

#### EBML

|Nombre |Descripción|
---|---|
|EBML|Establecer las características EBML de los datos a seguir. Cada documento EBML tiene que comenzar con esto.|
|EBMLVersion |La versión del analizador EBML utilizada para crear el archivo.|
|EBMLReadVersion|La versión mínima de EBML que debe admitir un analizador para leer este archivo.|
|EBMLMaxIDLength |La longitud máxima de los ID que encontrará en este archivo (4 o menos en Matroska).|
|EBMLMaxSizeLength|La longitud máxima de los tamaños que encontrará en este archivo (8 o menos en Matroska). Esto no anula el tamaño del elemento indicado al principio de un elemento. Los elementos que tengan un tamaño indicado mayor al permitido por EBMLMaxSizeLength se considerarán no válidos.|
|DocType|Una cadena que describe el tipo de documento que sigue a este encabezado EBML ("webm" en nuestro caso).|
|DocTypeVersion|La versión del intérprete de DocType utilizada para crear el archivo.|
|DocTypeReadVersion|La versión mínima de DocType que un intérprete debe admitir para leer este archivo.|

#### Elementos globales

Por el momento, solo se admite el elemento `Void` que se utiliza para anular datos dañados, para evitar comportamientos inesperados al usar datos dañados. El contenido se descarta. También se utiliza para reservar espacio en un subelemento para su uso posterior.

#### Segmento
Este elemento contiene todos los demás elementos de nivel superior (nivel 1). Normalmente, un archivo Matroska se compone de 1 segmento.

#### Información de búsqueda meta

Se admite la siguiente búsqueda de información.

|Nombre del elemento |Descripción|
---|---|
|SeekHead |Contiene la posición de otro elemento de nivel 1.|
|Seek |Contiene una única entrada de búsqueda para un elemento EBML.|
|SeekID |El ID binario correspondiente al nombre del elemento.|
|SeekPosition |La posición del elemento en el segmento en octetos (0 = elemento de primer nivel 1).|

## Referencias

* [WebM](https://www.webmproject.org/)
* [Repositorios de código WebM](https://www.webmproject.org/code/#webp-repositories)

