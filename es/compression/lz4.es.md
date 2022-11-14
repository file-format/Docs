{
  "date" : "2021-04-08",
  "keywords" :[ "archivo lz4", "formato de archivo lz4", "qué es un archivo lz4", "archivo", "ejemplo lz4", "extensión de archivo lz4","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - Formato de archivo comprimido LZ4",
  "description":"Obtenga información sobre el formato de archivo LBR y las API que pueden crear y abrir archivos LZ4",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## ¿Qué es un archivo LZ4?

Un archivo con la extensión .lz4 es un archivo comprimido creado con aplicaciones/utilidades que admiten la compresión [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). El algoritmo LZ4 se centra en el equilibrio entre la velocidad y la relación de compresión. Los archivos LZ4 comprimidos se pueden crear usando la utilidad de línea de comandos LZ4 y se pueden descomprimir usando la misma.

## Formato de archivo LZ4

El formato de archivo LZ4, basado en el algoritmo de compresión LZ4, es independiente del tipo de CPU, el sistema operativo, el sistema de archivos y el conjunto de caracteres. Es adecuado para la compresión de archivos y la compresión de transmisión mediante el algoritmo LZ4. Yann Collet llevó a cabo la implementación inicial del formato LZ4 en lenguaje [C](/es/programming/c/) en 2011 y está disponible para referencia del desarrollador en [Github](https://github.com/lz4/lz4) .

### Formato de cuadro LZ4

La estructura general del formato de archivo LZ4 se muestra a continuación.

|MagicNb|F. Descriptor| Bloque|(...)|Marca final |C. Suma de comprobación|
---|---|---|---|---|---|
|4 bytes| 3-15 bytes||| 4 bytes | 0-4 bytes|

#### Número mágico

4 Bytes, formato Little Endian. Valor: 0x184D2204

#### Descriptor de trama

El descriptor de trama consta de 3 a 15 bytes y es la parte más importante de las especificaciones. Juntos, los campos Magic_Number y Frame_Descriptor se denominan encabezado de trama LZ4 y su tamaño varía entre 7 y 19 bytes. Es como se muestra a continuación.

|FLG| BD| (Tamaño del contenido)| (Identificación del diccionario)| HC|
---|---|---|---|---|
|1 byte| 1 byte | 0 - 8 bytes| 0 - 4 bytes| 1 byte |

#### Bloques de datos

Cada bloque de datos sigue el siguiente orden.

|Tamaño de bloque| datos| (Bloque de suma de comprobación) |
---|---|---|
|4 bytes| |0 - 4 bytes|

#### Marca final

El flujo de bloques finaliza cuando el último bloque de datos va seguido del valor de 32 bits 0x00000000.

#### Suma de comprobación de contenido

Content_Checksum verifica la validez del contenido que se decodifica correctamente y se lleva a cabo utilizando el resultado del algoritmo xxHash-32. Valida los resultados de la transmisión exitosa de todos los bloques en el orden correcto y sin ningún error.

## Referencias

* [Formato de cuadro LZ4](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [Algoritmo de compresión LZ4 - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

