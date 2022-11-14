{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo MDB y las API que pueden crear y abrir archivos MDB",
  "title" :"Formato de archivo MDB: un archivo de base de datos de Microsoft Access",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## ¿Qué es un archivo MDB?

Un archivo con la extensión .mdb es un archivo de base de datos de Microsoft Access que es un Sistema de gestión de bases de datos relacionales (RDBMS). Almacena datos en tablas de bases de datos que están vinculadas entre sí a través de claves primarias y externas. El archivo MDB contiene la estructura completa de las tablas de la base de datos, consultas, procedimientos almacenados. MDB es el formato de archivo predeterminado para Microsoft Access 2003. Las versiones laterales de Microsoft Access utilizan los formatos de archivo [ACCDB](/es/database/accdb/), que es el formato de archivo más reciente hasta la fecha. Los archivos MDB se pueden abrir con aplicaciones como Microsoft Access, MDB Viewer, MDBOpener y se pueden convertir a ACCDB, [CSV](/es/spreadsheet/csv/), formatos de Excel, etc.

## Formato de archivo MDB

Hay especificaciones públicas disponibles para el formato MDB y sigue siendo el formato de archivo propietario de Microsoft. Microsoft, sin embargo, proporciona acceso de conectividad al archivo MDB utilizando el estándar Open Database Connectivity (ODBC) y Visual Basic para aplicaciones (VBA). La guía no oficial de MDB proporciona una breve descripción informal del formato MDB basado en la ingeniería inversa y se puede consultar para conocer las especificaciones.

### Páginas

Según la guía no oficial de MDB, un archivo MDB consta de páginas de tamaño fijo (2048 bytes para Jeb DB3 y 4096 bytes para Jet DB 4). El primer byte indica el tipo de página. Los siguientes son los tipos de página clave:

`Primera página:` Contiene información del encabezado de la base de datos que también incluye la identificación de la versión de Jet DB con la que el archivo es compatible. Además, también incluye información de seguridad de archivos y un mapa de uso de la página.

`Página de definición de tabla:` Una página de definición de tabla especifica columnas, tipos de datos, índice y otra información. Utiliza páginas adicionales si es necesario e incluye un mapa de páginas que contiene los datos de fila para esta tabla.

`Páginas de datos:` Las páginas de datos son los contenedores de datos reales donde los datos se almacenan por filas. Utiliza páginas subsidiarias para almacenar valores de datos largos.

Una única base de datos de Microsoft Access puede estar compuesta por varios archivos que permiten superar las limitaciones de tamaño de archivos y tablas. Esto facilita colocar formularios y código en un archivo MDB de front-end en el escritorio del usuario y datos en otros archivos MDB de back-end en servidores conectados a la red.

## Referencias ##

* [Especificaciones de acceso](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [La guía no oficial de MDB] (http://jabakobob.net/mdb/)

