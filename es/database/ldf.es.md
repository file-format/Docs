{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo LDF y las API que pueden crear y abrir archivos LDF",
  "title" :"LDF: formato de archivo de la base de datos maestra de SQL Server",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## ¿Qué es un archivo LDF?

Un archivo con la extensión .ldf es un archivo de registro mantenido por Microsoft SQL Server, que es un sistema de administración de bases de datos relacionales (RDBMS). Todas las transacciones realizadas en los archivos de la base de datos principal ([MDF](/es/database/mdf/)) (como inserción, actualización, eliminación) se registran en el archivo LDF. Los archivos LDF son componentes críticos de cualquier base de datos. En caso de falla del sistema, el archivo de registro se usa para restaurar la base de datos a un estado consistente. El archivo de registro de transacciones puede aumentar de tamaño si las transacciones no se confirman por completo. Los archivos LDF se pueden abrir con la aplicación de software Microsoft SQL Server.

## Operaciones registradas en archivo LDF

Un archivo de registro SQL registra las siguientes operaciones:

* El comienzo y el final de cada transacción.

* Cada modificación de datos de datos (insertar, actualizar o eliminar). Esto también incluye los cambios realizados por los procedimientos almacenados del sistema o las declaraciones del lenguaje de definición de datos (DDL) en cualquier tabla, incluidas las tablas del sistema.

* Cada asignación o desasignación de extensión y página.

* Crear o eliminar una tabla o índice.

## Formato de archivo LDF

El archivo LDF consta de registros de transacciones de SQL Server que se organizan como una cadena de registros. Cada entrada de registro tiene un número de secuencia de registro (LSN) que es mayor que el LSN del registro anterior. Las cadenas se concatenan una tras otra en el archivo. Debido a las modernas computadoras de alta velocidad, se pueden insertar registros donde existe el LSN2 en el archivo de registro antes del LSN1. Dado que las operaciones se registran en una serie, el cambio descrito por LSN2 se realizó después del registro de registro LSN1. Los registros de una transacción en particular se vinculan hacia atrás mediante punteros que se utilizan y aceleran la reversión de la transacción.
 

## Referencias

* [Archivos de base de datos y grupos de archivos](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Guía de administración y arquitectura de registros de transacciones](https://docs.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- servidor-ver15)

