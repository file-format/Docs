{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Su guía de formato de archivo para saber qué es un archivo _XLSX y las API que pueden crear y abrir archivos _XLSX",
  "title" :"¿Qué es un archivo _XLSX?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## ¿Qué es un archivo _XLSX?

Un archivo con la extensión .\_xlsx es en realidad un archivo [XLSX](/es/spreadsheet/xlsx/) al que otra aplicación le cambia el nombre. Esto puede suceder en ciertos casos cuando el nombre del archivo contiene una extensión . al final del nombre del archivo. Los archivos \_XLSX se pueden abrir en Microsoft Excel de manera similar a los archivos XLSX renombrándolos nuevamente a la extensión .xlsx.

## _Formato de archivo XLSX - Más información

Los archivos _XLSX no son diferentes a los archivos XLSX y utilizan el estándar Open XML adoptado por Microsoft en el año 2000. Antes de XLSX, [XLS](/es/spreadsheet/xls/) era el formato de archivo principal utilizado para trabajar con hojas de cálculo de Excel para guardar documentos. en formato binario. Este nuevo formato de archivo basado en XML vino con ventajas tales como tamaños de archivo pequeños, resistencia a la corrupción de archivos y representación de imágenes bien formateadas. Este nuevo formato de archivo basado en XML pasó a formar parte de Office 2007 y también se lleva a cabo en las nuevas versiones de Microsoft.

## \_Especificaciones del formato de archivo XLSX

Como un archivo \_XLSX es un archivo XLSX renombrado, tiene las mismas especificaciones que el archivo original. Es solo un archivo de almacenamiento que se basa en el formato de archivo de almacenamiento [ZIP](/es/compression/zip/). Si desea ver el contenido de este archivo, simplemente cambie el nombre del archivo a la extensión .zip y extráigalo para ver los archivos constituyentes de este libro de Excel. Un libro de trabajo en blanco, cuando se extrae a sus archivos, tiene los siguientes archivos y carpetas constituyentes.

### [Tipos_de_contenido].xml

Este es el único archivo que se encuentra en el nivel base cuando se extrae el zip. Enumera los tipos de contenido de las partes dentro del paquete. Todas las referencias a los archivos XML incluidos en el paquete se mencionan en este archivo XML.

### \_rels (Carpeta)

Esta es la carpeta Relaciones que contiene un solo archivo XML que almacena las relaciones a nivel de paquete. Los enlaces a las partes clave de los archivos Xlsx se encuentran en este archivo como URI. Estos URI identifican el tipo de relación de cada parte clave con el paquete. Esto incluye la relación con el documento principal de Office ubicado como xl/workbook.xml y otras partes dentro de docProps como propiedades principales y extendidas.

### accesorios de documentación

Esta carpeta contiene las propiedades generales del documento. Estos incluyen un conjunto de propiedades principales, un conjunto de propiedades extendidas o específicas de la aplicación y una vista previa en miniatura del documento. Un libro de trabajo en blanco tiene dos archivos en esta carpeta, a saber, app.xml y core.xml. El core.xml contiene información como autor, fecha de creación y guardado y modificación. App.xml contiene información sobre el contenido del archivo.

### xl (Carpeta)

Esta es la carpeta principal que contiene todos los detalles sobre el contenido del libro. Por defecto, tiene las siguientes carpetas:

* \_rels
* tema
* hojas de trabajo

y siguientes archivos xml:

* estilos.xml
* libro de trabajo.xml

## Referencias

* [MS-XLSX - Formato de archivo .xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

