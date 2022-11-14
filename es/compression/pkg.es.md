{
  "date" : "2021-04-08",
  "keywords" :[ "archivo pkg", "formato de archivo pkg", "qué es un archivo pkg", "archivo", "ejemplo de pkg", "extensión de archivo pkg","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Formato de archivo de archivo extensible",
  "description":"Obtenga información sobre el formato de archivo PKG y las API que pueden crear y abrir archivos PKG",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## ¿Qué es un archivo PKG?

Un archivo con extensión .pkg es un archivo de paquete de instalación que se usa para instalar software en macOS. Además de las computadoras Macintosh, también se usa en el iPhone. La aplicación de instalación integrada de Apple se puede utilizar para instalar el contenido de un archivo PKG. Un archivo PKG es similar a un archivo MSI utilizado en el sistema operativo Windows para la instalación de software. Durante la instalación, estos archivos de paquete pueden registrar mensajes que le dan una idea de qué elementos adicionales instala este paquete.

## Formato de archivo PKG

PKR son archivos binarios que se comprimen para reducir el tamaño total del archivo. Desde OSX 10.5, Apple ha introducido paquetes planos con archivos de instalación únicos. Estos son diferentes a los formatos de empaquetado anteriores que venían como paquetes en lugar de archivos individuales. Estos paquetes empaquetados contenían una jerarquía de directorios estructurada que almacenaba archivos de una manera que facilitaba su recuperación a través de algún archivo de índice. El formato de archivo PKG plano es en realidad un archivo [XAR](/es/compression/xar/) que tiene:

* Encabezado: define el tamaño, la suma de comprobación y la información de la versión
* Tabla de contenido: un documento XML que está (y debe) estar codificado como UTF-8 y se almacena al principio del archivo, lo que facilita el escaneo a través del archivo para extraer archivos individuales.
* Montón: montón de datos no estructurados a los que hace referencia el TOC

## Referencias

* [Formato de archivo de paquete plano](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

