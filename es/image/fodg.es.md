{
  "date" : "2019-10-11",
  "keywords" :[ "archivo fodg", "formato de archivo fodg", "qué es un archivo fodg", "archivo", "ejemplo de fodg", "extensión de archivo fodg","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - Formato de archivo de dibujo de OpenDocument",
  "description":"Obtenga información sobre el formato de archivo FODG y las API que pueden crear y abrir archivos FODG",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo FODG?

Un archivo con extensión .fodg es un formato de archivo Apache OpenOffice Drawing para almacenar elementos de dibujo. Se basa en las especificaciones de formato de archivo descritas por Advancement of Structural Information Standards (OASIS). Otro formato de archivo similar para los gráficos de OpenOffice es [ODG](/es/image/odg/) que almacena elementos de dibujo como una imagen vectorial. Los archivos FODG se pueden abrir con OpenOffice y LibreOffice. Otros formatos de archivo admitidos por OpenOffice, por ejemplo, incluyen [ODT](/es/word-processing/odt/), ODF, [ODP](/es/presentation/odp/) y [ODS](/es/spreadsheet/ods/).

## Formato de archivo FODG

FODG se basa en el formato de archivo XML de OpenDocument que cumple con OASIS OpenDocument Format ISO/IEC 26300. Tiene tipo de medio de Internet application/vnd.oasis.opendocument.graphics y también cumple con org.oasis-open.opendocument public.composite-content . La estructura XML es común para todos los tipos de documentos, como hojas de cálculo, archivos de dibujo y documentos de texto. Los documentos de OpenOffice aprovechan la separación de preocupaciones al separar el contenido, los estilos, los metadatos y la configuración de la aplicación en cuatro archivos XML separados.

`<office:document-content> ` - Contenido del documento y estilos automáticos utilizados en el contenido.
`<office:document-styles> ` - Estilos usados en el contenido del documento y estilos automáticos usados en los propios estilos.
`<office:document-meta> ` - Metainformación del documento, como el autor o la hora de la última acción de guardado.
`<office:document-settings> ` - Configuración específica de la aplicación, como el tamaño de la ventana o la información de la impresora.

## Referencias ##
* [Especificaciones futuras para la estandarización v 1.3](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [Formato de documento abierto de OASIS para aplicaciones de Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Formato OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

