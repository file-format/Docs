{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo MDF y las API que pueden crear y abrir archivos NDF",
  "title" :"Formato de archivo NDF - Archivo de base de datos maestra de SQL Server",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## ¿Qué es un archivo NDF?

Un archivo con extensión .ndf es un archivo de base de datos secundario utilizado por [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) para almacenar datos de usuario. NDF es un archivo de almacenamiento secundario porque el servidor SQL almacena los datos especificados por el usuario en un archivo de almacenamiento principal conocido como [MDF](/es/database/mdf/). El archivo de datos NDF es opcional y está definido por el usuario para administrar el almacenamiento de datos en caso de que el archivo MDF principal use todo el espacio asignado. Por lo general, se almacena en un disco separado y puede extenderse a múltiples dispositivos de almacenamiento. La presencia de archivos MDF es necesaria para abrir archivos NDF.

## Formato de archivo NDF

El formato de archivo NDF no es diferente de [MDF](/es/base de datos/mdf) y usa páginas como la unidad fundamental de almacenamiento de datos. cada página comienza con un encabezado de 96 bytes que incluye:

* ID de página
* Tipo de Estructura
* Número de registros en las páginas
* Punteros a las páginas anteriores y siguientes

### Estructura del archivo NDF

Un archivo MDF tiene la siguiente estructura de datos.

* Página 0: Encabezado
* Página 1: Primera PFS
* Página 2: Primer GAM
* Página 3: Primer SGAM
* Página 4: Sin usar
* Página 5: Sin usar
* Página 6: Primer MCD
* Página 7: Primera BCM

#### Encabezado del archivo NDF

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

## Página de archivo de datos

Las páginas en un archivo de datos de SQL Server comienzan desde cero (0) y se incrementan secuencialmente. Cada archivo es reconocido por un número de identificación de archivo único. El par de ID de archivo y número de página identifica de forma única una página en una base de datos. Un ejemplo que muestra los números de página en una base de datos es como en la siguiente imagen.

{{< figure src="../ndf.png" alt="Formato de archivo de base de datos NDF" >}}

Este ejemplo muestra los números de página en una base de datos que tiene un archivo de datos principal de 4 MB y un archivo de datos secundario de 1 MB.

## Referencias

* [Archivos de base de datos y grupos de archivos](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [Separar y adjuntar base de datos - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Análisis de la anatomía del archivo de datos de SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

