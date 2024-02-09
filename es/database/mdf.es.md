{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo MDF y las API que pueden crear y abrir archivos MDF",
  "title" :"Formato de archivo MDF: archivo de base de datos maestra de SQL Server",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## ¿Qué es un archivo MDF?

Un archivo con extensión .mdf es un archivo de base de datos maestro utilizado por [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) para almacenar datos de usuario. Es de suma importancia ya que todos los datos se almacenan en este archivo. El archivo MDF almacena datos de usuarios en bases de datos relacionales en forma de columnas, filas, campos, índices, vistas y tablas. SQL Server permite establecer configuraciones de crecimiento automático y reducción automática para tener un impacto positivo en el rendimiento de la base de datos. Los archivos MDF se pueden cargar y adjuntar a una base de datos utilizando Microsoft SQL Server. Los archivos MDF tienen el tipo mime Application/octet-stream.

## Formato de archivo MDF

La unidad fundamental de almacenamiento de datos en SQL Server es una página. Una página de almacenamiento asignada a la base de datos se divide en páginas lógicas numeradas de 0 a n. Una sola página comienza con un encabezado de 96 bytes que se compone de ID de página, tipo de estructura a la que pertenece la página, número de registros en la página y punteros a las páginas anterior y siguiente.

### Estructura del archivo

Un archivo MDF tiene la siguiente estructura de datos.

* Página 0: Encabezado
* Página 1: Primera PFS
* Página 2: Primer GAM
* Página 3: Primer SGAM
* Página 4: Sin usar
* Página 5: Sin usar
* Página 6: Primer MCD
* Página 7: Primera BCM

#### Encabezado de archivo

La página número 0 de todos los archivos contiene un encabezado que almacena metadatos sobre el archivo.

#### Espacio libre de página (PFS)
PFS identifica el estado de asignación y determina la cantidad de espacio libre.

* Bit 1: Indica si la página está asignada o no.
* Bit 2: Indica si la página es de extensión mixta.
* Bit 3: Indica que esta página es una página IAM.
* Bit 4: Indica que esta página contiene registros fantasma
* Bits 5 a 7: un valor combinado de tres bits, que indica la página completa de la siguiente manera:
* 0: La página está vacía
* 1: la página está llena entre un 1% y un 50 %
* 2: La página está llena en un 51–80 %
* 3: La página está llena en un 81–95 %
* 4: La página está llena en un 96–100 %

## Referencias

* [Archivos de base de datos y grupos de archivos](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Separar y adjuntar base de datos - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [Análisis de la anatomía del archivo de datos de SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

