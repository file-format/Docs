{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Base de datos Btrieve" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo BTR y las API que pueden crear y abrir archivos BTR",
  "title" :"BTR - Archivo de base de datos Btrieve",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## ¿Qué es un archivo BTR?

Un archivo con extensión .btr es un archivo de base de datos creado por la aplicación de base de datos transaccional [Btrieve](https://www.actian.com/). A diferencia de los sistemas de administración de bases de datos relacionales (RBMS), Btrieve se basa en el método de acceso secuencial indexado (ISAM), que es una forma de almacenar datos para una recuperación rápida. El archivo BTR almacena una colección de registros y se utiliza para generar informes según los requisitos. Los archivos BTR se pueden abrir con Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility y Legend Software BTRIEVE Viewer.

## Estructura del archivo BTR: más información

La estructura de datos internos y la alineación de cada byte en la estructura de un archivo BTR no están disponibles públicamente. Sin embargo, Btrieve
proporciona la [API de Btrieve](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) que se puede usar para leer la información de los archivos BTR. Es compatible con los siguientes lenguajes de programación y entornos de desarrollo.

* Embarcadero C/C++
* Embarcadero Delfos
* GNU C/C++
* Micro Foco COBOL
*Microsoft Visual Basic
*Microsoft Visual C++
* Watcom C/C++

La recuperación de datos de un archivo BTR depende del archivo DDF asociado. Sin el DDF, no será fácil recuperar la información de dicho archivo.

## Referencias

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Introducción a las API de Btreive](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

