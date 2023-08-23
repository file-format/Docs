---
date: 2020-08-12
keywords: jfif, .jfif, formato de archivo jfif, cómo abrir archivos jfif, extensión .jfif, extensión jfif
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Archivo JFIF - ¿Qué es un archivo .jfif?
linktitle: JFIF
description: "Obtenga información sobre el formato de archivo JFIF y las API que pueden crear y abrir archivos JFIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## ¿Qué es un archivo JFIF?

JFIF (JPEG File Interchange Format (JFIF)) es un archivo de formato de imagen que utiliza la extensión .jfif. JFIF se basa en JIF (formato de intercambio JPEG) reduciendo la complejidad y resolviendo sus limitaciones.

## Breve historia de JFIF

El desarrollo del documento JFIF estuvo a cargo de Eric Hamilton y se estableció un acuerdo sobre la primera versión a fines de 1991. La versión 1.02 se publicó el 7 de septiembre de 1992. RFC 2046 especificó que el formato JFIF se usa para transmitir imágenes JPEG a través de Internet. JFIF fue publicado por ECMA en 2009 y fue estandarizado por ITU-T en 2011 como su Recomendación T.871 y por ISO/IEC en 2013 como ISO/IEC 10918-5

## Formato de archivo JFIF ##

Un archivo JFIF consiste en una secuencia de marcadores como se define en la parte 1 del estándar JPEG. Cada marcador consta de dos bytes (FF seguido de un byte que especifica el tipo de marcador). Los marcadores pueden ser independientes o indicar el inicio de un segmento de marcador.

JFIF permite que múltiples componentes como Y, Cb, Cr, tengan diferentes resoluciones pero su alineación no está definida. A diferencia de JPEG, JFIF puede proporcionar información sobre la resolución y la relación de aspecto. JFIF también define el modelo de color a utilizar.

### Estructura del archivo ##

|Segmento|Código|Descripción|
|---|---|---|
|SOI|FF D8|Inicio de imagen|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|segmentos marcadores adicionales|
|SOS|FF DA|Inicio de escaneo|
||datos de imagen comprimidos||
|EOI|FF D9|Fin de la imagen|

El estándar JFIF define los siguientes segmentos:

### Segmento marcador JFIF APP0 ###

Es un segmento obligatorio que contiene parámetros de imagen. También puede contener una miniatura incrustada sin comprimir.

|Campo|Tamaño (bytes)|Descripción|
|---|---|---|
|APP0 marcador|2|FF E0|
|Longitud|2|Longitud del segmento excluyendo el marcador APP0|
|Identificador|5|JFIF (4A 46 49 46 00) en ASCII terminado por un byte nulo|
|Versión de JFIF|2|Versión de JFIF|
|Unidades de densidad|1|Unidad para los siguientes campos de densidad de píxeles</br> 00 : Sin unidades; la relación de aspecto de píxel ancho:alto es igual a Ydensity:Xdensity</br> 01: Píxeles por pulgada</br> 02 : Píxeles por centímetro|
|Xdensity|2|Densidad de píxeles horizontales mayor que cero|
|Ydensity|2|Densidad de píxeles verticales mayor que cero|
|Xthumbnail|1|Recuento de píxeles horizontales de la miniatura RGB incrustada. Puede ser cero|
|Ythumbnail|1|Recuento de píxeles verticales de la miniatura RGB incrustada. Puede ser cero|
|Datos de miniaturas|3 × n|Datos de miniaturas de ráster RGB de 24 bits sin comprimir|

### Extensión JFIF APP0 segmento marcador ###

Esta es una sección opcional que, si se define, debe seguir inmediatamente al segmento marcador JFIF APP0. Esta sección es compatible con JFIF versión 1.02 y superior y permite incrustar miniaturas en tres formatos diferentes.

|Campo|Tamaño (bytes)|Descripción|
|---|---|---|
|APP0 marcador|2|FF E0|
|Longitud|2|Longitud del segmento excluyendo el marcador APP0|
|Identificador|5|JFXX (4A 46 58 58 00) en ASCII terminado por un byte nulo|
|Formato de miniatura|1|Especifica qué formato de datos se utiliza para la siguiente miniatura incrustada:</br> 10: formato JPEG</br> 11: formato paletizado de 1 byte por píxel</br> 13: formato RGB de 3 bytes por píxel|
|Datos en miniatura|variable||

## Conversión de JFIF a otros formatos de archivo de imagen

JFIF se puede convertir a formatos de archivo de imagen populares como [PNG](/es/image/png/), [JPG](/es/image/jpeg/) y [PDF](/es/pdf/).

## Referencias ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#Historia)

