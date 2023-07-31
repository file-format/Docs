{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "extensión", "archivo", "formato de archivo", "Tipo de archivo BAK", "Extensión de archivo BAK", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo BAK y las API que pueden crear y abrir archivos BAK",
  "title" :"Formato de archivo BAK - Archivo de copia de seguridad de la base de datos",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## ¿Qué es un archivo BAK?

Un archivo con la extensión .bak suele ser un archivo de copia de seguridad que utilizan diferentes herramientas de software para almacenar copias de seguridad de datos. Desde la perspectiva de la base de datos, Microsoft SQL Server utiliza un archivo BAK para almacenar el contenido de una base de datos. Todos los datos y archivos asociados con la base de datos se almacenan en este formato de archivo para recuperarlos en caso de que la base de datos se corrompa o no sea válida por algún motivo. Los archivos de copia de seguridad se pueden almacenar e indexar en otros servidores por motivos de seguridad. Varias aplicaciones pueden crear archivos BAK, como SQL Server Management Studio, Transact-SQL y Windows PowerShell.

## Formato de archivo BAK

Los detalles internos de un archivo BAK no se conocen, pero se supone ampliamente que se basa en el formato de cinta de Microsoft (MTF). Las especificaciones de MTF están disponibles y se pueden consultar para comprender la estructura del archivo. El documento proporciona detalles sobre el almacenamiento MTF para cualquier persona que tenga un conocimiento general sobre las operaciones de administración de almacenamiento, las unidades de cinta y los sistemas de archivos.

### Conjuntos de datos

Un conjunto de datos es una colección de objetos escritos en un medio de almacenamiento (cinta, disco óptico, etc.) durante la copia de seguridad o restauración de datos. Los conjuntos de datos se componen de múltiples medios en caso de un gran volumen de datos.

### Elementos fundamentales de MTF

Un archivo MTF consta de algunos elementos fundamentales que constituyen sus componentes básicos. Estos elementos son:

#### Bloques de descriptores

Los bloques de descriptores (DBLK) se utilizan para controlar el formato y constituyen la base principal de un archivo MTF. Un solo archivo MTF define múltiples DBLK para cada función única. Cada DBLK es un bloque de datos de longitud variable que se divide en las siguientes cuatro partes:

* `Encabezado de bloque común`: estructura de longitud fija que es común a todos los DBLK. Este es el único encabezado de bloque que se requiere.
* `Información de tipo de DBLK`: bloque de longitud fija específico para el tipo de DBLK que se está definiendo
* `Datos del sistema operativo`: datos específicos que se definen según el tipo de DBLK y los sistemas operativos
* `Información de DBLK`: información específica de DBLK de longitud variable que no se puede guardar con la información de DBLK de longitud fija.

 {{< figure src="../bak.png" alt="Formato de archivo de copia de seguridad de Microsoft SQL" >}}

#### Flujo de datos

Los flujos de datos en un archivo MTF se utilizan para encapsular y alinear datos. Se compone de un encabezado de flujo, seguido de los datos de flujo. Un encabezado de flujo puede encapsular solo un único tipo de datos de flujo.

{{< figure src="../bak_datastream.png" alt="Formato de archivo de copia de seguridad de Microsoft SQL" >}}

#### Marcas de archivo

Una marca de archivo se utiliza para la separación lógica y el acceso rápido dentro de un medio. Las marcas de archivo son emuladas por el controlador del dispositivo o mediante el uso del bloque Soft Filemark Descriptor en caso de que el dispositivo utilizado no proporcione marcas de archivo.

## Referencias ##

* [[MS-BCP]: Formato de copia masiva](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5?redirectedfrom=MSDN)

