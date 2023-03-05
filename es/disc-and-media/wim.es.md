{
  "date" : "2021-08-11",
  "keywords" :[ "archivo wim", "formato de archivo wim", "qué es un archivo wim", "archivo", "ejemplo de wim", "extensión de archivo wim","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo WIM y las API que pueden crear y abrir archivos WIM",
  "title" :"WIM - Archivo de formato de imágenes de Windows",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## ¿Qué es un archivo WIM?
Los archivos con extensiones .wim se vieron por primera vez en Windows Vista. El WIM pertenece a un formato de imágenes basado en archivos que normalmente se introdujo en Microsoft Windows Vista. Permite implementar una sola imagen de disco en varias plataformas informáticas. Los archivos WIM se utilizan para administrar archivos como actualizaciones, controladores y componentes sin reiniciar la imagen del sistema operativo. Un archivo WIM AQ contiene un conjunto de archivos y metadatos asociados que es muy similar a otros formatos de archivo de disco.

## formatos de archivo WIM
El formato de archivo WIM no es como los formatos basados en sectores como VHD o IS, de hecho, está basado en archivos, lo que significa que la unidad fundamental de información en un WIM es un archivo. El beneficio básico de estar basado en archivos es el almacenamiento de una sola instancia de un archivo al que se hace referencia varias veces en el árbol del sistema de archivos y la independencia del hardware. Reduce la sobrecarga de abrir y cerrar varios archivos individualmente, porque los archivos se almacenan dentro de un solo WIM expediente. Los archivos WIM pueden almacenar múltiples imágenes de disco, a las que se hace referencia por su nombre único o por su índice numérico.
### Soporte para algoritmos de compresión
WIM admite las siguientes familias de algoritmos de compresión en velocidad descendente y proporción ascendente:
-XPRESS
- LZX
- LZMS
- Sólido-compresión.
Las tres primeras familias están basadas en LZ77, mientras que la compresión sólida se introdujo junto con LZMS en WIMGAPI Windows 8 y DISM Windows 8.1.
### Herramientas para formato de archivo WIM
Las siguientes herramientas suelen admitir el formato de archivo WIM:

- **ImageX**: una herramienta de línea de comandos utilizada para editar, crear e implementar imágenes de disco de Windows en el formato de imágenes de Windows. Junto con el WIMGAPI relevante, se distribuye como parte del kit de instalación automatizada de Windows gratuito. A partir de Windows Vista, el programa de instalación de Windows utiliza la API de WAIK para instalar Windows.
- **DISM**: una herramienta introducida en Windows 7 y Windows Server 2008 R2 que puede realizar tareas relacionadas con el servicio en una imagen de instalación de Windows, ya sea una imagen en línea o una imagen sin conexión dentro de una carpeta o un archivo WIM. esta herramienta fue capaz de montar y desmontar imágenes, agregar un controlador de dispositivo a una imagen sin conexión y consultar los controladores de dispositivo instalados en una imagen sin conexión.
 




## Referencias


* [Formato de imágenes de Windows - por Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


