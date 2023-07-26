{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "extensión", "archivo", "formato", "Libros de historietas", "Formato de archivo de historietas", "libro electrónico"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo CBC y las API que pueden crear y abrir archivos CBC",
  "title" :"CBC - Formato de archivo de colección de cómics",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## ¿Qué es un archivo CBC?

Un archivo con la extensión .cbc es una colección comprimida de archivos de historietas para libros electrónicos y contiene archivos [CBZ](/es/ebook/cbz/) y [CBR](/es/ebook/cbr/). Lo utiliza [Calibre](https://calibre-ebook.com/), una aplicación de conversión de libros electrónicos, que es un administrador de libros electrónicos de código abierto multiplataforma y le permite administrar sus libros electrónicos y convertirlos a diferentes formatos. . Un archivo CBC contiene un archivo .txt, comics.txt, que enumera otros archivos que forman parte del archivo. Hay varias aplicaciones disponibles en línea que pueden convertir archivos CBC a [AZW3](/es/ebook/azw3/), [EPUB](/es/ebook/epub/), [FB2](/es/ebook/fb2/), [MOBI](/es/ebook/ mobi/), [TXT](/es/word-processing/txt/), [PDF](/es/pdf/) y otros formatos de archivo populares.

## Formato de archivo CBC

Los archivos CBC son archivos comprimidos que contienen CBZ, CBR y un archivo de texto para enumerar los contenidos. El archivo de texto, comics.txt, está codificado en UTF8 y contiene una lista de los archivos CBC que los lectores utilizarán para organizar sus colecciones. Un archivo CBC generalmente tiene varios atributos que permiten la organización de esta colección, como Cómic, Categoría, Editor, Serie, Edición y Artista.

El contenido de un archivo CBC de muestra se enumera a continuación:

* comics.txt: archivo de texto que contiene una lista de archivos CBR y CBZ
* 1.cbz
* 2.cbz
* 3.cbz
* Archivo(s) CBZ

donde el archivo comics.txt enumera el contenido de la siguiente manera:

* 1.cbz: Primer Capítulo
* 2.cbz: Segundo Capítulo
* 3.cbz: Tercer Capítulo

Los lectores procesan el archivo comics.txt y generan la tabla de contenido en función de los datos proporcionados.

## Referencias

* [Calibre](https://calibre-ebook.com/)

