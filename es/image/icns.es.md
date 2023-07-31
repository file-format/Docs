{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "extensión", "archivo", "formato", "imagen", "Imagen de icono de Apple", "macOS", "Apple", "Icono" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Imagen del icono de Apple",
  "description":"Obtenga información sobre el formato de archivo ICNS y las API que pueden crear y abrir archivos ICNS",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## ¿Qué es un archivo ICNS? ##

Un formato de icono utilizado por los programas macOS se denomina archivo ICNS. Permite bandas alfa de 1 y 8 bits y guarda una o más imágenes, generalmente hechas a partir de documentos [PNG](/es/image/png/). El ícono del programa en el navegador y la interfaz de macOS se muestra usando archivos ICNS.

Según la ubicación, el mismo icono de estilo puede tener varias configuraciones. El formato ICNS ha sufrido numerosas modificaciones y ha evolucionado hasta el punto en que ahora puede utilizarse como base para varios formatos compatibles. Aquí hay algunos otros puntos importantes que necesita saber:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource y Mac OS icons Resource son algunos de los otros nombres.
* Para la información de los iconos, se utiliza una fuente en la rama de recursos.
* En la mayoría de los casos, un archivo contiene numerosas imágenes. Los tamaños de imagen admitidos son de 1612 píxeles cuadrados y 1024, 512, 256, 128, 48, 32 y 16 píxeles cuadrados.


## Formato de archivo ICNS ##

El formato de datos ICNS es una cápsula para una o más imágenes, que admite bandas de 1 bit y numerosos estados de imagen.
El sistema operativo puede cambiar el tamaño de las imágenes de los iconos para que se ajusten al tamaño de visualización requerido. Las imágenes de iconos más grandes normalmente se guardan como archivos [JPEG](/es/image/jpeg/) 2000 o [PNG](/es/image/png/). Es posible un tipo de archivos ICNS tanto comprimidos como sin comprimir.

Un encabezado y datos de iconos binarios conforman la estructura de un archivo ICNS. El encabezado contiene 8 bytes de datos, cuatro de los cuales son el literal mágico y cuatro de los cuales son la longitud del archivo. El tipo y el tamaño de cada imagen de icono se almacenan en la sección de datos de iconos, a la que siguen los datos de imagen binarios. El tamaño de la imagen determina el tamaño de la sección binaria.

## Especificación técnica ##

### Encabezado ###

|Desplazamiento|Tamaño|Objetivo
---|---|---|
|0|4|Literal mágico, debe ser "icns" (0x69, 0x63, 0x6e, 0x73)
|4|4|Longitud del archivo, en bytes, msb primero


### Datos del icono ###

|Desplazamiento|Tamaño|Objetivo
---|---|---|
|0|4|Tipo de icono
|4|4|Longitud de los datos, en bytes (incluidos el tipo y la longitud), msb primero
|8|Variable|Datos de icono

### Compresión ###

Los datos de píxeles están comprimidos hasta cierto punto. Los píxeles de 32 bits ("is32", "il32", "ih32", "it32") y ARGB ("ic04", "ic05") a menudo se comprimen (por canal) de forma similar a PackBits.

|Valor principal|Bytes finales|Resultado (sin comprimir)
---|---|---|
|0 - 127|1 - 128|1 - 128 bytes
|128 - 255|1 Byte|3 - 130 Copias

## Referencia ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

