{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "archivo", "extensión", "formato de archivo", "Valores separados por comas", "Hoja de cálculo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo CSV y las API que pueden crear y abrir archivos CSV",
  "title" :"Formato de archivo CSV",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## ¿Qué es un archivo CSV?

Los archivos con la extensión .csv (valores separados por comas) representan archivos de texto sin formato que contienen registros de datos con valores separados por comas. Cada línea en un archivo CSV es un nuevo registro del conjunto de registros contenidos en el archivo. Dichos archivos se generan cuando se pretende transferir datos de un sistema de almacenamiento a otro. Dado que todas las aplicaciones pueden reconocer registros separados por comas, la importación de dichos archivos de datos a la base de datos se realiza de manera muy conveniente. Casi todas las aplicaciones de hojas de cálculo como Microsoft Excel u OpenOffice Calc pueden importar CSV sin mucho esfuerzo. Los datos importados de dichos archivos se organizan en celdas de una hoja de cálculo para su representación al usuario.

## Breve historia ##

Los siguientes son algunos datos breves sobre el origen y la historia del formato de archivo CSV.

* 1972: el compilador IBM Fortran (nivel H extendido) los admitió en OS/360

* 1978: la entrada/salida dirigida por lista fue admitida por FORTRAN 77 que usaba comas y espacios para delimitadores

* 2005: CSV se estandarizó con [RFC4180](https://tools.ietf.org/html/rfc4180) como tipo de contenido MIME.

* 2013 - Las deficiencias de RFC4180 fueron manejadas por una recomendación W3C

* 2015: el W3C realizó los primeros borradores de recomendaciones para los estándares de metadatos CSV, que comenzaron como recomendación en diciembre de 2015

## Convertir archivos CSV ##

Los archivos CSV se pueden convertir a varios formatos de archivo diferentes usando las aplicaciones que pueden abrir estos archivos. Por ejemplo, Microsoft Excel puede importar datos del formato de archivo CSV y guardarlos en XLS, [XLSX](/es/spreadsheet/xlsx/), [PDF](/es/pdf/), [TXT](/es/word-processing/txt/) , XML y [HTML](/es/web/html/) formatos de archivo. De manera similar, otros servicios de escritorio y en línea ofrecen la capacidad de exportar archivos CSV a HTML, ODS y [RTF](/es/word-processing/rtf/).

## Formato de archivo CSV ##

Se sabe que el formato de archivo CSV se especifica en [RFC4180](https://tools.ietf.org/html/rfc4180). Define que cualquier archivo sea compatible con CSV si:

* Cada registro se ubica en una línea separada, delimitada por un salto de línea (CRLF). Por ejemplo:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* El último registro del archivo puede tener o no un salto de línea final. Por ejemplo:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx
* Puede haber una línea de encabezado opcional que aparece como la primera línea del archivo con el mismo formato que las líneas de registro normales. Este encabezado contendrá los nombres correspondientes a los campos del archivo y debe contener el mismo número de campos que los registros en el resto del archivo (la presencia o ausencia de la línea del encabezado debe indicarse a través del parámetro opcional "encabezado" de este Tipo de Mimica). Por ejemplo:
* nombre_campo,nombre_campo,nombre_campo CRLF
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* ﻿Dentro del encabezado y de cada registro, puede haber uno o más campos, separados por comas. Cada línea debe contener el mismo número de campos en todo el archivo. Los espacios se consideran parte de un campo y no deben ignorarse. El último campo del registro no debe ir seguido de una coma. Por ejemplo:
* aaa,bbb,ccc
* Cada campo puede o no estar encerrado entre comillas dobles (sin embargo, algunos programas, como Microsoft Excel, no usan comillas dobles). Si los campos no están entre comillas dobles, es posible que no aparezcan comillas dobles dentro de los campos. Por ejemplo:\
* "aaa", "bbb", "ccc" CRLF
* zzz,yyy,xxx
* Los campos que contienen saltos de línea (CRLF), comillas dobles y comas deben estar entre comillas dobles. Por ejemplo:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz,yyy,xxx
* Si se usan comillas dobles para encerrar campos, entonces una comilla doble que aparece dentro de un campo debe escaparse precediéndola de otra comilla doble. Por ejemplo:
* "aaa","b""bb","ccc"

Sin embargo, a la luz del uso moderno, el delimitador no se limita solo a la coma y también puede ser punto y coma, tabulación o espacios. Las aplicaciones como Microsoft Excel brindan la opción de especificar el carácter delimitador para importar registros desde un archivo CSV.

## Referencias

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

