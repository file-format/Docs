{
  "date" : "2021-08-16",
  "keywords" :[ "archivo nrg", "formato de archivo nrg", "qué es un archivo nrg", "archivo", "ejemplo nrg", "extensión de archivo nrg","extensión", "formato", "pie de página nrg", "archivo formato de nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo NRG y las API que pueden crear y abrir archivos NRG",
  "title" :"NRG - Formato de archivo de imagen de disco",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## ¿Qué es un archivo NRG?

Un formato de archivo de imagen creado mediante el uso de un disco óptico se considera un formato de archivo NRG. Este formato ha sido creado específicamente por Nero para la utilidad de Nero Burning Rom. Para el almacenamiento de imágenes de disco, se considera que se utiliza este formato ya que es apropiado para estos archivos específicos. Estos archivos pueden tener la forma de una copia exacta de un CD o DVD o pueden tener varios archivos que se pueden montar como un disco. Otros formatos de archivo más populares como [ISO](/es/compression/iso/) son aquellos en los que estos archivos se pueden convertir en algunas utilidades básicas. En su mayoría, los archivos NRG se utilizan para crear copias de seguridad o copias de algunos datos o discos importantes.

## Formato de archivo NRG ##

Este formato de archivo fue desarrollado por Nero AG como un formato de imagen de disco. Tenía la propiedad específica de la utilidad Nero Burning Rom, ya que fue desarrollado para almacenar imágenes de disco. Su primera versión se especificó para almacenar valores como enteros de 32 bits. Sin embargo, se lanzó su segunda versión y contenía soporte para enteros de 64 bits.

## Especificación técnica ##

Al comienzo del archivo, este formato no almacena sus datos como encabezado. Como un pie de página, se adjunta al final del archivo. En forma de fragmentos de IFF, se almacena la información de la imagen. El desplazamiento del primer fragmento se puede obtener leyendo el pie de página de NRG en los últimos 8 bytes a 12 bytes del archivo. En todas las versiones del formato de archivo NRG, hay fragmentos, DAOI, texto de CD, tipo de medio de información de sesión, información de disco, Relo y el final de la cadena adjunto. El orden de los bytes es big-endian y todos los valores enteros no están firmados en el momento del almacenamiento.

### Trozos principales ###

#### Hoja de referencia ####

Esta hoja de referencia está disponible fácilmente en todas las versiones de formato de archivos NRG. El trozo de **CUEX** significa los bloques de concatenación de tamaño fijo y cada uno de estos representa el punto de referencia.

#### Información DAO ####

Esta información también está presente en todas las versiones del formato NRG. Los fragmentos de **DAOI** almacenan la información específica relevante en 2 partes. Su primera parte consta únicamente de los datos específicos de la sesión. Su segunda parte solo repite la información gris relacionada con el seguimiento y es solo una vez para cada pista.

#### CD-texto ####

Esto está disponible en la segunda versión de NRG. El fragmento de **CDTX** consiste en la concatenación sin procesar del paquete de texto de CD que tiene 18 bytes para cada uno.

#### Información de pista extendida ####

Está disponible en todas las versiones del formato de archivo de NRG. Estos fragmentos se utilizan para almacenar la información de seguimiento para el seguimiento de sesiones simultáneas. Este dato se repite una sola vez en el caso de cada pista.

#### Información de la sesión ####

Esto también está disponible en todas las versiones del formato de archivo de NRG. La información de los fragmentos de la sesión debe utilizarse para escanear la imagen de la sesión rápidamente y luego rastrear el recuento.

#### Fin de la cadena ####

El fragmento final significa que ahora no hay más fragmentos que deban leerse y esto también está disponible en todas las versiones de NRG.


## Referencias ##

* [NRG - por Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))


