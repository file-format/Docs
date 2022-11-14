---
date: 2019-12-09
keywords: arc, .arc, formato de archivo arc, cómo abrir archivos arc, extensión .arc, extensión arc
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo ARC
linktitle: ARC
description: "Obtenga información sobre el formato de archivo ARC y las API que pueden crear y abrir archivos ARC."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## ¿Qué es un archivo ARC?

ARC es un formato de archivo y compresión de datos sin pérdidas desarrollado por System Enhancement Associates (SEA). El formato de archivo y la aplicación que lo crea se denominan ARC. ARC fue muy popular durante los primeros días del BBS de acceso telefónico, ya que combinaba las funciones de compresión y archivado de varios archivos en el mismo archivo. Más tarde, ARC fue reemplazado por [ZIP](/es/compression/zip/) que ofrecía mejores relaciones de compresión.

La extensión de archivo .arc es utilizada por varios otros tipos de archivos de almacenamiento no relacionados, como el formato ARC utilizado por Internet Archive para almacenar múltiples recursos web, un formato ARC diferente utilizado por el archivador FreeArc, un formato diferente utilizado por Nintendo para recursos, etc. .

## Breve historia del formato de archivo ARC

El programa ARC fue escrito por Thom Henderson de System Enhancement Associates en 1985. Este programa agrupaba archivos en un solo archivo y también los comprimía. Los archivos generados por el programa ARC usaban la extensión .arc. SEA lanzó el código fuente de ARC en 1986 y ARC fue portado a Unix y Atari ST por Howard Chu en 1987.

Phil Katz desarrolló PKARC y PKXARC para archivar y extraer archivos. Los archivos funcionaban con el formato de archivo ARC y eran significativamente más rápidos. A diferencia de ARC, Katz dividió las funciones de compresión y archivo entre dos archivos diferentes, lo que redujo el requisito de memoria para ejecutarlos.

Después de la demanda entre SEA y Katz, SEA se retiró del mercado de shareware y desarrolló ARC+Plus con una interfaz de usuario de pantalla completa. El formato ARC ya no es común en PC.

## Formato de archivo ARC

El archivo ARC consta de una secuencia de encabezado de archivo y archivo seguido del marcador de fin de archivo, como se muestra a continuación.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### Encabezado del archivo ARC ###

|Compensación|Etiqueta|Tipo|Valor|Descripción|
|---|---|---|---|---|
|00|ARCIDO |DB|$1A| |
|01|ARCMTD|DB|00|Método|
|02|ARCFNT|DS|12|nombre de archivo|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Tamaño comprimido|
|13|ARCDAT|DW|0000|Fecha de archivo (MSDOS)|
|15|ARCTIM|DW|0000|Tiempo de archivo (MSDOS)|
|17|ARCCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Tamaño sin comprimir|
|1D|ARCFIL|DS|ARCNSZ| |

### Métodos de compresión ###

El byte del método de compresión indica el método de compresión utilizado. Los siguientes son los métodos de compresión utilizados para el archivo ARC.

|Método|Nombre|Descripción|
|---|---|---|
|0|Almacenado|No se usa compresión|
|1|Empaquetado|Codificación de longitud de ejecución repetida (RLE)|
|2|Apretado|Codificación Huffman|
|3|Crunched|LZW con búfer 4K, códigos de 12 bits|
|4|Crunched|Primero empaquetado, luego búfer LZW 4K con 12 bits|
|5|Crunched|Packing, LZW, búfer 4K, longitud variable (9-12 bits)|
|6|Aplastado|LZW, búfer de 8K, longitud variable (9-13 bits)|
|7|Aplastado|Empaquetado, luego búfer LZW 8K, 2-13 bits (PAK 1.0)|
|8|Destilación|Huffman dinámico con búfer de 8K (PAK 2.0)|

## Referencias

- [ARC (formato de archivo) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

