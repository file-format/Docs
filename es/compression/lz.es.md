{
  "date" : "2021-04-08",
  "keywords" :[ "archivo lz", "formato de archivo lz", "qué es un archivo lz", "archivo", "ejemplo lz", "extensión de archivo lz","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Formato de archivo comprimido Lzip",
  "description":"Obtenga información sobre el formato de archivo LZ y las API que pueden crear y abrir archivos LZ",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## ¿Qué es un archivo LZ?

Un archivo con la extensión .lz es un archivo comprimido creado con Lzip, que es una herramienta gratuita de línea de comandos para la compresión. Admite concatenación para comprimir archivos de soporte. Los archivos LZ tienen una aplicación de tipo multimedia/lzip y admiten índices de compresión más altos que [BZ2](/es/compression/bz2/). LZ se basan en el algoritmo LZMA (cadena Lempel-Ziv-Markov) e incluyen una suma de comprobación CRC de 32 bits y bytes de identificación para comprobar la integridad del archivo.

## Formato comprimido LZMA

El formato comprimido LZMA consta de un flujo comprimido de bits que se codifica mediante un codificador de rango binario adaptativo. El flujo se divide en paquetes. Cada paquete describe un solo byte o una secuencia LZ77. La longitud y la distancia de cada paquete se codifica implícita o explícitamente.

Los siete tipos de paquetes son los siguientes ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Código empaquetado (secuencia de bits) |Nombre del paquete |Descripción del paquete|
---|---|---|
|0 + código de bytes| LIT| Un solo byte codificado mediante un codificador de rango binario adaptativo.|
|1+0 + longitud + distancia| PARTIDO| Una secuencia LZ77 típica que describe la longitud y la distancia de la secuencia.|
|1+1+0+0| REPRESENTACIÓN CORTA| Una secuencia LZ77 de un byte. La distancia es igual a la última distancia LZ77 utilizada.|
|1+1+0+1 + largo| REPETICIÓN LARGA[0]| Una secuencia LZ77. La distancia es igual a la última distancia LZ77 utilizada.|
|1+1+1+0 + largo| REPRESENTACIÓN LARGA[1]| Una secuencia LZ77. La distancia es igual a la penúltima distancia LZ77 utilizada.|
|1+1+1+1+0 + largo| REPRESENTACIÓN LARGA[2]| Una secuencia LZ77. La distancia es igual a la tercera distancia LZ77 utilizada por última vez.|
|1+1+1+1+1 + largo| REPRESENTACIÓN LARGA[3]| Una secuencia LZ77. La distancia es igual a la cuarta distancia LZ77 utilizada por última vez.|


## Referencias

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

