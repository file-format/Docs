{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo EDB: un archivo de base de datos de correo de Exchange",
  "description":"Obtenga información sobre el formato de archivo EDB y las API que pueden crear y abrir archivos EDB",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## ¿Qué es un archivo EDB?

Un archivo con la extensión de archivo .edb es una base de datos de buzones creada por Microsoft Exchange Server para almacenar datos relacionados con el correo. EDB, Exchange Database, almacena mensajes que están en proceso y no son SMTP. EDB también se conoce como archivos de base de datos de motor de almacenamiento extensible (ESE) y almacena archivos que utilizan una estructura de árbol b. Al ser archivos de almacenamiento, los archivos EDB se pueden convertir a otros formatos de archivo de almacenamiento de correo, como [PST](/es/email/pst/) y [OST](/es/email/ost/).

## Formato de archivo EDB

No hay especificaciones de formato de archivo EDB abiertas/oficiales disponibles a las que se pueda hacer referencia. Se han logrado algunos avances en la ingeniería inversa del formato de archivo, lo que ha dado como resultado una decodificación de especificaciones parciales. Según estos, un archivo EDB consta de:
* Encabezado del archivo: contiene información del encabezado del archivo de la base de datos
* Páginas de tamaño fijo: contiene la base de datos que consta de tablas e índices

### Encabezado del archivo de la base de datos
El encabezado del archivo de la base de datos reside en la primera página de la base de datos y tiene al menos 668 bytes. El encabezado del archivo contiene `Versión de formato de archivo` y `Tipo de archivo` además de otros campos.

#### Tipos de archivo
|Tipo|Descripción
---|---|
|0| Base de datos|
|1| Streaming|

`Nota:` No se conocen los identificadores de estos tipos.

#### Versión de formato de archivo
El formato original de EDB comenzó en abril de 1997 y siguió evolucionando para los cambios posteriores.

|Fecha de revisión|Versión|Revisión|descripción
---|---|---|---|
|abril 1997| 0x00000620|0x00000000| Sistema operativo original formato Beta.|
|Mayo 1997 |0x00000620|0x00000001| Agregar columnas en el catálogo para indexación condicional y OLD.|
|Jun 1997|0x00000620|0x00000002|Agregue el indicador fLocalizedText en IDB.|
|Oct 1997|0x00000620|0x00000003|Agregue SPLIT_BUFFER a las páginas raíz del árbol espacial.|
|Enero de 1998|0x00000620|0x00000002|Revertir la revisión para que ESE97 siga siendo compatible con versiones posteriores.|
||0x00000620|0x00000003|Agregar nuevas columnas etiquetadas al catálogo ("CallbackData" y "CallbackDependencies").|
|Mayo de 1998|0x00000620|0x00000004|Compatibilidad con valor superlargo (SLV): signSLV, fSLVExists en dbheader.|
|Mayo 1998|0x00000620|0x00000005|Nuevo árbol espacial SLV.|
|Oct 1998|0x00000620|0x00000006|Mapa espacial SLV.|
|Diciembre de 1998|0x00000620|0x00000007|IDXSEG de 4 bytes.|
|Jan 1999|0x00000620|0x00000008|Nuevo formato de columna de plantilla.|
|Jun 1999|0x00000620|0x00000009|Columnas de plantilla ordenadas. Usado en Windows XP SP3|
||0x00000620|0x0000000b|Contiene el encabezado de la página con la suma de comprobación ECC Usado en Exchange|
||0x00000620|0x0000000c|Usado en Windows Vista (SP0)|
||0x00000620|0x00000011|Compatibilidad con páginas de 2 KiB, 16 KiB y 32 KiB. Encabezado de página ampliado con sumas de comprobación ECC adicionales. Compresión de columnas. Sugerencias de espacio. Usado en Windows 7 (SP0)|
|Mayo 1999|0x00000623|0x00000000|Nuevo Administrador de Espacio.|

### Archivos de base de datos

El archivo de la base de datos EDB contiene el esquema de todas las tablas de la base de datos. Además, también incluye registros para todas las tablas de la base de datos e índices para las tablas. Su ubicación está determinada por los siguientes identificadores.

* JetCreateDatabase
* JetCreateDatabase2
* Base de datos JetAttach
* JetAttachDatabase2

En base a esto, el estado de la base de datos se puede evaluar de la siguiente manera.

|Valor|Identificador|Descripción
---|---|---|
|1|JET_dbstateJustCreated|La base de datos se acaba de crear.|
|2|JET_dbstateDirtyShutdown|La base de datos requiere que se ejecute una recuperación total o parcial para que se pueda utilizar o mover. No se debe intentar mover bases de datos en este estado.|
|3|JET_dbstateCleanShutdown|La base de datos está limpia. La base de datos se puede adjuntar sin ningún archivo de registro.|
|4|JET_dbstateBeingConverted|La base de datos se está actualizando.|
|5|JET_dbstateForceDetachInternal|Este valor se introduce en WindowsXP|
 

## Referencias
* [Especificaciones del archivo de base de datos (EDB) del motor de almacenamiento extensible (ESE)] (https://github.com/libyal/libesedb/tree/master/documentation)

