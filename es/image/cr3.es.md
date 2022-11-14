{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo CR3 - Archivo de imagen Canon Raw 3",
  "description":"Obtenga más información sobre el formato de archivo CR3 y las API que pueden crear y abrir archivos CR3",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## ¿Qué es un archivo CR3?

Un archivo CR3 es un formato de archivo de imagen RAW de Canon creado por cámaras digitales Canon seleccionadas. Fue presentado por Canon para reemplazar el formato de archivo CR2 y es utilizado por algunos de los dispositivos digitales de Canon. Los archivos CR3 almacenan los datos de imagen sin pérdida originales no procesados capturados por la cámara. El uso de estas imágenes en bruto proporciona imágenes de alta calidad y deja mucho espacio para editar a los fotógrafos. Además de los datos de la imagen principal, los archivos CR3 también almacenan información de metadatos sobre la imagen.

## Formato de archivo CR3

Los archivos CR3 se almacenan en el disco como un archivo binario en el formato de archivo de medios base ISO (ISO/IEC 14496-12) y también incluyen [etiquetas de Canon] personalizadas (https://exiftool.org/TagNames/Canon.html#uuid). También incluye el [códec 'crx' de Canon](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) que es una combinación de JPEG-LS (Rice-Golomb + RLE codificación) y JPEG-2000 (LeGall 5/3 DWT + cuantificación).

## Etiquetas personalizadas CR3

Los archivos CR3 contienen etiquetas personalizadas para diferentes propósitos. Algunas de estas etiquetas son las siguientes.

|ID de etiqueta| Nombre de la etiqueta| Escribible |Valores / Notas|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Etiquetas Canon CCTP|
|'CMT1' |IFD0| - |--> Etiquetas EXIF|
|'CMT2' |ExifIFD| - |--> Etiquetas EXIF|
|'CMT3' |Cañón de notas de creador| - |--> Etiquetas Canon|
|'CMT4' |Información GPS| - |--> Etiquetas GPS|
|'CNCV' |Versión del compresor| no| |
|'CNOP' |CanonCNOP| - |--> Etiquetas Canon CNOP|
|'CNTH' |CanonCNTH| - |--> Etiquetas Canon CNTH|
|'THMB' |Imagen en miniatura| no| |

## Referencias

* [Formato de archivo CR2](http://lclevy.free.fr/cr2/)
* [Etiquetas de Canon](https://exiftool.org/TagNames/Canon.html#uuid)

