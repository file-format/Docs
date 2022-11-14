{
  "date" : "2019-10-11",
  "keywords" :[ "archivo bz2", "formato de archivo bz2", "qué es un archivo bz2", "archivo", "ejemplo de bz2", "extensión de archivo bz2","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Formato de archivo comprimido",
  "description":"Aprenda a saber qué es un archivo BZ2 y las API que pueden crear y abrir archivos BZ2",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## ¿Qué es un archivo BZ2?

BZ2 son archivos comprimidos generados con el método de compresión de código abierto [BZIP2](http://www.bzip.org/), principalmente en sistemas UNIX o Linux. Se utiliza para la compresión de un solo archivo y no para archivar varios archivos. Esto contrasta con el formato de archivo TAR en las mismas plataformas que archiva varios archivos en un solo archivo pero sin compresión. Los archivos comprimidos como BZ2 se pueden descomprimir con aplicaciones como [WinZip](https://www.winzip.com/win/en/). BZIP2 utiliza el algoritmo de compresión Run-Length Encoding (RLE) o [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) para lograr altos niveles de compresión.

## Formato de archivo BZ2

No hay especificaciones formales disponibles para este formato de archivo. Sin embargo, [especificaciones de ingeniería inversa] no oficiales (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) muestran que un flujo .bz2 consta de un encabezado de 4 bytes que se sigue por cero o más bloques comprimidos. Es seguido inmediatamente por un marcador de fin de flujo que contiene un CRC de 32 bits para el flujo completo de texto sin formato procesado. No hay relleno entre los bloques comprimidos y todos los bloques están alineados en bits.

## Descomprimir/Extraer Archivo BZ2

Puede descomprimir un archivo BZ2 en Windows y Mac OS usando software como WinZip. En Linux, el siguiente comando en terminal.

```
bzip2 -d filename.bz2
```

## Referencias

* [Especificaciones del formato BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

