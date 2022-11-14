---
date: 2019-12-13
keywords: flac, formato de archivo flac, extensión .flac, archivo flac, flac vs mp3
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo FLAC y las API que pueden crear y abrir archivos FLAC."
title: Formato de archivo FLAC
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## ¿Qué es un archivo FLAC?

FLAC (Free Lossless Audio Codec) es un formato de codificación de audio de compresión sin pérdidas desarrollado por la Fundación Xiph.Org. FLAC es un formato abierto libre de regalías que se guarda con la extensión .flac. El audio digital comprimido con el algoritmo FLAC normalmente se reduce entre un 50 y un 70 por ciento de tamaño. Los archivos FLAC se pueden descomprimir en una copia idéntica de los archivos de audio originales.

## Formato de archivo FLAC

Esta es una descripción general del flujo de bits FLAC.

- **marcador fLaC**: este marcador se agrega al comienzo de la transmisión. Es seguido por uno o más bloques de metadatos.
- **Bloques de metadatos**: FLAC admite 128 tipos de bloques de metadatos; actualmente se definen los siguientes.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **CUADRO**: Los datos de audio se componen de uno o más fotogramas de audio.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Breve historia del formato de archivo FLAC

Josh Coalson comenzó el desarrollo de FLAC en 2000. La primera versión de FLAC se lanzó el 20 de julio de 2001. FLAC se incorporó bajo la marca Xiph.Org el 20 de enero de 2003. El desarrollo de FLAC se trasladó al repositorio Xiph.Org git con el lanzamiento de la versión 1.3.0 el 26 de marzo de 2013.

## Composición del Proyecto FLAC

El proyecto FLAC consiste en lo siguiente:

- Formatos de transmisión.
- Formato de contenedor simple para la transmisión (FLAC).
- libFLAC: una biblioteca de codificadores, decodificadores e interfaz de metadatos de referencia.
- libFLAC++: un contenedor orientado a objetos para libFLAC.
- flac: un programa de línea de comandos para codificar y decodificar transmisiones FLAC.
- metaflac: un editor de metadatos de línea de comandos para FLAC.
- Complementos de entrada para reproductores de música como Winamp, XMMX, etc.
- Formato contenedor Ogg (Ogg FLAC).

## Diseño FLAC

Dependiendo de la densidad y amplitud de la música, el tamaño del archivo comprimido puede ser un 80% menor que el del archivo original.

### Codificador de origen ###

- Solo admite muestras enteras y no de punto flotante. Puede manejar una resolución de bits PCM de 4 a 32 bits por muestra y una frecuencia de muestreo de 1 Hz a 65 535 Hz. La codificación FLAC está limitada a 24 bits por muestra.
- Los canales se pueden agrupar para aprovechar las correlaciones entre canales para aumentar la compresión.
- Las sumas de comprobación CRC se utilizan para identificar tramas corruptas.
- Para la conversión de muestras de audio, FLAC utiliza predicción lineal.

### Metadatos ###

- FLAC es compatible con ReplayGain (utilizado para percibir y normalizar el volumen del audio).
- FLAC utiliza el mismo sistema utilizado en los comentarios de Vorbis para el etiquetado.
- La mayoría de las aplicaciones FLAC utilizan libFLAC para codificar/descodificar.
- La API libFLAC está organizada en flujos, flujos buscables y archivos para aumentar la abstracción del flujo de bits FLAC base.

### Compresión ###

libFLAC usa niveles de compresión de 0 a 8, donde 0 es el nivel de compresión más rápido y 8 es el más lento. Los archivos comprimidos siempre son sin pérdidas, aunque la compensación es entre velocidad y tamaño.

## FLAC frente a MP3
El MP3 es un formato de compresión con pérdida, lo que significa que puede cortar una parte del audio para reducir su tamaño después de aplicar la compresión. Mientras que FLAC es un formato de archivo sin pérdidas, lo que significa que puede escuchar el audio en su forma más pura. Anteriormente, los formatos de archivo sin pérdidas eran CDA o WAV, que no ocupaban mucho espacio como FLAC. La siguiente tabla mostrará la comparación entre estos dos formatos para algunos términos importantes:

|Término|FLAC|MP3|
---|---|---|
|**Calidad de datos**|Sin pérdida de datos de audio| Es posible que se pierdan algunos datos al comprimir datos de audio|
|**Tamaño**|Tamaño de archivo más grande en comparación con los formatos con pérdida. Así que necesita una mayor capacidad de almacenamiento | Tamaño de archivo más pequeño, adecuado para reproducir en dispositivos de audio compactos con poco espacio de almacenamiento |
|**Requisitos de hardware**| Necesita equipos de audio de alta calidad y gran capacidad de almacenamiento | Se pueden guardar enormes bibliotecas de audio en un espacio de almacenamiento más pequeño. Adecuado para dispositivos portátiles, como reproductores de audio o teléfonos móviles|
|**Distribución a través de Internet**|No se puede distribuir fácilmente a través de Internet debido al enorme tamaño de archivo |El tamaño de archivo compacto facilita la distribución a través de Internet|
|**Compatibilidad**|El códec para escuchar música y audio más popular que es prácticamente compatible con todos los dispositivos del planeta. Compatible con PC, teléfonos, receptores AV, reproductores de Blu-ray, dispositivos de transmisión como Roku o Fire TV de nueva generación.

## Referencias ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

