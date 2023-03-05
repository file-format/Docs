{
  "date" : "2019-12-09",
  "keywords" :[ "archivo zl", "formato de archivo zl", "qué es un archivo zl", "archivo", "ejemplo zl", "extensión de archivo zl","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - Formato de archivo comprimido ZLIP",
  "description":"Obtenga información sobre el formato de archivo ZL y las API que pueden crear y abrir archivos ZL",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## ¿Qué es un archivo ZL?

Un archivo con extensión .zl es un formato de archivo comprimido ZLIP que utiliza una variante del algoritmo de compresión DEFLATE para comprimir archivos. Es independiente del tipo de CPU, el sistema operativo, el sistema de archivos y el conjunto de caracteres y, por lo tanto, se puede utilizar para el intercambio de información. Las especificaciones técnicas de la compresión ZLIP están disponibles en el [sitio de IETF](https://tools.ietf.org/html/rfc1950) y se pueden consultar desde la perspectiva del desarrollador.

## Formato de archivo ZL

Una secuencia zlib tiene la siguiente estructura:

* `CMF (Método de compresión y banderas)`: este byte se divide en un método de compresión de 4 bits y un campo de información de 4 bits según el método de compresión.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Método de compresión)` - Identifica el método de compresión utilizado en el archivo. Sus valores y el método de compresión correspondiente son los siguientes.

| Valor CM| Compresión|
|---|---|
|CM = 8|DEFLATE con un tamaño de ventana de hasta 32K|
|CM = 15|Reservado|

* `CINFO (Información de compresión)` - Para CM = 8, CINFO es el logaritmo en base 2 del tamaño de la ventana LZ77, menos ocho (CINFO=7 indica un tamaño de ventana de 32K).

* `FLG (FLaGs)`: este byte de bandera se divide de la siguiente manera:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Referencias ##

* [Especificaciones del formato de archivo Zlib](https://tools.ietf.org/html/rfc1950)

