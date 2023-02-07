{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo ZST - Formato de archivo comprimido Zstandard",
  "description":"Obtenga más información sobre el formato de archivo ZST y las API que pueden crear y abrir archivos ZST",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## ¿Qué es un archivo ZST?

Un archivo ZST es un archivo comprimido que se genera con el algoritmo de compresión Zstandard (zstd). Es un archivo comprimido que se crea con compresión sin pérdidas por el algoritmo. Los archivos ZST se pueden usar para comprimir diferentes tipos de archivos, como bases de datos, sistemas de archivos, redes y juegos. El estándar Z se rige por [RFC 8878] (https://www.rfc-editor.org/rfc/rfc8878) que describe el mecanismo de compresión general, el tipo de medio y la codificación de contenido.

## Formato de archivo ZST

Los archivos ZST se almacenan en formato de archivo comprimido en el disco. El mecanismo de compresión es como se describe en RFC 8878 que deja obsoleto a RFC 8478.

## Marcos ZST

Un archivo ZST consta de uno o más fotogramas. Cada cuadro puede ser un cuadro estándar Z o un cuadro saltable. Un marco Zstandard contiene datos comprimidos, mientras que un marco saltable contiene metadatos de usuario personalizados.

### Marco estándar Z

Un marco Zstandard tiene la siguiente estructura.

|Campo|Tamaño en Bytes|
---|---|
|Número_mágico |4 bytes|
|Frame_Header |2-14 bytes|
|Bloque_de_datos |n bytes|
|[Más bloques de datos] ||
|[Content_Checksum] |4 bytes|

### Marco saltable

Un marco saltable permite la inserción de metadatos definidos por el usuario en un flujo de marcos concatenados. La estructura de un marco saltable es la siguiente.

|Número_mágico |Tamaño_del_cuadro |Datos_del_usuario|
---|---|---|
|4 bytes |4 bytes |n bytes|

## Referencias ##

* [Compresión Zstandard RFC 8878](https://www.rfc-editor.org/rfc/rfc8878)

