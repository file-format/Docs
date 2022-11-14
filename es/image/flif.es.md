---
date: 2020-08-12
keywords: flif, .flif, formato de archivo flif, cómo abrir archivos flif, extensión .flif, extensión flif
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo FLIF
linktitle: FLIF
description: "Obtenga información sobre el formato de archivo FLIF y las API que pueden crear y abrir archivos FLIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## ¿Qué es un archivo FLIF? ##

FLIF (Free Lossless Image Format) es un formato de imagen sin pérdidas que utiliza la extensión .flif para sus archivos. FLIF afirma superar a [PNG](/es/image/png/), [WebP](/es/image/webp/) sin pérdidas, BPG sin pérdidas y JPEG 2000 sin pérdidas en términos de relación de compresión. FLIF utiliza entrelazado progresivo, por lo que cualquier descarga parcial de la imagen se puede utilizar como codificación con pérdida para toda la imagen.

## Breve historia ##

FLIF se anunció en septiembre de 2015 y la versión alfa se lanzó en octubre de 2015. En septiembre de 2016, se lanzó la primera versión estable de FLIF.

## Diseño FLIF ##

FLIF utiliza una variante de CABAC (codificación aritmética binaria adaptable al contexto), MANIAC (codificación aritmética de enteros cercanos a cero metaadaptativos) para la compresión. MANIAC es un algoritmo de codificación de entropía desarrollado por Jon Sneyers y Pieter Wuille. En MANIAC, los contextos son nodos de árboles de decisión que se aprenden dinámicamente en el momento de la codificación. Esto hace que el modelo de contexto sea más específico de la imagen y da como resultado una mejor compresión. FLIF tiene las siguientes características:

- Admite compresión sin pérdidas
- Admite compresión con pérdida con preprocesamiento de codificador
- Admite escala de grises, RGB y RGBA
- Soporta profundidad de color de 1 a 16 bits por canal
- Admite archivos entrelazados y no entrelazados
- Admite la decodificación progresiva de archivos descargados parcialmente
- Admite animaciones
- Admite perfiles de color ICC integrados, metadatos Exif y XMP
- Tiene soporte limitado para comprimir archivos RAW de cámara (RGGB)

## Formato de archivo FLIF ##

Un archivo FLIF tiene las siguientes cuatro partes:

## Encabezado principal ##

El encabezado principal contiene los metadatos principales, incluidos el ancho, la altura, la profundidad de color y la cantidad de fotogramas.

|Tipo|Valor|Descripción|
|---|---|---|
|4 bytes|"FLIF"|Magia|
|4 bits|3 = ni todavía; 4 = todavía; 5 = ni anim; 6 = i anim|Entrelazado, animación|
|4 bits|1 = escala de grises; 3 = RGB; 4 = RGBA|Número de canales (nb_channels)|
|1 byte|'0','1','2' ('0'=personalizado)|Bytes por canal (Bpc)|
|variante|ancho-1|Ancho|
|variante|altura-1|Altura|
|varint|nb_frames-2 (solo si es animación)|Número de fotogramas (nb_frames)|

## Fragmentos de metadatos ##

Esta parte contiene metadatos que no son píxeles, como Exif/XMP, perfil de color ICC, etc., que se codifica mediante la compresión DEFLATE. Estos fragmentos se definen de manera similar a los fragmentos PNG, con la diferencia de que el tamaño del plato está codificado con un número variable de bytes. Los nombres de los fragmentos pueden tener 4 letras (4 bytes) o un valor inferior a 32 que indique un fragmento no opcional.

El siguiente es un ejemplo de mandriles opcionales:

|Nombre del fragmento|Descripción|Contenido (después de la descompresión DEFLATE)|
|---|---|---|
|iCCP|perfil de color ICC|datos de perfil de color ICC sin procesar|
|eXif|Metadatos Exif|Encabezado "Exif\0\0" seguido de un encabezado TIFF y los datos EXIF|
|eXmp|Metadatos XMP|XMP contenido dentro de un xpacket de solo lectura sin relleno|

### Convenio de denominación ###

- **Primera letra**: las mayúsculas se usan para fragmentos críticos y las minúsculas para fragmentos no críticos.
- **Segunda letra**: las mayúsculas se usan para públicos y las minúsculas para fragmentos privados
- **Tercera letra**: Las mayúsculas se utilizan para los mandriles que se necesitan para mostrar la imagen correctamente y las minúsculas no son importantes para mostrar la imagen.
- **Cuarta letra**: Las mayúsculas se utilizan para mandriles que se pueden copiar a ciegas de forma segura. Los mandriles en minúsculas dependen de los datos de la imagen.

## Segundo encabezado ##

Este contiene la información sobre la codificación real de los píxeles.

|Tipo|Descripción|Condición|Valor predeterminado|
|---|---|---|---|
|1 byte|byte NUL (0x00), nombre de fragmento de un flujo de bits FLIF16||
|uni_int(1,16)|Bits por píxel de los canales|Bpc == '0': repeat(nb_channels)|8 si Bpc == '1', 16 si Bpc == '2'|
|uni_int(0,1)|Indicador: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Número de bucles|nb_frames > 1||
|uni_int(0,60_000)|Retardo de cuadro en ms|nb_frames > 1: repetir(nb_frames)|
|uni_int(0,1)|Indicador: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|corte|tiene_corte_personalizado_y_alfa|2|
|uni_int(2,128)|divisor alfa|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Indicador: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|variable|Transformaciones (ver abajo)|||
|uni_int(1) = 0|Bit indicador: hecho con transformaciones|||
|uni_int(0,2)|Predictor de píxeles invisibles|alpha_zero && entrelazado && rango alfa incluye cero||

**Canales**

|Número de canal|Descripción|
|---|----|
|0|Rojo o Gris|
|1|Verde|
|2|Azul|
|3|Alfa|

**Transformaciones**

|Tipo|Descripción|
|---|---|
|uni_int(1) = 1|Bit indicador: aún no hecho|
|uni_int(0,13)|Identificador de transformación|
|variable|Datos de transformación (depende de la transformación)|

La transformación se utiliza para modificar los datos de píxeles para una mejor compresión y para realizar un seguimiento de los valores de píxeles que se producen realmente.

## Datos de píxeles ##

Esta parte contiene los datos de píxeles reales codificados mediante la codificación de entropía MANIAC. Los píxeles pueden codificarse usando codificación entrelazada o no entrelazada.

### Método entrelazado ###

En este método, se definen los niveles de zoom. El nivel de zoom 0 se usa para la imagen completa, el nivel de zoom 1 se usa para todas las filas con números pares, el nivel de zoom 2 se usa para todas las columnas con números pares del nivel de zoom 1. En otras palabras, cada nivel de zoom 2k con número par es una versión reducida del imagen, a escala 1:2^k. Los niveles de zoom se codifican de mayor a menor.

### Método no entrelazado ###

En este método, la codificación de los árboles MANIAC comienza inmediatamente seguida por la codificación de los píxeles.

## Referencias ##

- [FLIF - Wikipedia](https://en.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

