{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "archivo", "extensión", "formato", "eBook", "Libro digital" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo LRF y las API que pueden crear y abrir archivos LRF",
  "title" :"Formato de archivo LRF: un archivo de lector portátil de Sony",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## ¿Qué es un archivo LRF?

Un archivo con la extensión .lrf es un archivo de libro electrónico de banda ancha (BBeB) que contiene datos para un BBeB de Sony, incluidos texto, imágenes y datos de paginación. El archivo se guarda en un formato binario comprimido que contiene un encabezado, un número específico de objetos y un índice de objetos. Los archivos LRF y LRX incluyen los dos formatos de libro BBeB disponibles. Los archivos LRF no están encriptados y se pueden compilar a partir de archivos [LRX](/es/ebook/lrf/). Los archivos LRF se pueden convertir desde varios otros tipos de archivos, incluidos PDF y HTML. Si su computadora no puede abrir el archivo LRF, entonces probablemente no tenga instalado el software para abrir o editar los archivos LRF. Los programas que pueden abrir archivos LRF son Calibre, BookDesigner, Makelrf y Canon Book Creator para Windows, Calibre para Linux, Calibre y Sony Reader para Macintosh.

## Breve historia

El tipo de archivo LRF está asociado ante todo con Line Rider por [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). El Line Rider es un juguete de física de Internet y fue inventado en septiembre de 2006 por un estudiante universitario esloveno, Boštjan Čadež. Los lectores electrónicos de libros electrónicos de la marca Sony (como los lectores Sony PRS-500 y Sony Librie) utilizan la extensión de archivo LRF para sus documentos y textos. Este tipo de archivo propietario ahora está obsoleto, al igual que los archivos LRS y LRX relacionados. Esos tres tipos de archivos componían el libro electrónico de banda ancha (BBeB), que se suspendió en 2010 cuando Sony comenzó a vender sus libros electrónicos en formato EPUB.

## Formato de archivo LRF

Las especificaciones detalladas del formato de archivo LRF están disponibles en [archivo web] (https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Un archivo LRF consta de:
* un encabezado
* varios objetos
* un índice de objetos.

Todos estos valores están en orden Intel (LSB primero).

### Encabezado LRF

|Desplazamiento (hexadecimal) |Tamaño (bytes) |Nombre/significado| Valor de ejemplo|
---|---|---|---|
|0 |8| Firma LRF| 4C 00 52 00 46 00 00 00 = "LRF" en Unicode|
|8 |2| versión?| 999 en la mayoría de los archivos|
|A |2| "Psuedo-Cifrado" |byte de clave 48|
|0C |4| IDObjetoRaíz| 0x0044|
|10 |8| NúmeroDeObjetos |342|
|18 |8| DesplazamientoÍndiceObjeto| 0x00093440|
|20 |4| desconocido| 0|
|24 |1| Banderas| (16 - de atrás hacia adelante, 1 = de adelante hacia atrás) 16|
|25 |1| desconocido |(¿relleno?) 0|
|26 |2| desconocido| 1600|
|28 |2| desconocido| (¿relleno?) 0|
|2A |2| Altura?| 600|
|2C |2| Ancho?| 800|
|2E |1| desconocido| 24|
|2F |1| desconocido |(¿relleno?) 0|
|30 |0x14| desconocido| ceros|
|44 |4| Id. de objeto solo del objeto PlaneStream (0x1E) | 0x0042|
|48 |4| desconocido |0x1536|
|4C |2| Tamaño de compilación XML | 0x035C|


## Referencias

* [Formato de archivo LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - Por Wikipedia](https://en.wikipedia.org/wiki/BBeB)

