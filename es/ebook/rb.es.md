{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "dispositivo Rocket eBook de Nuvo Media", "archivo", "extensión", "formato", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo RB para el dispositivo Rocket eBook de Nuvo Media y las API que pueden crear y abrir archivos RB",
  "title" :"RB - Archivo de libro electrónico Rocket",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## ¿Qué es un archivo RB?

El archivo con extensión .rb contiene el contenido del libro electrónico Rocket. El Rocket eBook es en realidad un dispositivo fabricado por Nuvo Media; lanzaron este dispositivo en 1998. Aunque Rocket eBook es capaz de mostrar imágenes, pero solo en pantalla en blanco y negro. Tiene una pantalla de 106 ppp o 480 x 320 píxeles en una pantalla táctil de 4,5 x 3 pulgadas. El libro electrónico Rocket se conecta a una computadora a través de una conexión de puerto serie para descargar libros electrónicos en formato de archivo RB. Los archivos RB pueden usar DRM, pero esta tecnología no se usa en los libros electrónicos modernos. El archivo RB convencionalmente contiene un archivo HTML con las imágenes y un archivo pseudo-OPF con todos los metadatos (.info).

## Especificación técnica del formato de archivo RB ##

Aparece un número mágico (en hexadecimal) en los primeros 4 bytes del archivo: B0 0C B0 0C.

Parece que los siguientes dos bytes son un número de versión, como "02 00", que significa versión principal 2 y versión secundaria 0.

Los siguientes cuatro bytes contienen el texto "NUVO", seguido de 4 bytes de 00h.

Los siguientes 4 bytes son la fecha de creación del libro, codificados como int16. Esto nos pone en el desplazamiento 0Eh. La versión anterior de ORocketLibrary codificaba el valor total del año (es decir, 1999 era "CF 07", 2000 era "D0 07"). En la versión reciente, tm_year se almacena literalmente, es decir, 100 para el año 2000 ("64 00"). Después del año viene un int8 que representa el número de mes relativo a 1 y un int8 que representa el día del mes.

Los siguientes 6 bytes son 00h. Para el ajuste de tiempo, estos pueden reservarse.

El desplazamiento absoluto de la "Tabla de contenido" está contenido en un int32 en el desplazamiento 18h.

Después de esto, hay un int32 que contiene la longitud del archivo .rb. Esto se utiliza para determinar si los archivos están completos o no.

Todo este fragmento de bytes (20h a 128h) parece ser necesario solo para un título que está encriptado. En títulos no cifrados, siempre son cero.

En la mayoría de los casos, sigue la tabla de contenido (en el desplazamiento 128). Comienza con un recuento int32 del número de entradas de "página" (secciones de archivo .rb) en la ToC. Cada entrada consta de un nombre (rellenado con ceros hasta 32 bytes), seguido de 3 int32: la longitud del segmento de datos, la posición en el archivo .rb y un indicador para esta entrada. A día de hoy, los valores conocidos son: 1 (cifrado), 2 (página de información) y 8 (desinflado). Todos los nombres se adaptan, según sea necesario, para garantizar que todos sean únicos.

## Referencias

* [E-Reader - Por MobileRead](https://en.wikipedia.org/wiki/E-reader)

