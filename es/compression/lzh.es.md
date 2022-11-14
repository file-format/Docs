{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Comprimido", "Archivo", "Extensión", "Formato de archivo", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo LZH",
  "description":"Obtenga información sobre el formato de archivo LZH y las API que pueden crear y abrir archivos LZH",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## ¿Qué es un archivo LZH? ##

Un archivo con la extensión .lzh y .lha generalmente se relaciona con el formato de archivo de compresión de archivos. Este formato de archivo es el mismo que otros formatos de compresión de archivos como [ZIP](/es/compression/zip/), [RAR](/es/compression/rar/), etc. El objetivo principal de estos formatos de archivo es reducir el tamaño del formato para enviar fácilmente, así como para mantenerlos juntos en forma comprimida. En comparación con otras compañías occidentales, los archivos LZH son muy populares en Japón y generalmente se usan para comprimir datos de videojuegos. El complemento LZH para Windows 7 está integrado en la versión japonesa de Windows 7. Microsoft lanzó por primera vez el complemento de carpeta Microsoft Compressed (LZH) para la versión japonesa de Windows XP. Este formato de archivo se implementa con disposiciones de compresión y funciones utilizadas por el algoritmo Lempel-Ziv y Haruyasu

## Especificación LZH ##

El método de compresión de un archivo LZH se muestra como una cadena de texto de cinco bytes, como -lz1-. Estos son los bytes tercero a séptimo en el archivo comprimido.

|Especificación|Descripción|
---|---|
|Extensión | .lzh, .lha|
|Tipo de medio| application/x-lzh-compressed|
|Código de tipo| "LHA_" (LHA-ESPACIO)|
|ITU| public.archive.lha|
|Desarrollado por| Haruyasu Yoshizaki (Yoshi)|
|Tipo| Compresión|
|Extendido desde| LArc|

## Problemas para abrir un archivo LZH ##

Los siguientes son algunos problemas que pueden causar un mal funcionamiento del formato de archivo LZH:
  

* El archivo puede estar corrupto. Para resolver este problema, descargue el archivo nuevamente o solicite al remitente que vuelva a enviar el archivo
* La segunda razón es un archivo infectado, en este caso escanee el archivo correctamente
* Enlaces inadecuados al archivo LZH
* Eliminación de la descripción de la LZH
* No hay suficientes recursos de hardware
* Drivers obsoletos del equipo

## Referencias ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
