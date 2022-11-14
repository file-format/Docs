{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "extensión", "archivo", "formato", "eBook", "Formato de archivo Kindle", "Estructura de archivo AZW3" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo AZW3 y las API que pueden crear y abrir archivos AZW3",
  "title" :"¿Qué es un archivo AZW3?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## ¿Qué es un archivo AZW3?

AZW3, también conocido como Kindle Format 8 (**KF8**), es la versión modificada del formato de archivo digital de libros electrónicos [AZW](/es/ebook/azw/) desarrollado para dispositivos Amazon Kindle. El formato es una mejora de los archivos AZW más antiguos y se usa en dispositivos Kindle Fire solo con compatibilidad con el formato de archivo anterior, es decir, [MOBI](/es/ebook/mobi/) y AZW. Amazon introdujo el formato KFX (KF versión 10) después de KF8 que se usa en los últimos dispositivos Kindle. Los archivos AZW3 tienen una aplicación de tipo de medio de Internet/vnd.amazon.mobi8-ebook. Los archivos AZW3 se pueden convertir a otros formatos de archivo, como [PDF](/es/pdf/), [EPUB](/es/ebook/epub/), [AZW](/es/ebook/azw/), [DOCX](/es/ procesamiento de textos/docx/) y [RTF](/es/procesamiento de textos/rtf/).

## Formato de archivo AZ3/KF8 ##

Los archivos KF8 son de naturaleza binaria y conservan la estructura de un formato de archivo MOBI como archivo PDB. Como se mencionó anteriormente, un archivo KF8 puede consistir tanto en un MOBI como en una versión KF8 más reciente de EPUB más adelante. Los detalles internos del formato han sido decodificados por [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), que es un script de Python que analiza la base de datos compilada final y extrae los archivos fuente MOBI o AZW de ella. Los archivos AZW3 (KF8) apuntan a la versión EPUB3 con compatibilidad con versiones anteriores para EPUB también. KF8 compila los archivos EPUB y genera una estructura binaria basada en el formato de archivo PDB.

## Referencias ##

* [KF8 - Por Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Desempaquetar Kindle](https://github.com/kevinhendricks/KindleUnpack)

