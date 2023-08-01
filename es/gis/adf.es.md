{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - Formato de cuadrícula binaria ESRI ArcInfo",
  "description":"Obtenga información sobre el formato de archivo ADF y las API que pueden crear y abrir archivos ADF",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## ¿Qué es un archivo ADF?

Un archivo con extensión .adf es un formato de archivo de datos ráster utilizado por aplicaciones de software ESRI como ArcGIS, ArcView y ArcInfo. Los datos espaciales se almacenan como una cuadrícula binaria que es nativa de ESRI. La cuadrícula se compone de filas y columnas de celdas que pueden ser números enteros y coma flotante. Las cuadrículas de enteros en un archivo ADF representan datos discretos y las cuadrículas de punto flotante representan datos continuos. Otro formato de archivo ESRI popular es el archivo [SHP](/es/gis/shp/) que representa información geoespacial en forma de datos vectoriales para ser utilizados por aplicaciones de sistemas de información geográfica (GIS).

## Formato de archivo ADF - Más información

Los archivos ADF se guardan como archivos binarios en un disco en una cuadrícula binaria. Las cuadrículas de enteros tienen atributos que se almacenan en una tabla de atributos de valor (IVA). Cada valor único en la cuadrícula tiene un registro en VAT donde el registro almacena el valor único y el número de celdas en la cuadrícula está representado por ese valor.

Las rejillas de coma flotante no tienen IVA.

### Estructura de cuadrícula

Dentro del archivo ADF, las cuadrículas se implementan utilizando una estructura de datos ráster en mosaico. La unidad básica dentro de esta estructura de datos ráster es un bloque rectangular de celdas. Cada bloque se almacena en un disco y se comprime en una estructura de archivo de longitud variable, llamada mosaico. Cada bloque se almacena como un registro de longitud variable.

Los rásteres de GRID se almacenan en espacios de trabajo, donde un espacio de trabajo contiene un subdirectorio de información y un subdirectorio para cada GRID. Hay varios archivos que ubican geográficamente y atribuyen datos para la grilla correspondiente. El subdirectorio Info contiene varios archivos que mantienen cierta información sobre GRID y otros conjuntos de datos, como coberturas, en el espacio de trabajo.

## Referencias ##

* [Formato de cuadrícula ESRI](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)


