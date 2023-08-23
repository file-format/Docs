{
  "date" : "2019-12-10",
  "keywords" :[ "XLTM", "archivo", "extensión", "formato de archivo", "Excel Open XML Macro", "Hoja de cálculo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tu guía de formato de archivo para saber qué es un archivo XLTM y las API que puedes crear y abrir",
  "title" :"¿Qué es un archivo XLTM?",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## ¿Qué es un archivo XLTM?

La extensión de archivo XLTM representa archivos generados por Microsoft Excel como archivos de plantilla habilitados para macros. Los archivos XLTM son similares a [XLTX](/es/spreadsheet/xltx/) en estructura, excepto que el último no admite la creación de archivos de plantilla con macros. Dichos archivos de plantilla se utilizan para generar y establecer el diseño, el formato y otras configuraciones junto con las macros para facilitar la creación de archivos XLSX similares.

## Breve historia ##

Fue a principios de 2000 cuando Microsoft decidió apostar por el cambio para adaptarse al estándar de **Office Open XML**. Los documentos, de diferentes tipos, bajo este nuevo Estándar fueron identificados agregando "X" en sus extensiones, donde "X" significa XML. En 2007, este nuevo formato de archivo pasó a formar parte de Office 2007 y también se mantiene en las nuevas versiones de Microsoft Office. El nuevo tipo de archivo ha agregado ventajas de tamaño de archivo pequeño, menos cambios de corrupción y representación de imágenes bien formateadas.

## Especificaciones del formato de archivo XLTM ##

Los archivos XLTM se basan en el formato de archivo Office OpenXML y usan XML y [ZIP](/es/compression/zip/) para reducir el tamaño del archivo. Estos se pueden abrir con Microsoft Excel haciendo doble clic en el archivo. La organización de archivos en un formato de archivo XLTM se puede observar cambiando el nombre del archivo a ZIP y luego extrayendo su contenido al disco.

### [Tipos_de_contenido].xml ###

Este es el único archivo que se encuentra en el nivel base cuando se extrae el zip. Enumera los tipos de contenido de las partes dentro del paquete. Todas las referencias a los archivos XML incluidos en el paquete se mencionan en este archivo XML.

### \_rels (Carpeta) ###

Esta es la carpeta Relaciones que contiene un solo archivo XML que almacena las relaciones a nivel de paquete. Los enlaces a las partes clave de los archivos Xltx se encuentran en este archivo como URI. Estos URI identifican el tipo de relación de cada parte clave con el paquete. Esto incluye la relación con el documento principal de Office ubicado como xl/workbook.xml y otras partes dentro de docProps como propiedades principales y extendidas.

### accesorios de documentación ###

Esta carpeta contiene las propiedades generales del documento. Estos incluyen un conjunto de propiedades principales, un conjunto de propiedades extendidas o específicas de la aplicación y una vista previa en miniatura del documento. Un libro de trabajo en blanco tiene dos archivos en esta carpeta, a saber, app.xml y core.xml. El core.xml contiene información como autor, fecha de creación y guardado y modificación. App.xml contiene información sobre el contenido del archivo.

### xl (Carpeta) ###

Esta es la carpeta principal que contiene todos los detalles sobre el contenido del libro. Por defecto, tiene las siguientes carpetas:

* \_rels
* tema
* hojas de trabajo

y siguientes archivos xml:

* estilos.xml
* libro de trabajo.xml

## Referencias ##

* [Formato de archivo MS-XLSX](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

