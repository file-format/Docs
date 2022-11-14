{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Comprimido", "Archivo", "Extensión", "Formato de archivo", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo LZO",
  "description":"Obtenga información sobre el formato de archivo LZO y las API que pueden crear y abrir archivos LZO",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## ¿Qué es un archivo LZO? ##

Un archivo con la extensión .lzo se combina con funciones de archivado de archivos que pueden reducir el tamaño de todos los archivos en el archivo comprimido. Todos los archivos comprimidos pueden comprender uno o más archivos o incluso grupos de carpetas con varios archivos de diferentes tipos y dimensiones. El tamaño de un archivo comprimido es menor en comparación con el tamaño conjunto de todos los archivos y carpetas almacenados en un archivo comprimido LZO. Todos los archivos comprimidos LZO se almacenan en formato LZO y se ejecutan explícitamente con funciones de compresión utilizadas por el software de compresión y descompresión de archivos LZOP. Todas las especificaciones de compresión se combinan en este programa de compresión y descompresión de archivos que se origina en la biblioteca de compresión de archivos Lempel-Ziv-Oberhume. La velocidad de descompresión más rápida y las relaciones de compresión desarrolladas también se combinan en estos archivos LZO.

## Especificación LZO ##

Markus Franz Xaver Johannes Oberhumer desarrolló el algoritmo "lzop" original, basado en algoritmos anteriores de Abraham Lempel y Jacob Ziv, en 1996. Esta biblioteca implementa una variedad de algoritmos con las siguientes características:

* Compresión más rápida que DEFLATE
* Descompresión rápida
* Búferes adicionales que se necesitan durante la compresión (de 8 KB o 64 KB de tamaño, según el nivel de compresión)
* Los búferes de origen y destino son toda la memoria requerida para la descompresión
* Proporciona control sobre la relación de compresión y la velocidad de compresión

Como algoritmo de compresión de bloques, LZO realiza una compresión superpuesta y una descompresión in situ. Para lograr una compresión superpuesta, el tamaño del bloque de compresión y descompresión debe coincidir. El algoritmo de compresión LZO divide los datos de entrada en coincidencias (un diccionario deslizante) y literales que no coinciden, dando buenos resultados con datos altamente redundantes y resultados aceptables con datos no comprimibles, aumentando solo los datos incompresibles en 1/64 del original Talla.

## Problemas para abrir un archivo LZO ##

Los siguientes son algunos problemas que pueden causar un mal funcionamiento del formato de archivo LZO:
  


* El archivo puede estar corrupto. Para resolver este problema, descargue el archivo nuevamente o solicite al remitente que vuelva a enviar el archivo
* La segunda razón es un archivo infectado, en este caso escanee el archivo correctamente
* Enlaces inadecuados al archivo LZO
* Eliminación de la descripción del LZO
* No hay suficientes recursos de hardware
* Drivers obsoletos del equipo
  


## Referencias ##

* [LZO - Por Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

