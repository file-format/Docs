{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "archivo", "extensión", "formato", "formato de archivo de intercambio de audio", "música", "formato de archivo aiff", "aiff a mp3", "aiff vs wav", "convertir aiff a mp3"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo AIFF y las API que pueden crear, convertir y abrir archivos AIFF",
  "title" :"AIFF - Formato de archivo de intercambio de audio",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## ¿Qué es un archivo AIFF?
El AIFF (formato de archivo de intercambio de audio) es un formato de archivo de audio sin comprimir desarrollado por Apple en 1998, pero se basa en **EA IFF 85** (estándar para archivos de formato de intercambio desarrollado por Electronic Arts), un formato contenedor utilizado en los sistemas Amiga. . Este formato de archivo viene con un estándar para almacenar sonidos muestreados. El formato es lo suficientemente bueno en cuanto a flexibilidad y permite el almacenamiento de sonidos muestreados monoaurales o multicanal a varias frecuencias y anchos de muestra. Dado que los archivos AIFF no están comprimidos, esto los hace más grandes que otros formatos con pérdida como [MP3](/audio/mp3/).

Los archivos AIFF constan de 2 canales de audio estéreo sin comprimir con un tamaño de muestra de 16 bits, grabado a 44,1 khz. Debido a la alta calidad del audio, un audio de 5 minutos puede ocupar hasta 50 MB de espacio en disco, que es similar al formato de archivo [WAV](/audio/wav/).

## AIFF frente a WAV

AIFF y WAV son casi iguales en términos de calidad. Ambos usan la misma codificación PCM (modulación de código de pulso), lo que los hace más grandes en comparación con otros formatos con pérdida, como [MP3](/audio/mp3/), [M4A](/audio/m4a/). Algunas de las diferencias generales se escriben en la siguiente tabla:

|AIFF|WAV|
---|---|
|Usado principalmente para MAC|Usado principalmente para PC|
|Permite metadatos| No permite metadatos|

## Estructura del archivo AIFF

**EA IFF 85** establece una estructura general para almacenar datos en archivos. Un archivo **EA IFF 85** consta de varios fragmentos de datos. Un bloque en construcción de un archivo AIFF consta de información de encabezado seguida de datos:
{{< figure src="../chunk.png" alt="Fragmento AIFF" >}}

Un archivo AIFF es una colección de varios tipos diferentes de fragmentos. Hay dos tipos generales de fragmentos que son importantes para formar un fragmento de archivo AIFF:
- **Chunk común**: contiene parámetros importantes que describen el sonido muestreado, como su duración y frecuencia de muestreo.
- **Pieza de datos de sonido**: contiene las muestras de audio reales.
Hay muchos otros fragmentos opcionales que enumeran los parámetros del instrumento, definen marcadores, almacenan información específica de la aplicación, etc.

### Tipos de fragmentos locales

Los tipos de fragmentos para formar AIFF se dan en la siguiente tabla:

|Tipo de fragmento| Descripción|
---|---|
|Common Chunk|Common Chunk describe los parámetros fundamentales del sonido muestreado|
|Pieza de datos de sonido|La pieza de datos de sonido contiene los fotogramas de muestra reales|
|Marker Chunk|El Marker Chunk contiene marcadores que apuntan a posiciones en los datos de sonido|
|Pieza de instrumento|La pieza de instrumento define los parámetros básicos que un instrumento, como un muestreador, podría utilizar para reproducir los datos de sonido|
|Pieza de datos MIDI|La pieza de datos MIDI se puede utilizar para almacenar datos MIDI|
|Pieza de grabación de audio|La pieza de grabación de audio contiene información pertinente a los dispositivos de grabación de audio|
|Chunk específico de la aplicación|Los fabricantes de aplicaciones pueden utilizar el Chunk específico de la aplicación para cualquier fin|
|Chunk de Comentarios|El Chunk de Comentarios se utiliza para almacenar comentarios en el FORMULARIO AIFF|
|Porciones de texto: nombre, autor, derechos de autor, anotación| Todos son fragmentos de texto |

## Referencias ##

* [Formato de archivo de intercambio de audio: por Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

