{
  "date" : "2022-01-23",
  "keywords" :[ "archivo xz", "formato de archivo", "qué es un archivo xz", "archivo", "ejemplo xz", "extensión de archivo xz","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo XZ - Archivo comprimido XZ",
  "description":"Obtenga información sobre el formato de archivo XZ y las API que pueden crear y abrir archivos XZ",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## ¿Qué es un archivo XZ?

XZ es un formato de archivo comprimido que utiliza el algoritmo de compresión LZMA2. Fue diseñado como reemplazo de los populares formatos gzip y bzip2 y ofrece una serie de ventajas sobre estos estándares más antiguos. Los archivos XZ son compatibles con muchas plataformas y se pueden descomprimir rápida y fácilmente. Si bien no son tan comunes como los archivos [ZIP](/es/compression/zip/) o [RAR](/es/compression/rar/), los archivos XZ se pueden usar para almacenar grandes cantidades de datos sin sacrificar la calidad de la compresión. Si necesita comprimir o descomprimir archivos grandes, vale la pena considerar la extensión de archivo XZ.

## Formato de archivo XZ

El archivo XZ se genera y se guarda como archivos binarios en el disco. Utiliza el algoritmo LZMA para comprimir datos y puede lograr una relación de compresión de hasta el 50%. Los archivos XZ se utilizan normalmente para distribuciones de software y archivos de copia de seguridad. Se pueden descomprimir utilizando la utilidad XZ, que se incluye en la mayoría de las distribuciones de Linux.

## Descomprimir archivos XZ en Linux/Unix

Para descomprimir archivos XZ, instale primero el paquete `xz-utils`:
```
$ sudo apt-get install xz-utils
```

Use el comando `unxz` para extraer archivos .xz:
```
$ unxz compressed_xz_file.xz
```

o usando con la opción --decompress de XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Referencias

* [Utilidades XZ](https://en.wikipedia.org/wiki/XZ_Utils)

