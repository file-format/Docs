{
  "date" : "2019-11-25",
  "keywords" :[ "archivo jpm", "formato de archivo jpm", "qué es un archivo jpm", "archivo", "ejemplo de jpm", "extensión de archivo jpm","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPM - Formato de archivo compuesto JPEG 2000",
  "description":"Obtenga información sobre el formato de archivo JPM y las API que pueden crear y abrir archivos JPM",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-08"
}

## ¿Qué es un archivo JPM?

JPM se refiere al sistema de codificación de imágenes JPEG 2000, Parte 6, que se utiliza para la creación de imágenes de documentos. Se basa en el estándar de contenido de trama mixto (ISO/IEC 16485) y contiene imágenes fijas en capas que utilizan JPEG 2000 y otras codificaciones. Además de sus propias especificaciones, el formato de archivo JPM hereda características de su padre, es decir, el formato de archivo [jp2](/es/image/jp2/).

## Formato de archivo JPM

El formato de archivo JPM está definido por [ISO/IEC 15444-6:2003](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124) -- la imagen JPEG 2000 sistema de codificación -- Parte 6: Formato de archivo de imagen compuesto. Una imagen compuesta puede contener imágenes escaneadas, imágenes sintéticas o ambas, lo que requiere una combinación de métodos de compresión de tono continuo y de dos niveles. El formato de archivo JPM define un modelo de composición que describe el método de combinación de varias imágenes para generar una imagen compuesta utilizando el modelo de imágenes de contenido de ráster mixto (MRC) de múltiples capas, definido en ITU-T T.44 | ISO/CEI 16485.

### Especificaciones JPM
El estándar de formato de archivo JPM especifica que es un contenedor binario para representar una imagen compuesta mediante la cual varias imágenes se pueden combinar en una sola imagen. Establece el mecanismo para agrupar varias imágenes en una jerarquía de objetos de diseño, páginas y colecciones de páginas para almacenar JPEG 2000 y otros formatos de datos de imágenes comprimidas. El formato incluye el mecanismo de incorporación de metadatos (a menudo denominados metadatos estructurales en proyectos de bibliotecas digitales).

## Referencias

* [Rec. UIT-T. T.805](http://www.itu.int/rec/T-REC-T.805/en)
* [ISO/IEC 15444-6:2013](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124)
* [Wikipedia:JPEG 2000](http://en.wikipedia.org/wiki/JPEG_2000)

