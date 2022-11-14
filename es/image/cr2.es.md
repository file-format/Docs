{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo CR2 - Archivo de imagen Canon Raw 2",
  "description":"Obtenga más información sobre el formato de archivo CR2 y las API que pueden crear y abrir archivos CR2",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## ¿Qué es un archivo CR2?

Un archivo CR2 (Camera RAW 2) es un archivo de imagen RAW creado por cámaras digitales Canon. Almacena los datos de imagen sin pérdida originales no procesados capturados por la cámara. El formato de archivo CR2 fue desarrollado por Canon para sus cámaras digitales y puede grabar imágenes de alta calidad de hasta 14 bits de RGB. Esto produce imágenes de alta calidad con suficiente espacio para posprocesamiento. Canon ha utilizado el formato de imagen CR2 en sus modelos de cámara 350D, 20D y 1D. Los archivos CR2 son archivos RAW y contienen información de metadatos adicional, como información de la cámara, información de la lente, información de horquillado, balance de blancos y otras configuraciones.

## Formato de archivo CR2

Los archivos CR2 se almacenan en la tarjeta de memoria de la cámara como archivos binarios en formato de archivo propiedad de Canon. El formato de archivo CR2 reemplazó al formato de archivo CRW utilizado inicialmente y luego fue reemplazado por el formato de archivo Canon RAW 3. El formato de archivo CR2 se basa en las especificaciones [TIFF](/es/image/tiff/) que tiene 4 directorios de archivos de imagen (IFD).

|Compensación |Contenido |Comentario|
---|---|---|
|0x0000 |Encabezado |contiene el orden de los bytes, la versión y el desplazamiento de la imagen RAW|
|calculado |IFD#0 |esta parte contiene la sección Exif, que contiene la sección Makernotes.
Información sobre la imagen #0|
|imagen |computada#0 |versión pequeña de la imagen (una cuarta parte del tamaño de la original), comprimida en Jpeg|
|calculado |IFD#1 |Información sobre la imagen#1.|
|imagen |computada#1 |versión pequeña de la imagen, comprimida en Jpeg|
|calculado |IFD#2 |Información sobre la imagen#2.|
|computado |imagen#2 |versión pequeña de la imagen, no comprimida|
|en el encabezado| EFI#3| Información sobre la imagen #3, la imagen RAW de dimensión completa |
|computed |picture#3 |Datos de imagen RAW, comprimidos sin pérdidas en Jpeg (¡no datos RGB!)|

## Ventaja del formato de archivo CR2

El almacenamiento de imágenes en formato RAW permite una gran cantidad de procesamiento posterior a la fotografía, como el ajuste del balance de blancos. Esto es mucho más difícil y con una gran pérdida de calidad con otros formatos de archivo de imagen como [JPEG](/es/image/jpeg/).

## ¿CR2 es mejor que JPEG?

Los archivos CR2 son archivos sin procesar sin pérdida de datos y, por lo tanto, sin pérdida de calidad. JPEG, por otro lado, es un formato de archivo de imagen con pérdida, ya que pierde algunos datos para reducir el archivo. Por lo tanto, los archivos CR2 son de alta calidad y más adecuados para retoques y mejoras.

## Referencias

* [Formato de archivo CR2](http://lclevy.free.fr/cr2/)

