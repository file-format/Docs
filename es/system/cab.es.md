{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "extensión", "archivo", "formato", "sistema", "Archivo de gabinete de Windows", "Microsoft", "Instalador", "Configuración", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Archivo de gabinete de Windows",
  "description":"Obtenga información sobre el formato de archivo CAB y las API que pueden crear y abrir archivos CAB",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## ¿Qué es un archivo CAB? ##

Un archivo con extensión .cab pertenece a un archivo contenedor de Windows que pertenece a la categoría de archivos del sistema. Es un archivo que se guarda en formato de archivo comprimido en las versiones de Microsoft Windows que admiten algoritmos de datos comprimidos, como [LZX](/es/compression/lzx/), Quantum y [ZIP](/es/compression/zip/ ). El archivo tiene un uso vital cuando un usuario o desarrollador desea contener y compartir datos y archivos de instalación de software. Las funciones de compresión de datos sin pérdidas y la certificación digital incluida en estos archivos hacen que este archivo sea perfecto para almacenar y compartir dichos archivos. Admite diferentes instaladores de Microsoft, como Device Installer, SetUp API y AdvPak.

## Breve historia ##

El archivo CAB es un tipo de archivo de compresión de datos desarrollado por Microsoft. Inicialmente se llamó "Diamante", pero luego se conoció popularmente como archivo CAB, abreviatura de la palabra "Gabinete".

## Especificación técnica ##

Un archivo CAB normalmente puede contener hasta un máximo de 65535 carpetas, que a su vez pueden contener un máximo de 65536 archivos cada una. El mecanismo de almacenamiento de archivos CAB ahorra tiempo y espacio, ya que guarda cada carpeta como un bloque comprimido en lugar de comprimir y almacenar cada archivo por separado. Las carpetas vacías no se pueden almacenar en carpetas de archivos CAB. El archivo CAB fue desarrollado por primera vez por Microsoft y se usa en varios instaladores, como InstallShield con un formato ligeramente diferente. Los archivos CAB están comúnmente conectados a programas autoextraíbles. Los archivos CAB de Microsoft son fácilmente reconocibles debido a su marcador único que ayuda a identificar el formato. El marcador único para todos los archivos CAB de Microsoft es un prefijo de cuatro palabras, MSCF. Al ver este código, un usuario puede distinguir fácilmente un archivo CAB de Microsoft de otros archivos y usarlo en consecuencia en compresores o versiones. Los archivos se pueden comprimir con más datos de instalación de software, o los datos actuales se pueden descomprimir con el software adecuado.


## Ejemplo de cabina ##

El siguiente ejemplo ilustra la relación entre archivos y carpetas en una estructura de archivos CAB:

{{< figure src="../cab.png" alt="Formato de archivo CAB" >}}

## Referencia ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
