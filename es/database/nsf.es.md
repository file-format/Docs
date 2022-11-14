{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo NSF y las API que pueden crear y abrir archivos NSF",
  "title" :"Formato de archivo NSF - Formato de base de datos de Lotus Notes",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## ¿Qué es un archivo NSF?

Un archivo con la extensión .nsf (Notes Storage Facility) es un formato de archivo de base de datos utilizado por el [software IBM Notes] (https://en.wikipedia.org/wiki/HCL_Domino), que anteriormente se conocía como Lotus Notes. Define el esquema para almacenar diferentes tipos de objetos, como correos electrónicos, citas, documentos, formularios y vistas. Toda esta información está contenida en un solo archivo NSF para colaboración comercial similar a un archivo PST/OST. Algunas de las aplicaciones que pueden abrir archivos NSF incluyen IBM Lotus Notes e IBM Domino.

## Especificaciones de formato de archivo NSF

Los archivos NSF son de naturaleza binaria y sus especificaciones están disponibles por Joachim Metz en [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database% 20archivo%20formato.asciidoc). Según estos detalles, un archivo NSF se compone de:

* Encabezado de archivo
* Cabecera de la base de datos

Además, consta de:

* Supermanzana
* Bloque descriptor de cubo
* Mapa de bits
* Cubo de vectores de reubicación de registros
* Cubos de resumen
* Cubos no resumidos


### Encabezado del archivo NSF

El encabezado del archivo NSF tiene un tamaño de 6 bytes. Consiste en:

|Compensación|Tamaño|Valor|Descripción|
---|---|---|---|
0|2|0x1a 0x00|Firma|
2|4| |El tamaño del encabezado de la base de datos|

### Cabecera de la base de datos

El encabezado de la base de datos NSD contiene los siguientes valores confirmados.

* Información de la base de datos
* Identificador de base de datos (DBID)
* Información de replicación
* Banderas de búfer de información de base de datos
* Título
* Categorías
* Clase
* Clase de diseño (nombre de la plantilla)
* Identificadores de notas especiales
* Relleno
* Información de la base de datos 2
* Información de la base de datos 3
* Información de la base de datos 4
* Información de la base de datos 5
* Relleno
* Identificador de instancia de base de datos (DBIID)
* Historial de replicación

## Referencias

* [Formato NSF - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

