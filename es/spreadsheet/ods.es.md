{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "archivo", "extensión", "formato de archivo", "Hoja de cálculo OpenDocument" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tu guía de formato de archivo para saber qué es un archivo ODS y las API que puedes crear y abrir",
  "title" :"¿Qué es un archivo ODS?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## ¿Qué es un archivo ODS?

Los archivos con extensión .ods representan el formato de documento de hoja de cálculo OpenDocument que el usuario puede editar. Los datos se almacenan dentro del archivo ODF en filas y columnas. Es un formato basado en XML y es uno de los varios subtipos de la familia Open Document Formats (ODF). El formato se especifica como parte de las especificaciones ODF 1.2 publicadas y mantenidas por OASIS. Varias aplicaciones en Windows, así como en otros sistemas operativos, pueden abrir archivos ODS para editarlos y manipularlos, incluidos Microsoft Excel, NeoOffice y LibreOffice. Los archivos ODS también se pueden convertir a otros formatos de hoja de cálculo, como [XLS](/es/spreadsheet/xls/), [XLSX](/es/spreadsheet/xlsx/) y otros mediante diferentes aplicaciones.

## Breve historia ##

Las especificaciones de formato de archivo ODS se basan en el estándar desarrollado como especificaciones ODF. Estas especificaciones han evolucionado en el pasado en forma de tres versiones desarrolladas y publicadas por OASIS de la siguiente manera:

`2005`- La versión 1.0 se publicó en mayo de 2005

`2007`: la versión 1.1 se publicó en febrero de 2007

`2011`: la versión 1.2 se publicó en septiembre de 2011

Hubo cambios bastante menores en la transición de las versiones ODF 1.0 a 1.1. La [versión de ODF 1.2] (https://www.oasis-open.org/standards#opendocumentv1.2) es la última versión de las especificaciones de ODF y los desarrolladores deben consultarla para el desarrollo de aplicaciones relacionadas con la lectura/escritura de ODS.

## Formato de archivo ODS ##

El formato OpenDocument admite la representación de documentos como un solo documento XML, así como una colección de varios subdocumentos dentro de un paquete como archivo [ZIP](/es/compression/zip/). Cada uno de los archivos del archivo ZIP almacena parte del documento completo. Cada subdocumento almacena un aspecto particular del documento. Por ejemplo, un subdocumento contiene la información de estilo y otro subdocumento contiene el contenido del documento. Un documento ODF típico tiene los siguientes componentes:

* `content.xml`: contenido del documento y estilos automáticos utilizados en el contenido.
* `styles.xml`: estilos utilizados en el contenido del documento y estilos automáticos utilizados en los propios estilos.
* `meta.xml`: metainformación del documento, como el autor o la hora de la última acción de guardado.
* `settings.xml`: configuración específica de la aplicación, como el tamaño de la ventana o la información de la impresora.

Además de estos, en el paquete puede haber muchos otros subdocumentos como miniaturas de documentos, imágenes, etc.

Los archivos de documentos de hoja de cálculo son el subconjunto de archivos ODF donde el contenido (hojas) se almacena en el subdocumento content.xml.

## Referencias ##

* [OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

