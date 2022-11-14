{
  "date" : "2019-10-11",
  "keywords" :[ "archivo qlr", "formato de archivo qlr", "qué es un archivo qlr", "archivo", "ejemplo de qlr", "extensión de archivo qlr","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - Archivo de definición de capa QGIS",
  "description":"Obtenga información sobre el formato de archivo QLR y las API que pueden crear y abrir archivos QLR",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## ¿Qué es un archivo QLR?

Un archivo con .qlr es un archivo de definición de capa que contiene un puntero a la fuente de datos de la capa. Esto se suma a la información de estilo [QGIS](https://www.qgis.org/en/site/) para la capa. Al tener referencias a todos los estilos relacionados, este archivo se usa como fuente única de datos para obtener la información de estilo. Con los archivos QLR, la información de las fuentes de datos se puede colocar en este único archivo que otras aplicaciones pueden leer para cargar la información de estilo. Los archivos QLR se pueden abrir con cualquier editor de texto como Notepad++.

## Formato de archivo QLR

QLR, similar a [QGS](/es/gis/qgs/), es un archivo XML que contiene punteros a la fuente de datos de la capa en forma de etiquetas XML. Es similar al archivo .lyr de ArcGIS. Las etiquetas de nivel superior de un archivo QML se muestran en la imagen a continuación.

{{< figure src="../qlr.png" title="" >}}

## Referencias

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

