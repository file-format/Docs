---
date: 2019-12-09
keywords: arj, .arj, formato de archivo arj, cómo abrir archivos arj, extensión .arj, extensión arj
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo ARJ
linktitle: ARJ
description: "Obtenga información sobre el formato de archivo ARJ y las API que pueden crear y abrir archivos ARJ."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## ¿Qué es un archivo ARJ? ##

ARJ (Archivado por Robert Jung) es un archivo comprimido de alta eficiencia desarrollado por Robert K. Jung. ARJ se desarrolló para DOS y las primeras versiones de Windows a principios de la década de 1990. Los archivos ARJ son útiles para realizar copias de seguridad o compartir una gran cantidad de archivos, ya que no tiene que realizar un seguimiento de todos esos archivos y solo hay un archivo para manejar. La extensión .arj se utiliza para los archivos de almacenamiento ARJ.

## Formato de archivo ARJ ##

Un archivo ARJ contiene dos tipos de encabezados:

- Encabezado principal: hay un encabezado principal al comienzo del archivo.
- Encabezados locales: los encabezados locales están presentes antes de cada archivo.

|Compensación|Tipo|Recuento|Descripción|
|---|---|---|---|
|0000h|palabra|1|ID=0EA60h|
|0002h|palabra|1|tamaño básico del encabezado|
|0004h|byte|1|Tamaño del encabezado|
|0005h|byte|1|Número de versión del archivador|
|0006h|byte|1|Número mínimo de versión necesario|
|0007h|byte|1|SO host:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMIGOS</br> 4 - MAC-OS (Sistema xx)</br> 5 - OS/2</br> 6 - MANZANA GS</br> 7 - CALLE ATARI</br> 8 - SIGUIENTE</br> 9 - VAX VMS|
|0008h|byte|1|Banderas internas, mapa de bits:</br> 0 - sin contraseña / contraseña</br> 1 - reservado</br> 2 - el archivo continúa en el siguiente disco</br> 3 - el campo de posición de inicio del archivo está disponible</br> 4 - traducción de ruta ( "\" a "/" )|
|0009h|byte|1|Método de compresión:</br> 0 - almacenado</br> 1 - más comprimido</br> 2 - comprimido</br> 3 - comprimido más rápido</br> 4 - comprimido más rápido|
|000Ah|byte|1|Tipo de archivo:</br> 0 - binario</br> 1 - texto de 7 bits</br> 2 - encabezado de comentario</br> 3 - directorio</br> 4 - etiqueta de volumen|
|000Bh|byte|1|reservado|
|000Ch|dword|1|Fecha/Hora del archivo original en formato MS-DOS|
|0010h|dword|1|Tamaño del archivo comprimido|
|0014h|dword|1|Tamaño del archivo original"|
|0018h|dword|1|CRC-32 del archivo original|
|001Ah|palabra|1|Posición de especificación de archivo en nombre de archivo|
|001Ch|palabra|1|Atributos de archivo|
|001Eh|palabra|1|Datos de host|
|?|dword|1|Posición de inicio del archivo extendido|
|??????h|dword|1|CRC-32 del encabezado básico|
|??????h|palabra|1|Tamaño del primer encabezado extendido|
|??????h+"SIZ"+2|dword|1|CRC-32 del encabezado extendido|
|??????h+"SIZ"+6|byte|?|Archivo comprimido|

## Referencias ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

