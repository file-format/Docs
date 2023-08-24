{
  "date" : "2019-10-11",
  "keywords" :[ "archivo ott", "formato de archivo ott", "qué es un archivo ott", "archivo", "ejemplo de ott", "extensión de archivo ott","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - Archivo de plantilla de OpenDocument",
  "description":"Obtenga más información sobre el formato de archivo OTT y las API que pueden crear y abrir archivos OTT",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo OTT?

Los archivos con extensión OTT representan documentos de plantilla generados por aplicaciones de conformidad con el formato estándar OpenDocument de OASIS. Estos se crean con aplicaciones de procesador de texto, como OpenOffice Writer gratuito, y pueden contener configuraciones que se pueden usar para generar nuevos documentos a partir de estos archivos de plantilla. Estas configuraciones incluyen márgenes de página, bordes, encabezados, pies de página y otras configuraciones de página. Estas plantillas se utilizan en documentos oficiales, como membretes de empresas y formularios estandarizados.

## Breve historia ##

Las especificaciones del formato de archivo ODP se basan en el estándar desarrollado como especificaciones ODF. Estas especificaciones han evolucionado en el pasado en forma de tres versiones desarrolladas y publicadas por OASIS de la siguiente manera:

**2005:** La versión 1.0 se publicó en mayo de 2005

**2007:** La versión 1.1 se publicó en febrero de 2007

**2011:** La versión 1.2 se publicó en septiembre de 2011

Hubo cambios bastante menores en la transición de las versiones ODF 1.0 a 1.1. La [versión de ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) es la última versión de las especificaciones de ODF y los desarrolladores deben consultarla para el desarrollo de aplicaciones relacionadas con la lectura/escritura de ODS.

## Especificaciones de formato de archivo

El formato OpenDocument admite la representación de documentos como un solo documento XML, así como una colección de varios subdocumentos dentro de un paquete como archivo [ZIP](/es/compression/zip/). Cada uno de los archivos del archivo ZIP almacena parte del documento completo. Cada subdocumento almacena un aspecto particular del documento. Por ejemplo, un subdocumento contiene la información de estilo y otro subdocumento contiene el contenido del documento. Un documento ODF típico tiene los siguientes componentes:

* content.xml: contenido del documento y estilos automáticos utilizados en el contenido.
* estilos.xml: estilos utilizados en el contenido del documento y estilos automáticos utilizados en los propios estilos.
* meta.xml: metainformación del documento, como el autor o la hora de la última acción de guardado.
* settings.xml: configuración específica de la aplicación, como el tamaño de la ventana o la información de la impresora.

Además de estos, en el paquete puede haber muchos otros subdocumentos como miniaturas de documentos, imágenes, etc. Los archivos de documentos son el subconjunto de archivos ODF donde el contenido (hojas) se almacena en //content.xml// subdocumento.

## Referencias ##

* [OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

