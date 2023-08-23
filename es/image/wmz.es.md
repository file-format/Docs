{
  "date" : "2019-10-11",
  "keywords" :[ "archivo wmz", "formato de archivo wmz", "qué es un archivo wmz", "archivo", "ejemplo de wmz", "extensión de archivo wmz","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo WMZ - Metarchivo comprimido de Windows",
  "description":"Obtenga información sobre el formato de archivo WMZ y las API que pueden crear y abrir archivos WMZ",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## ¿Qué es un archivo WMZ?

Un archivo con extensión .wmz es una versión comprimida de [WMF](/es/image/wmf/) y se utiliza para almacenar metarchivos. Es un archivo de nivel intermedio generado por versiones anteriores de las aplicaciones de Microsoft Office y no se usa mucho. Los archivos WMZ se generan al guardar documentos en formato [HTML](/es/web/html/). Estos también pueden generarse al enviar por correo electrónico documentos que contienen imágenes prediseñadas incrustadas, ecuaciones, etc. Las aplicaciones que pueden abrir archivos WMZ incluyen (pero no se limitan a) Corel Winzip y Apple Archive Utility.

## Formato de archivo WMZ

Los archivos WMZ están comprimidos [Gzip](/es/compression/gz/) y contienen [WMF](/es/image/wmf/) en su interior. Gzip usa el algoritmo DEFLATE para la compresión del archivo. GZIP es diferente del formato de archivo [ZIP](/es/compression/zip/) ya que aplica un algoritmo de compresión para completar el archivo en lugar de los archivos individuales. El formato de archivo consta de:

* Encabezado de archivo
* Encabezados opcionales
* Datos comprimidos
* Pie de página del archivo

El formato de archivo GZIP [especificaciones versión 4.3](https://datatracker.ietf.org/doc/html/rfc1952) publicado por Internet Engineering Task Force (IETF) contiene información detallada sobre el formato de archivo.

## Referencias

* [RFC1952: especificación de formato de archivo GZIP](https://datatracker.ietf.org/doc/html/rfc1952), por [IETF](https://www.ietf.org)
* [Metaarchivo de Windows - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

