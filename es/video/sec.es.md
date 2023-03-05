---
date: 2022-03-25
keywords: sec, .sec, formato de archivo sec, formato de archivo .sec, extensión .sec, extensión sec
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo SEC y las API que pueden crear y abrir archivos SEC."
title: Formato de archivo SEC - Archivo de video de seguridad de Samsung
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## ¿Qué es un archivo SEC?

Un archivo SEC es un archivo de video que se crea con el sistema de vigilancia Samsung DVR. El video se captura de las cámaras de vigilancia y se almacena en un disco en formato SEC. El video SEC grabado se puede reproducir con el software de video de Samsung que puede administrar la transmisión de video de varias cámaras.

## Formato de archivo SEC - Más información

Los archivos SEC contienen flujo h264/AVC en su interior usando un formato de archivo propietario. El encabezado de un archivo SEC comienza con el número de modelo del SRD-1670D. La información de fecha y hora se encuentra al final del archivo.

### Convertir archivo SEC a AVI

El archivo SEC se puede convertir al formato de archivo estándar [AVI](/es/video/avi/) usando FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Referencias ##

- [Archivos de Samsung y SEC](https://spreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

