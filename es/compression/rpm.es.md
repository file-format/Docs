{
  "date" : "2021-04-08",
  "keywords" :[ "archivo rpm", "formato de archivo rpm", "qué es un archivo rpm", "archivo", "ejemplo rpm", "extensión de archivo rpm","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Archivo del administrador de paquetes de Red Hat",
  "description":"Obtenga información sobre el formato de archivo RPM y las API que pueden crear y abrir archivos RPM",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## ¿Qué es un archivo RPM?

Un archivo con extensión .rpm es un paquete del sistema operativo Red Hat Linux para instalaciones de programas en sistemas Linux. Red Hat Package Manager utiliza el formato de archivo RPM y es un sistema de gestión de paquetes gratuito y de código abierto. Aunque los archivos RPM se pueden usar tal cual para la instalación de programas, estos se pueden convertir a otros formatos de paquetes como [DEB](/es/compression/deb/) usando el programa Debian llamado Alien.

## Formato de archivo RPM

Un archivo RPM es un binario que puede contener un conjunto de archivos. La mayoría de las veces, los archivos RPM son "RPM binarios", que son los ejecutables compilados del software. El archivo RPM puede contener RPM de origen (SRPM) que se pueden usar para compilar el paquete a partir del código fuente. El formato de archivo RPM consta de cuatro secciones.

* Lead - Identifica el archivo como un archivo RPM
* Firma: se puede utilizar para garantizar la integridad y/o la autenticidad
* Encabezado: contiene metadatos que incluyen el nombre del paquete, la versión, la arquitectura, la lista de archivos, etc.
* Archivo de archivos: también conocido como carga útil, que suele estar en formato cpio, comprimido con [GZIP](/es/compression/gz/)

## Referencias

* [RPM-Wikipedia](https://rpm.org)
* [Documentación RPM](https://rpm.org/documentation.html)

