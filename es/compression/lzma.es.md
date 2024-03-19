{
  "date" : "2021-04-08",
  "keywords" :[ "archivo lzma", "formato de archivo lzma", "qué es un archivo lzma", "archivo", "ejemplo de lzma", "extensión de archivo lzma","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - Formato de archivo comprimido LZMA",
  "description":"¿Qué es un archivo LZMA y las API que pueden crear y abrir archivos LZMA?",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## ¿Qué es un archivo LZMA?

Un archivo con la extensión .lzma es un archivo comprimido creado con el método de compresión LZMA (Algoritmo de cadena Lempel-Ziv-Markov). Estos se encuentran/utilizan principalmente en el sistema operativo Unix y son similares a otros algoritmos de compresión como [ZIP](/es/compression/zip/) para minimizar el tamaño del archivo. LZMA es un formato de archivo heredado, que está siendo o ha sido reemplazado por el formato .xz. El tipo MIME del formato .lzma es \`application/x-lzma'. Este formato de archivo fue diseñado por Igor Pavlov para su uso en LZMA SDK.

## Formato de archivo LZMA

El archivo LZMA consta de dos partes principales:

1. Encabezado
1. Datos comprimidos


### Encabezado LZMA

Los archivos LZMA tienen un encabezado de 13 bytes seguido de los datos comprimidos LZMA. El encabezado LZMA consta de:

* Propiedades
* Tamaño del diccionario
* Tamaño sin comprimir

#### Propiedades del encabezado LZMA

El campo Propiedades contiene tres propiedades. Se proporciona una abreviatura entre paréntesis, seguida del rango de valores de la propiedad. El campo consta de

1) el número de bits de contexto literal (lc, [0, 8]);
2) el número de bits de posición literal (lp, [0, 4]); y
3) el número de bits de posición (pb, [0, 4]).

#### Tamaño del diccionario LZMA

Esto se almacena como un entero little endian de 32 bits sin signo con valores que van desde 2^n y 2^n + 2^(n-1). LZMA Utils puede descomprimir archivos con cualquier tamaño de diccionario.

#### Tamaño sin comprimir
El tamaño sin comprimir se almacena como un entero little endian de 64 bits sin signo. Un valor especial de 0xFFFF_FFFF_FFFF_FFFF indica que se desconoce el tamaño sin comprimir. El valor está representado por el marcador de fin de carga útil (\*) si y solo si se desconoce el tamaño sin comprimir.

## Referencias

* [Algoritmo de cadena Lempel–Ziv–Markov](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
