---
date: 2019-10-11
keywords: vob, .vob, formato de archivo vob, formato de archivo .vob, extensión .vob, extensión vob, formato de video vob, archivos de DVD vob
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo VOB y las API que pueden crear y abrir archivos VOB."
title: Formato de archivo VOB
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## ¿Qué es un archivo VOB? ##

Los archivos VOB se almacenan normalmente en el directorio VIDEO_TS en un DVD con una extensión .vob. Los archivos VOB contienen datos de video y audio, así como otros datos como menús y subtítulos. VOB se basa en el formato de transmisión de programas MPEG-2, pero tiene limitaciones y especificaciones adicionales en transmisiones privadas. Los archivos VOB son un subconjunto estricto de flujos de programas MPEG, por lo que todos los archivos VOB son flujos de programas MPEG, pero todos los flujos de programas MPEG no son compatibles con VOB.

## Estructura de DVD Video ##

Cuando se abre un DVD en una computadora, VIDEO_TS es el directorio de nivel superior con AUDIO_TS. AUDIO_TS está vacío y no se utiliza. Dentro del directorio VIDEO_TS, hay archivos VOB, BUP e IFO. Los archivos VOB contienen el contenido MPEG. Estos se dividen en fragmentos de 1 GB o menos para que sean compatibles con todos los sistemas operativos. Los archivos IFO contienen información sobre los menús y la estructura del título. Los archivos BUK son archivos de respaldo de los archivos IFO con el mismo nombre. Estos archivos están destinados a mantenerse en un área separada físicamente para que, en caso de que el archivo IFO se dañe debido a daños físicos en el DVD, el archivo BUK pueda proporcionar la misma información.

### Disposición física ###

- Todos los archivos en el disco deben ser contiguos.
- Los archivos relacionados deben estar uno al lado del otro (VOB, IFO, BUP).
- Los archivos numerados deben estar en orden ascendente.

## Protección de copia ##

Muchos DVD de video están encriptados e impiden la copia de datos del DVD. Se necesitan claves de autenticación y descifrado para reproducir los archivos que se encuentran en el área de entrada inaccesible del DVD. Estas claves son utilizadas por el software de descifrado de CSS que está presente en el reproductor de DVD o en el reproductor de software. Sin las claves, los archivos de video no se pueden reproducir, ya que se solicitarán las claves cuando se abran los archivos.

## Referencias ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Dentro de DVD-Video/Estructura de directorio](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

