---
date: 2019-10-11
keywords: flv, .flv, formato de archivo flv, formato de archivo .flv, extensión .flv, extensión flv, formato de video flv
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Obtenga información sobre el formato de archivo FLV y las API que pueden crear y abrir archivos FLV."
title: Formato de archivo FLV
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## ¿Qué es un archivo FLV? ##

FLV (Flash Video) es un formato de archivo contenedor con la extensión .flv. FLV se usa para entregar contenido de audio/video a través de Internet usando Adobe Flash Player o Adobe Air. Los datos de los archivos FLV se codifican de la misma forma que los archivos SWF. El soporte directo se agregó a Flash Player 7 en 2003. Adobe Systems creó F4V en 2007 debido a las restricciones de FLV.

### Codificación ###

Los archivos FLV contienen flujos de bits de video de Sorenson Spark, que son una variante patentada del estándar de video H.263. Es el formato de compresión requerido para Flash Player 6 y 7. La versión 8 de Flash Player es compatible con flujos de bits de video On2 TrueMotion VP6. Es el formato de compresión recomendado para Flash Player 8 y superior. FLV admite audio en MP3, Nellymoser Asao Codec y el códec Speex de código abierto. También admite audio sin comprimir o audio en formato ADPCM. AAC (HE-AAC/AAC SBR, AAC Main Profile y AAC-LC) son compatibles con las versiones recientes de Flash Player 9.

## Estructura ##

Los archivos FLV constan de encabezado y paquetes. Un archivo FLV comienza con el encabezado. El encabezado tiene los siguientes campos.

- **Firma**: Su valor es FLV
- **Versión**: Su valor por defecto es 1. Solo es válido 0x01.
- **Banderas**: 0x04 se usa para audio y 0x01 se usa para video, por lo que 0x05 se usa tanto para audio como para video.
- **Tamaño del encabezado**: el valor predeterminado es 9. Se usa para omitir un encabezado expandido más nuevo.

Después del encabezado vienen los Paquetes. El archivo FLV se divide en varios paquetes llamados etiquetas FLV que tienen encabezados de 15 bytes. Los paquetes contienen metadatos para audio, video, guiones, información de encriptación y carga útil. Los paquetes FLV tienen los siguientes campos.

- **Reservado**: Está reservado para FMS y debe ser 0.
- **Filtro**: Indica si los paquetes están filtrados o no.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Tipo de paquete**: Esto define el tipo de contenido en el paquete.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Tamaño de datos**: Indica la longitud del mensaje.
- **Timestamp Lower**: Esto almacena la marca de tiempo en milisegundos en la que se aplican los datos de la etiqueta. Se establece en NULL para el primer paquete.
- **Timestamp Upper**: Extensión para crear un valor uint32_be.
- **ID de transmisión**: se establece en NULL para la primera transmisión.
- **Datos de carga útil**: Estos son los datos basados en el tipo de paquete.

## Referencias ##

- [Video Flash - Wikipedia] (https://en.wikipedia.org/wiki/Flash_Video)

