{
  "date" : "2019-10-11",
  "keywords" :[ "archivo tbz", "formato de archivo tbz", "qué es un archivo tbz", "archivo", "ejemplo de tbz", "extensión de archivo tbz","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Archivo de alquitrán comprimido Bzip",
  "description":"Obtenga información sobre el formato de archivo TBZ y las API que pueden crear y abrir archivos TBZ",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## ¿Qué es un archivo TBZ?

Un archivo con extensión .tbz es un archivo comprimido que usa compresión BZIP para reducir el tamaño de los archivos de contenido. Los archivos TBZ son en realidad archivos UNIX [TAR](/es/compression/tar/) comprimidos con BZIP. La compresión de segundo nivel más reciente es [BZIP2](/es/compression/bz2/) que reemplazó a BZIP. El formato de archivo TBZ es adecuado para transferir archivos grandes. Los archivos TBZ se pueden abrir/extraer usando aplicaciones de software como 7-Zip, PeaZip y jZip. Los usuarios de Linux y macOS también pueden abrir una TBZ con el comando BZIP2 desde una ventana de terminal.

## Formato de archivo TBZ

Los archivos TBZ son en realidad archivos comprimidos creados con compresión BZIP/[BZIP2](/es/compression/bz2). No hay especificaciones formales disponibles para este formato de archivo. Sin embargo, [especificaciones de ingeniería inversa] no oficiales (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) muestran que un flujo .bz2 consta de un encabezado de 4 bytes que se sigue por cero o más bloques comprimidos.

## Referencias ##

* [Especificaciones del formato BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

