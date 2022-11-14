---
date: 2019-10-11
keywords: rm, .rm, formato de archivo rm, formato de archivo .rm, extensión .rm, formato de archivo RealMedia
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo RM y las API que pueden crear y abrir archivos RM."
title: Formato de archivo RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## ¿Qué es un archivo RM? ##

RealMedia es un formato de contenedor multimedia propietario desarrollado por RealNetworks que utiliza la extensión .rm. Se utiliza con la combinación de [RealAudio (RA)](/es/audio/ra/) y [RealVideo(RV)](/es/video/rv/) para la transmisión por Internet. Estos flujos tienen una tasa de bits constante. Para la tasa de bits variable, RealNetworks desarrolló el formato RealMedia Variable Bitrate (RMVB). RealMedia es adecuado para transmitir contenido a través de Internet y se puede utilizar para transmitir televisión en vivo, por ejemplo.

## Estructura del archivo RealMedia ##

Un archivo RealMedia consta de una serie de fragmentos, cada uno con la siguiente estructura:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Los siguientes son los tipos de fragmentos presentes en el archivo RealMedia:

- **Encabezado de archivo RealMedia (.RMF)**: debe ser el primer fragmento del archivo RealMedia. Solo un fragmento RMF está presente en un archivo. Contiene información sobre el número de encabezados.
- **Encabezado de propiedades del archivo (PROP)**: contiene información sobre las propiedades generales del archivo RealMedia. Solo hay un fragmento de este tipo en cada archivo de RealMedia.
- **Encabezado de propiedades de medios (MDPR)**: este fragmento contiene información sobre las propiedades de la transmisión. Contiene información sobre el tipo de transmisión y el códec utilizado. Hay un fragmento MDPR para cada secuencia en el archivo.
- **Encabezado de descripción del contenido (CONT)**: este fragmento contiene información de texto como el título o el autor del contenido del archivo RealMedia. Este fragmento es solo para fines informativos.
- **Encabezado de datos (DATA)**: este fragmento contiene un grupo de paquetes de datos.
- **Encabezado de índice (INDX)**: este fragmento viene después de todos los fragmentos de DATOS y contiene entradas de índice. Un archivo puede tener más de un fragmento INDX.

## Formatos de audio y video compatibles ##

### Formatos de audio ###

-lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- red: AC3
- sorbo: sipro
- cocinar: cocinar
- atrc: ATRAC3
- ralf: formato sin pérdida de RealAudio
- Raac: LC-AAC
- racp: HE-AAC

### Formatos de vídeo ###

-CLV1: ClearVideo
-RV10: H.263
-RV13: H.263
-RV20: H.263+, RV20
- RV30: precursor de H.264
- RV40: precursor de H.264, RV40
-RVTR: H.263+ (RV20)

## Referencias ##

- [RealMedia-Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

