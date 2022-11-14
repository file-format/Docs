{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo CPG - Archivo de página de códigos ESRI",
  "description":"Obtenga información sobre el formato de archivo CPG y las API que pueden crear y abrir archivos CPG",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## ¿Qué es un archivo CPG?

Un archivo CPG es un archivo opcional que requiere el ESRI Shapefile que se usa para especificar la página de códigos para identificar el conjunto de caracteres que se usará. Estos se almacenan en formato de archivo de texto sin formato y contienen información sobre la codificación aplicada para crear el archivo de forma. En caso de que un archivo CPG no esté disponible, el archivo de forma utiliza la codificación predeterminada del sistema. Un archivo CPG, si está presente, debe tener el mismo prefijo que el del archivo [SHP](/es/gis/shp/), por ejemplo, carreteras.shp, carreteras.cpg.

Los archivos CPG se pueden abrir con ESRI ArcGIS Pro.

### Formato de archivo CPG - Más información

Al ver un archivo de forma en ArcCatalog o cualquier otra aplicación de ArcGIS, solo ve el archivo de forma. Pero en realidad, el archivo de formas usa otros archivos asociados que se leen junto con el archivo de formas principal. El archivo CPG también es uno de estos si está presente junto con el archivo SHP principal.

## Referencias

* [Extensiones de archivo de forma
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

