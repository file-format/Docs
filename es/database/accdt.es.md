{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo ACCDT y las API que pueden crear y abrir archivos ACCDT",
  "title" :"ACCDT: formato de archivo de base de datos de plantillas de Microsoft Access 2007",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## ¿Qué es un archivo ACCDT?

Un archivo con extensión .accdt es un archivo de plantilla de base de datos de Microsoft Access que contiene elementos de base de datos predefinidos. Estos elementos son una colección de estructuras que definen las aplicaciones de una base de datos, como los esquemas de la base de datos para almacenar datos, la descripción del diseño para las vistas de los datos y los metadatos que describen la base de datos. Al ser archivos de plantilla, los archivos ACCDT se pueden usar para crear bases de datos basadas en la configuración de plantilla disponible en estos. Los archivos de base de datos resultantes se guardan como archivos [ACCDB](/es/database/accdb/) y se rellenan con datos en tablas. Microsoft Access 2007 y posteriores pueden abrir archivos ACCDT.

## Formato de archivo ACCDT

Los archivos de plantilla ACCDT se basan en las especificaciones de Office Open XML y todos los datos están contenidos en un paquete ZIP. La información sobre la estructura y el contenido de la base de datos se encuentra en los archivos [XML](/es/web/xml/) y archivos de texto y se vinculan entre sí a través de relaciones. Puede cambiar el nombre de un archivo ACCDT a la extensión [.zip](/es/compression/zip/) y usar cualquier software de compresión para extraer el contenido del archivo ZIP.

### Estructura del archivo

Los archivos ACCDT son paquetes que contienen una colección de partes relacionadas. Cada **parte** almacena información sobre el contenido de una aplicación de base de datos utilizando formatos XML, de texto y binarios, que incluye:

* Objetos de base de datos
* Metadatos asociados
* Estructura del paquete

#### Paquete

Un paquete es un archivo [ZIP](/es/compression/zip/) que contiene varias partes y cumple con las convenciones de empaquetado abierto especificadas en [ISO/IEC-29500-2](https://go.microsoft.com/fwlink/ ?LinkId=150883). Los archivos ACCDT deben contener al menos una parte de metadatos de plantilla que debe ser el objetivo de una relación. Esta plantilla de metadatos es la parte inicial de un archivo ACCDT.

#### Parte

Una parte es un flujo de bytes que tiene un tipo asociado para especificar la naturaleza y el tipo de contenido almacenado en él. La enumeración de partes especifica partes válidas, tipos de contenido válidos y relaciones requeridas entre todas las partes en un paquete.

#### Relación

`Relación del paquete`: donde el destino es una parte y el origen es el paquete como un todo.

"Relación de parte a parte": donde el destino es una parte y el origen es una parte del paquete.

`Relación explícita`: cuando se hace referencia a un recurso desde el contenido de una parte de origen al hacer referencia a un elemento de relación por el valor de su atributo ID.

`Relación implícita`: una relación que no es explícita.

`Relación interna` - donde el objetivo es una parte del paquete.

`Relación externa` - donde el objetivo es un recurso externo que no está en el paquete.

## Referencias ##

* [Formato de archivo de plantilla de acceso](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

