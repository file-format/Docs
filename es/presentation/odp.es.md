{
  "date" : "2019-10-11",
  "keywords" :[ "archivo odp", "formato de archivo odp", "qué es un archivo odp", "archivo", "ejemplo odp", "extensión de archivo odp","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - Formato de archivo de presentación de OpenOffice",
  "description":"Obtenga más información sobre el formato de archivo ODP y las API que pueden crear y abrir archivos ODP",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo ODP?

Los archivos con extensión .odp representan el formato de archivo de presentación utilizado por OpenOffice.org en el estándar OASISOpen. Un archivo de presentación es una colección de diapositivas donde cada diapositiva puede incluir texto, imágenes, formato, animaciones y otros medios. Estas diapositivas se presentan a la audiencia en forma de presentaciones de diapositivas con configuraciones de presentación personalizadas. Los archivos ODP se pueden abrir con aplicaciones que se ajusten al formato OpenDocument (como OpenOffice o StarOffice).

## Breve historia

Las especificaciones del formato de archivo ODP se basan en el estándar desarrollado como especificaciones ODF. Estas especificaciones han evolucionado en el pasado en forma de tres versiones desarrolladas y publicadas por OASIS de la siguiente manera:

`2005` - La versión 1.0 se publicó en mayo de 2005
`2007`: la versión 1.1 se publicó en febrero de 2007
`2011`: la versión 1.2 se publicó en septiembre de 2011

Hubo cambios bastante menores en la transición de las versiones ODF 1.0 a 1.1. La [versión de ODF 1.2] (https://www.oasis-open.org/standards#opendocumentv1.2) es la última versión de las especificaciones de ODF y los desarrolladores deben consultarla para el desarrollo de aplicaciones relacionadas con la lectura/escritura de ODS.

## Especificaciones de formato de archivo

El formato OpenDocument admite la representación de documentos como un único documento XML, así como una colección de varios subdocumentos dentro de un paquete como archivo [ZIP](https://docs.fileformat.com/Compression/ZIP/). Cada uno de los archivos del archivo ZIP almacena parte del documento completo. Cada subdocumento almacena un aspecto particular del documento. Por ejemplo, un subdocumento contiene la información de estilo y otro subdocumento contiene el contenido del documento. Un documento ODF típico tiene los siguientes componentes:

* `content.xml`: contenido del documento y estilos automáticos utilizados en el contenido.
* `styles.xml`: estilos utilizados en el contenido del documento y estilos automáticos utilizados en los propios estilos.
* `meta.xml`: metainformación del documento, como el autor o la hora de la última acción de guardado.
* `settings.xml`: configuración específica de la aplicación, como el tamaño de la ventana o la información de la impresora.

Además de estos, en el paquete puede haber muchos otros subdocumentos como miniaturas de documentos, imágenes, etc.

Los archivos de documentos de hoja de cálculo son el subconjunto de archivos ODF donde el contenido (hojas) se almacena en el subdocumento content.xml.

## Referencias

* [OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

