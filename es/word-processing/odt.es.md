{
  "date" : "2019-10-11",
  "keywords" :[ "archivo odt", "formato de archivo odt", "qué es un archivo odt", "archivo", "ejemplo de odt", "extensión de archivo odt","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODT - Archivo de texto de OpenDocument",
  "description":"Obtenga información sobre el formato de archivo ODT y las API que pueden crear y abrir archivos ODT",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo ODT?

Los archivos ODT son un tipo de documentos creados con aplicaciones de procesamiento de texto que se basan en el formato de archivo de texto OpenDocument. Estos se crean con aplicaciones de procesador de texto, como OpenOffice Writer gratuito, y pueden contener contenido como texto, imágenes, objetos y estilos. El archivo ODT es para el procesador de texto Writer lo que [DOCX](/es/word-processing/docx/) es para Microsoft Word. Varias aplicaciones, incluidos Google Docs y el procesador de textos basado en la web de Google incluido con Google Drive, pueden abrir los archivos ODT para editarlos. Microsoft Word también puede abrir archivos ODT y guardarlos en otros formatos como [DOC](/es/word-processing/doc/) y DOCX.

## Breve historia ##

Las especificaciones del formato de archivo ODP se basan en el estándar desarrollado como especificaciones ODF. Estas especificaciones han evolucionado en el pasado en forma de tres versiones desarrolladas y publicadas por OASIS de la siguiente manera:

**2005** La versión 1.0 se publicó en mayo de 2005

**2007:** La versión 1.1 se publicó en febrero de 2007

**2011:** La versión 1.2 se publicó en septiembre de 2011

Hubo cambios bastante menores en la transición de las versiones ODF 1.0 a 1.1. La [versión de ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) es la última versión de las especificaciones de ODF y los desarrolladores deben consultarla para el desarrollo de aplicaciones relacionadas con la lectura/escritura de ODS.

## Especificaciones de formato de archivo ##

El formato OpenDocument admite la representación de documentos como un solo documento XML, así como una colección de varios subdocumentos dentro de un paquete como archivo [ZIP](/es/Compression/ZIP/). Cada uno de los archivos del archivo ZIP almacena parte del documento completo. Cada subdocumento almacena un aspecto particular del documento. Por ejemplo, un subdocumento contiene la información de estilo y otro subdocumento contiene el contenido del documento. Un documento ODF típico tiene los siguientes componentes:

* content.xml: contenido del documento y estilos automáticos utilizados en el contenido.
* estilos.xml: estilos utilizados en el contenido del documento y estilos automáticos utilizados en los propios estilos.
* meta.xml: metainformación del documento, como el autor o la hora de la última acción de guardado.
* settings.xml: configuración específica de la aplicación, como el tamaño de la ventana o la información de la impresora.

Además de estos, en el paquete puede haber muchos otros subdocumentos como miniaturas de documentos, imágenes, etc. Los archivos de documentos son el subconjunto de archivos ODF donde el contenido (hojas) se almacena en //content.xml// subdocumento.

## Referencias ##

* [OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

