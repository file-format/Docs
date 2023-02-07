{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AVL - Archivo de leyenda de ArcView",
  "description":"Obtenga información sobre el formato de archivo AVL y las API que pueden crear y abrir archivos AVL",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## ¿Qué es un archivo AVL?

Un archivo AVL es un archivo de leyenda que contiene una clave para un mapa generado con el software ESRI ArcView GIS (Sistema de información geográfica). Contiene información de simbología de referencia utilizada en el mapa correspondiente para el acceso. Un archivo AVL puede contener más información, como simbología, configuración de visualización, como transparencia, propiedades de visualización dependientes de la escala, tabla unida/información de tabla relacionada, consulta de definición, propiedades de etiquetado para capas de entidades y propiedades de visualización de anotaciones para capas de anotaciones según el tipo. especie de capa.

Se puede hacer referencia a un archivo AVL desde el archivo del proyecto ArcView [.APR](/es/gis/apr/).

## Formato de archivo AVL - Más información

Los archivos AVL se guardan en formato de archivo de texto sin formato. Significa que puede abrir archivos AVL en cualquier editor de texto como Notepad, Notepad ++ y Apple TextEdit. Una vez abierto, no solo puede ver el contenido del archivo sino también modificarlo.

### Diferencia entre archivos .LYR y .AVL

* **Diferencia de formato de archivo** - .lyr es un archivo binario mientras que .avl es un archivo de texto
* **Diferencia de contenido**: un archivo .lyr contiene más información que un archivo .avl. Un archivo AVL solo almacena información de simbología, mientras que un archivo LYR almacena toda la información disponible en el cuadro de diálogo de propiedades de capa en ArcMap.

## Referencias

* [Diferencia entre archivos .lyr y .avl](https://support.esri.com/en/technical-article/000005936)

