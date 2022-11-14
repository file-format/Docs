{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "archivo", "extensión", "formato de archivo", "Excel", "Hoja de cálculo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo OTS y las API que pueden crear y abrir archivos OTS",
  "title" :"OTS: formato de archivo de plantilla de hoja de cálculo de OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## ¿Qué es un archivo OTS?

Un archivo con extensión .ots es un archivo de plantilla de hoja de cálculo de OpenDocument que se crea con el software de aplicación Calc incluido en Apache OpenOffice. El software de aplicación Calc es similar a Excel disponible en Microsoft Office. El formato de archivo OTS se utiliza para crear plantillas que contienen configuraciones predefinidas relacionadas con estilos, fuentes, datos, diseño de hojas de cálculo y formato. Los archivos OTF tienen `aplicación tipo mime/vnd.oasis.opendocument.spreadsheet-template`. Estos archivos de plantilla se pueden utilizar como punto de partida para generar y guardar archivos de datos reales que se guardan en [formato de archivo ODS](/es/hoja de cálculo/ods/). Los archivos OTS se pueden usar con aplicaciones como OpenOffice y LibreOffice.

## Formato de archivo OTS

Los archivos OTS se guardan en el formato de archivo basado en XML OpenDocument de OASIS que se compone de una colección de varios subdocumentos con un paquete como un archivo [ZIP](/es/compression/zip/). Cada archivo zip almacena parte del documento completo y cada subdocumento almacena un aspecto particular del documento. Por ejemplo, un subdocumento contiene la información de estilo y otro subdocumento contiene el contenido del documento. Un documento ODF típico tiene los siguientes componentes:

### Contenido OTS.xml

El archivo content.xml contiene el contenido real del documento. Sin embargo, esto no incluye datos binarios como imágenes.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml de formato de archivo OTS

El archivo styles.xml contiene información de estilo y se usa mucho para dar formato y diseño. Los tipos de estilos incluyen:

* Estilos de párrafo
* Estilos de página
* Estilos de personajes
* Estilos de marco
* Estilos de lista

### Meta.xml

El archivo meta.xml contiene información sobre los metadatos del archivo, como autor, última fecha de modificación, etc.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Configuración.xml

El archivo `settings.xml` incluye configuraciones de nivel de documento, como el factor de zoom y la posición del cursor.

## Referencias ##

* [Especificación de OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

