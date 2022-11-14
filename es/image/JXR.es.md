---
date: 2020-08-12
keywords: jxr, .jxr, formato de archivo jxr, cómo abrir archivos jxr, extensión .jxr, extensión jxr
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo JXR
linktitle: JXR
description: "Obtenga información sobre el formato de archivo JXR y las API que pueden crear y abrir archivos JXR."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## ¿Qué es un archivo JXR? ##

JPEG XR (rango extendido de JPEG) es un formato de archivo para imágenes fotográficas de tonos continuos. Es un estándar de compresión de imágenes fijas basado en HD Photo desarrollado por Microsoft. Admite compresión con pérdida y sin pérdida.

## Breve historia ##

Windows Media Photo fue anunciado por primera vez por Microsoft en WinHEC 2006. Pasó a llamarse HD Photo en noviembre de 2006. JPEG XR fue aprobado como estándar internacional ISO/IEC 29199-2 el 19 de junio de 2009. ITU-T e ISO/IEC publicaron una moción especificación de formato (ITU-T T.833 | ISO/IEC 29199-3), un conjunto de prueba de conformidad (ITU-T T.834 | ISO/IEC 29199-4) y software de referencia (ITU-T T.835 | ISO /IEC 29199-5) para JPEG XR después de completar la especificación de codificación de imágenes en 2010. En 2011 se publicó un informe técnico que describe la arquitectura de flujo de trabajo para JPEG XR.

## Diseño JPEG XR ##

En comparación con JPEG, JPEG XR ofrece varias mejoras, entre ellas:

- **Mejor compresión**: JPEG XR ofrece relaciones de compresión más altas.
- **Compresión sin pérdida**: JPEG XR admite compresión sin pérdida.
- **Estructura de mosaico**: la imagen JPEG XR se puede segmentar en regiones de mosaico donde cada región se puede decodificar por separado.
- **Más precisión de color**: JPEG XR incluye conversión interna al espacio de color YCoCg para admitir imágenes que usan el espacio de color RGB. JPEG XR también admite un modelo de color CMYK entero de 16 bits por componente (64 bits por píxel). JPEG XR admite el formato de color de punto flotante de exponente compartido RGBE para imágenes HDR. JPEG XR también admite codificaciones de color en escala de grises y multicanal.
- **Mapa de transparencia**: JPEG XR admite el canal alfa para la transparencia.
- **Modificación de imágenes de dominio comprimido**: las imágenes JPEG XR se pueden convertir a codificación con pérdida, reducir su resolución, recortarlas, voltearlas, rotarlas y la estructura de mosaicos se puede modificar, todo sin decodificar completamente el archivo.
- **Soporte de metadatos**: el archivo de imagen JPEG XR puede contener un perfil de color ICC para una representación de color uniforme en varios dispositivos. El formato también es compatible con los formatos de metadatos Exif y XMP.

## Formato de contenedor ##

Los datos de imagen JPEG XR se pueden almacenar en formato de contenedor similar a TIFF mediante el uso de una tabla de etiquetas de directorio de archivos de imagen (IFT). Un archivo JXR contiene lo siguiente en etiquetas IFD:

- Datos de imagen: Es un dato de imagen autónomo contiguo.
- Datos de canal alfa opcionales: si está presente, los datos de la imagen se pueden comprimir por separado, lo que permite la compatibilidad con aplicaciones que no admiten transparencia.
- Metadatos
- Metadatos XMP opcionales
- Metadatos Exif opcionales

Como se basa en el formato TIFF, hereda todas las limitaciones del formato TIFF, como el límite de tamaño de archivo de 4 GB.

## Referencias ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

