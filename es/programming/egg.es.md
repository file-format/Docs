{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo EGG - Archivo de distribución de Python",
  "description":"Obtenga información sobre el formato de archivo EGG y las API que pueden crear y abrir archivos EGG",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## ¿Qué es un archivo EGG?

Un archivo EGG, también conocido como huevos de Python, es un formato de distribución más antiguo de las distribuciones de Python. Es un archivo comprimido [ZIP](/es/compression/zip/) con extensión .egg y contiene los archivos fuente de la aplicación Python junto con metainformación sobre la distribución. Los archivos EGG son una alternativa a un archivo ejecutable de Windows [EXE](/es/executable/exe/) pero es multiplataforma. Este formato anterior para las distribuciones de Python se reemplazó con el formato de archivo Wheel (WHL) más nuevo a principios de 2010.

## Formato de archivo de huevo

Los archivos EGG se guardan como archivos ZIP comprimidos. Significa que si reemplaza la extensión .egg con .zip, podrá abrirlo con utilidades de descompresión estándar como Corel WinZIP, Microsoft Explorer o RARLAB WinRAR.

Los archivos EGG se pueden crear usando el paquete **distutils** disponible por Python. Otra herramienta que puede crear y abrir archivos EGG es **SetupTools**. Los archivos EGG se pueden instalar como un paquete usando **easy_install**.

`NOTA: el formato de archivo EGG ha quedado obsoleto en favor del nuevo formato de archivo de rueda WHL.`

## Referencia ##

* [HUEVOS de Python](https://python101.pythonlibrary.org/chapter38_eggs.html)

