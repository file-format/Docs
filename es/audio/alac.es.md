---
date: 2021-03-21
keywords: alac, formato de archivo alac, extensión .alac
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo ALAC y las API que pueden crear y abrir archivos ALAC."
title: ALAC - Formato de archivo de códec de audio sin pérdidas de Apple
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## ¿Qué es un archivo ALAC?

El formato de archivo ALAC es Apple Lossless Audio Codec (ALAC) que utiliza el contenedor QuickTime compatible con MPEG-4. Se introdujo en 2004 como formato de archivo patentado, hasta 2011 cuando Apple lo puso a disposición de código abierto y libre de regalías. El formato es similar al [FLAC](/es/audio/flac/) (Free Lossless Audio Codec) pero ofrece más compresión comparativamente. Ofrece una mejor alternativa de sonido a [AAC](/es/audio/aac/) o [MP3](/es/audio/mp3/). Los archivos de audio codificados con el códec ALAC se pueden abrir con Apple QuickTime, Apple iTunes y Micrsoft Windows Media Player con el códec K-Lite.

## Formato de archivo ALAC

Los archivos basados en el códec ALAC son archivos binarios que están disponibles como [código abierto en GitHub](https://github.com/macosforge/alac) para referencia del desarrollador. Contiene las fuentes para el codificador y decodificador ALAC. Apple también ha proporcionado una utilidad de línea de comandos, llamada `alacconvert`, para leer y escribir los datos de audio a/desde archivos Core Audio Format (CAF) y [WAVE](/es/audio/wav/). Los siguientes son algunos puntos clave sobre el formato de archivo ALAC.

1. `Profundidad de bits`: 16, 20, 24 y 32 bits.
1. `Frecuencia de muestreo`: cualquier frecuencia de muestreo de números enteros arbitrarios de 1 a 384 000 Hz. Se pueden admitir velocidades teóricas de hasta 4.294.967.295 (2^32 - 1) Hz.
1. `Tamaño del paquete`: el tamaño predeterminado del paquete es de 4096 fotogramas de muestra de audio por paquete. Ciertamente son posibles otros tamaños de paquetes. Sin embargo, no se garantiza que los tamaños de paquetes no predeterminados funcionen correctamente en todos los dispositivos de hardware compatibles con Apple Lossless. No se admiten paquetes con más de 16 384 tramas de muestra.
1. "Canales compatibles": admite de uno a ocho canales. Cada canal tiene el siguiente orden de información.

|Núm Can| Orden|
|---|---|
|1 |mono|
|2 |estéreo (izquierda, derecha)|
|3 |MPEG 3.0 B (Centro, Izquierda, Derecha)|
|4 |MPEG 4.0 B (Centro, Izquierda, Derecha, Centro Surround)|
|5 |MPEG 5.0 D (Centro, Izquierda, Derecha, Surround izquierdo, Surround derecho)|
|6 |MPEG 5.1 D (Centro, Izquierda, Derecha, Surround izquierdo, Surround derecho, Efectos de baja frecuencia)|
|7 |Apple AAC 6.1 (Centro, Izquierda, Derecha, Surround izquierdo, Surround derecho, Surround central, Efectos de baja frecuencia)|
|8 |MPEG 7.1 B (Centro, Centro izquierdo, Centro derecho, Izquierda, Derecha, Surround izquierdo, Surround derecho, Efectos de baja frecuencia)|

## Referencias

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Códec de audio sin pérdidas de Apple](https://macosforge.github.io/alac/)
* [macosforge - alac en GitHub](https://github.com/macosforge/alac)

