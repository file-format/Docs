{
  "date" : "2023-01-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo WOFF2 - Archivo Web Open Font Format 2.0",
  "description":"Obtenga información sobre qué es un archivo WOFF2 y las API que pueden crear y abrir un archivo WOFF2",
  "linktitle" : "WOFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-10"
}

## ¿Qué es un archivo WOFF2?

WOFF2 es un formato de archivo de fuente que es una versión más comprimida del formato de fuente abierta web (WOFF). Fue desarrollado como una forma de reducir el tamaño de archivo de las fuentes web, permitiéndoles cargar más rápido y usar menos ancho de banda. WOFF2 usa un algoritmo de compresión llamado Brotli para comprimir los datos de la fuente, lo que puede resultar en tamaños de archivo significativamente más pequeños que las fuentes [WOFF](/es/font/woff/) equivalentes. Este formato es compatible con la mayoría de los navegadores web modernos, incluidos Chrome, Firefox, Safari, Opera y Edge (versión 14 en adelante).

## Formato de archivo WOFF2 - Más información

La estructura de archivo interna de un archivo de fuente WOFF2 se compone de varias partes diferentes, que incluyen un encabezado, metadatos, un directorio de tabla y los datos de la fuente en sí.

1. El encabezado contiene información sobre el formato general del archivo, incluido el número de versión y la cantidad de tablas que están presentes en el archivo.

1. La sección de metadatos contiene información como el nombre de la fuente, los derechos de autor y otra información relacionada con la fuente.

1. El directorio de tablas contiene información sobre las diferentes tablas que componen la fuente, incluida su ubicación en el archivo y su longitud.

1. Los datos de la fuente en sí se dividen en varias tablas diferentes, cada una de las cuales contiene información específica sobre la fuente, como sus caracteres y sus glifos correspondientes. Estas tablas pueden incluir:

* La tabla 'glyf' contiene los contornos reales de las fuentes, incluidos la forma y el tamaño de cada carácter.
* La tabla 'head' contiene información general sobre la fuente, como el número de versión, el tamaño del diseño, etc.
* La tabla 'hmtx' contiene información sobre las métricas de la fuente, incluidos los anchos y las posiciones de los caracteres.
* Cada tabla se comprime y almacena en formato de archivo WOFF2 después de completar el proceso de codificación.

La estructura en general está diseñada para permitir un análisis y decodificación rápidos, de modo que los navegadores web puedan cargar y mostrar la fuente en un sitio web de manera rápida y eficiente.

### Encabezado WOFF2
El encabezado WOFF consta de una firma identificativa que indica el tipo de datos incluidos en el archivo. El encabezado WOFF junto con sus campos es el siguiente.

|Tipo|Nombre de campo|Descripción|
---|---|---|
|UInt32|firma |0x774F4632 'wOF2' |
|UInt32| sabor |La "versión sfnt" de la fuente de entrada.|
|UInt32| longitud |Tamaño total del archivo WOFF.|
|UInt16| numTables |Número de entradas en el directorio de tablas de fuentes.|
|UInt16| reservado |Reservado; puesto a cero.|
|UInt32| totalSfntSize |Tamaño total necesario para los datos de fuentes sin comprimir, incluido el encabezado sfnt, el directorio y las tablas de fuentes (incluido el relleno).|
|UInt32| totalCompressedSize Longitud total del bloque de datos comprimido.|
|UInt16| majorVersion |Versión principal del archivo WOFF.|
|UInt16| minorVersion |Versión menor del archivo WOFF.|
|UInt32| metaOffset |Desplazamiento al bloque de metadatos, desde el comienzo del archivo WOFF.|
|UInt32| metaLength |Longitud del bloque de metadatos comprimido.|
|UInt32| metaOrigLength |Tamaño sin comprimir del bloque de metadatos.|
|UInt32| privOffset |Desplazamiento al bloque de datos privados, desde el principio del archivo WOFF.|
|UInt32| privLength |Longitud del bloque de datos privados.|


## Referencias
* [Formato de archivo w3 WOFF2](https://www.w3.org/TR/WOFF2/)

