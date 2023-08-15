{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo ACCDB y las API que pueden crear y abrir archivos ACCDB",
  "title" :"Formato de archivo ACCDB: archivo de base de datos de Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## ¿Qué es un archivo ACCDB?

Un archivo con extensión .accdb es un archivo de base de datos de Microsoft Access 2007 que almacena datos de usuarios en tablas. Es compatible con el almacenamiento
formularios personalizados, consultas SQL y otros datos. Los archivos ACCDB reemplazaron los archivos [MDB](/es/database/mdb/) después de que Microsoft cambió a una estructura de archivos basada en XML. Los archivos ACCDB aún se pueden convertir a MDB con compatibilidad anterior. Sin embargo, ACCDB es el formato de archivo de base de datos de Access ampliamente utilizado ahora. Microsoft también admitió funciones adicionales en formato ACCDB, como la posibilidad de almacenar archivos adjuntos, datos binarios y compatibilidad con campos de valores múltiples.

## Formato de archivo ACCDB

Al igual que MDB, no hay especificaciones públicas disponibles para el formato de archivo ACCDB. Microsoft admite el acceso a estos archivos mediante programación a través del estándar Open Database Connectivity (ODBC) y Visual Basic para aplicaciones (VBA).

### Una visión

Un volcado hexadecimal de un archivo ACCDB simple sugiere que existen similitudes generales en la estructura con las últimas versiones de la familia de formato MDB anterior. Ambos formatos de archivo usan tamaños de página fijos de 4096 bytes. Otra similitud entre ACCDB y MDB es la forma del número mágico, que incluye la cadena "Standard ACE DB" para ACCDB. Una versión o código de compatibilidad está en la misma ubicación en ambos formatos. Las mdbtools | El archivo HACKING indica "Offset 0x14 contiene la versión Jet de esta base de datos" y la Guía MDB no oficial está de acuerdo. La información de estas fuentes, combinada con la entrada de Wikipedia para [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), sugiere que un valor de 0x02 indica ACE 12 (Access 2007) y 0x03 indica ACE 14 (Acceso 2010). Sin embargo, una base de datos mínima creada en Access 2010 y una similar creada en Access 2016 tienen 0x02 en esta ubicación. Una base de datos mínima creada en Access 2016, pero que definía una columna con el tipo de datos "entero grande" recientemente introducido, tenía un valor de 0x05. En los archivos ACCDB, este indicador parece reflejar la compatibilidad del archivo en lugar de la versión del motor ACE utilizado para crearlo.

## Referencias

* [Formato de archivo de acceso](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
* [Especificaciones de Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Motor de base de datos Microsoft Jet](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [¿Qué formato de archivo de Access debo usar?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)
