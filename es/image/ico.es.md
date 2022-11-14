{
  "date" : "2019-10-11",
  "keywords" :[ "archivo ico", "formato de archivo ico", "qué es un archivo ico", "archivo", "ejemplo ico", "extensión de archivo ico","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Formato de archivo de imagen",
  "description":"Obtenga información sobre el formato de archivo ICO y las API que pueden crear y abrir archivos ICO",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo ICO?

Los archivos con extensión ICO son tipos de archivos de imágenes que se utilizan como íconos para representar una aplicación en [Microsoft Windows] (https://www.microsoft.com/en-us/windows). Estos vienen en diferentes tamaños, soporte de color y resolución para adaptarse a los requisitos de la pantalla. Otro formato de archivo de imagen similar en Microsoft Windows es [CUR](/es/image/cur/) para la representación del cursor y define un punto de acceso en el encabezado de la imagen. En MacOS, los formatos de archivo ICNS tienen el mismo propósito que los archivos ICO. Varios sitios web en línea, así como aplicaciones, ofrecen la función de crear dichos archivos y convertir otros formatos de imagen como [BMP](/es/image/bmp/), [PNG](/es/image/png/), etc. a un formato de archivo de icono. El tipo de medio de Internet oficial registrado por la IANA para archivos ICO es image/vnd.microsoft.icon.

## Breve historia ##

Los iconos se introdujeron con el lanzamiento de Microsoft Windows 1.0. Estos tenían un tamaño de 32x32 y eran monocromáticos. Con la llegada de win32, se introdujo la compatibilidad con imágenes de iconos en color verdadero con una dimensión de hasta 256x256 píxeles. Windows XP fue el primero en brindar soporte para imágenes de íconos en color de 32 bits, lo que permite agregar al ícono áreas semitransparentes como sombras, suavizado y efectos de vidrio. Microsoft solo recomendó tamaños de íconos de hasta 48 × 48 píxeles para Windows XP. Windows Vista agregó una vista de iconos de 256 × 256 píxeles al Explorador de Windows, así como soporte para el formato comprimido [PNG](/es/image/png/). Con usuarios que utilizan resoluciones más altas y modos de DPI altos, se recomiendan formatos de icono más grandes (como 256 × 256).

## Formato de archivo ICO ##

Un solo archivo ICO consta de una o más de una imagen pequeña de varios tamaños y profundidades de color. La presencia de imágenes de múltiples tamaños es para escalar apropiadamente a diferentes resoluciones de pantalla. Todos los valores en los archivos ICO/CUR se representan en orden de bytes [little-endian](https://en.wikipedia.org/wiki/Little-endian).

El archivo ICO consta de un encabezado de icono, un directorio de iconos,

|Campo|Descripción
---|---|
|Icon Header|Almacena información general sobre el archivo ICO.
|Directorio[1..n]|Almacena información general sobre cada imagen del archivo.
|Icono #1|Los "datos" reales para la primera imagen en el antiguo formato AND/XOR DIB o PNG más reciente
|...|
|Icono #n|Datos de la última imagen del icono

### Encabezado ###

|Desplazamiento|Tamaño (en bytes)|Propósito
---|---|---|
|0|2|Reservado. Siempre debe ser 0.
|2|2|Especifica el tipo de imagen: 1 para imagen de icono (.ICO), 2 para imagen de cursor (.CUR). Otros valores no son válidos.
|4|2|Especifica el número de imágenes en el archivo.

### Directorio ###

El directorio contenido en un archivo ICO, representado como estructura ICONDIR, contiene una estructura ICONDIRECTORY para cada imagen en el archivo. Lo mismo va seguido de un bloque contiguo de todos los datos de mapa de bits de la imagen. Esto es como se muestra a continuación.

|Desplazamiento|Tamaño|Descripción
---|---|---|
|0 (0)|1|Ancho, debe ser 0 si 256 píxeles
|1 (1)|1|Altura, debe ser 0 si 256 píxeles
|2 (2)|1|Recuento de colores, debe ser 0 si hay más de 256 colores
|3 (3)|1|Reservado, debe ser 0
|4 (4)|2|Los planos de color cuando están en formato .ICO, deben ser 0 o 1, o el punto de acceso X cuando están en formato .CUR
|6 (6)|2|Bits por píxel cuando está en formato .ICO, o el punto de acceso Y cuando está en formato .CUR
|8 (8)|4|Tamaño de los datos de mapa de bits en bytes.
|12 (C)|4|Desplazamiento en el archivo.

## Referencias ##

* [ICO - Por Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA-vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

