{
  "date" : "2020-08-20",
  "keywords" :[ "archivo woff", "formato de archivo woff", "qué es un archivo woff", "archivo", "ejemplo woff", "extensión de archivo woff","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Formato de archivo abierto web",
  "description":"Un archivo WOFF es un formato de fuente abierta creado en el formato de fuente abierta web.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## ¿Qué es un archivo WOFF?

Un archivo con la extensión .woff es un archivo de fuente web basado en el formato de fuente abierta web (WOFF). Tiene un contenedor comprimido de formato específico basado en tipos de fuente TrueType (.TTF) u OpenType (.OTT). WOFF se introdujo con el objetivo de diferenciar las fuentes web de los archivos de fuentes utilizados en las aplicaciones de escritorio. Además, el formato apuntaba a reducir la latencia de la transferencia de fuentes desde el servidor a la computadora del cliente a través de la red. Hay varias herramientas disponibles que pueden convertir archivos WOFF a TTF y otros formatos de archivos de fuentes.

## **Formato de archivo WOFF**

El formato de fuente WOFF comprime tablas de datos de fuentes de estructuras sfnt basadas en tablas utilizadas en diferentes tipos de fuentes, como TrueType, OpenType y Open Font Format. Es como un contenedor para estos tipos de fuentes y también tiene espacio para incluir los metadatos de las fuentes y los datos de uso privado que se incluirán en el contenedor. Los convertidores usan los archivos sfnt en un archivo con formato WOFF y los agentes de usuario restauran el archivo codificado para usarlo con el documento web. Cabe señalar que los datos de fuente restaurados coinciden exactamente con el formato de fuente de entrada en todos los aspectos.

Las utilidades de archivo WOFF a menudo contienen características adicionales, como subconjuntos de glifos, validación o adiciones de características de fuente, pero no es necesario. Tanto el creador como los agentes de uso deben asegurarse de que se conserve la validez de los datos de fuentes subyacentes.

### Estructura del archivo WOFF

La estructura de archivos WOFF es similar a la de las fuentes sfnt. Se basa en un directorio de tablas que contiene las longitudes y los desplazamientos de cada tabla de datos de fuente. Todas las tablas se siguen después de esta información inicial. El archivo contiene una base de datos de fuentes que son las mismas que las fuentes originales. El orden de las tablas también es el mismo pero cada una puede estar comprimida. Sin embargo, el directorio de la tabla WOFF reemplaza el directorio de la tabla original.

Un archivo WOFF consta de lo siguiente:

* WOFFHeader: encabezado de archivo con tipo de fuente y versión básicos, junto con compensaciones de metadatos y bloques de datos privados.
* TableDirectory: directorio de tablas de fuentes, que indica el tamaño original, el tamaño comprimido y la ubicación de cada tabla dentro del archivo WOFF.
* FontTables: las tablas de datos de fuentes de la fuente sfnt de entrada, comprimidas para reducir los requisitos de ancho de banda.
* ExtendedMetadata: un bloque opcional de metadatos extendidos, representados en formato XML y comprimidos para su almacenamiento en el archivo WOFF.
* PrivateData: un bloque opcional de datos privados para que lo use el diseñador de fuentes, la fundición o el proveedor.

### Encabezado WOFF
El encabezado WOFF consta de una firma identificativa que indica el tipo de datos incluidos en el archivo. El encabezado WOFF junto con sus campos es el siguiente.

|Tipo|Nombre de campo|Descripción|
---|---|---|
|UInt32|firma |0x774F4646 'wOFF' |
|UInt32| sabor |La "versión sfnt" de la fuente de entrada.|
|UInt32| longitud |Tamaño total del archivo WOFF.|
|UInt16| numTables |Número de entradas en el directorio de tablas de fuentes.|
|UInt16| reservado |Reservado; puesto a cero.|
|UInt32| totalSfntSize |Tamaño total necesario para los datos de fuentes sin comprimir, incluido el encabezado sfnt, el directorio y las tablas de fuentes (incluido el relleno).|
|UInt16| majorVersion |Versión principal del archivo WOFF.|
|UInt16| minorVersion |Versión menor del archivo WOFF.|
|UInt32| metaOffset |Desplazamiento al bloque de metadatos, desde el comienzo del archivo WOFF.|
|UInt32| metaLength |Longitud del bloque de metadatos comprimido.|
|UInt32| metaOrigLength |Tamaño sin comprimir del bloque de metadatos.|
|UInt32| privOffset |Desplazamiento al bloque de datos privados, desde el principio del archivo WOFF.|
|UInt32| privLength |Longitud del bloque de datos privados.|


## **Referencias**
* [Formato de archivo w3 WOFF](https://www.w3.org/TR/WOFF/)

