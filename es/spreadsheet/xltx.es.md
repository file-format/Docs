{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "archivo", "extensión", "formato de archivo", "Excel Open XML", "Hoja de cálculo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tu guía de formato de archivo para saber qué es un archivo XLTX y las API que puedes crear y abrir",
  "title" :"¿Qué es un archivo XLTX?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## ¿Qué es un archivo XLTX?

Los archivos con la extensión .xltx representan archivos de plantilla de Microsoft Excel que se basan en las especificaciones de formato de archivo de Office OpenXML. Se utiliza para crear un archivo de plantilla estándar que se puede utilizar para generar archivos [XLSX](/es/spreadsheet/xlsx/) que muestran la misma configuración que se especifica en el archivo XLTX.

## Breve historia

Fue a principios de 2000 cuando Microsoft decidió apostar por el cambio para adaptarse al estándar de **Office Open XML**. Los documentos, de diferentes tipos, bajo este nuevo Estándar fueron identificados agregando "X" en sus extensiones, donde "X" significa XML. En 2007, este nuevo formato de archivo pasó a formar parte de Office 2007 y también se mantiene en las nuevas versiones de Microsoft Office. El nuevo tipo de archivo ha agregado ventajas de tamaño de archivo pequeño, menos cambios de corrupción y representación de imágenes bien formateadas.

## Especificaciones del formato de archivo XLTX

Los archivos XLTX se basan en el formato de archivo Office OpenXML y usan XML y [ZIP](/es/compression/zip/) para reducir el tamaño del archivo. Fue creado con el lanzamiento de Microsoft Office 2007 para reemplazar el formato de archivo XLT binario. Similar a XLTX, el formato de archivo XLT se puede usar para crear archivos [XLS](/es/spreadsheet/xls/) usando Microsoft Excel 2003 y 2007. Estos se pueden abrir con Microsoft Excel haciendo doble clic en el archivo. La organización de archivos en un formato de archivo XLTX se puede observar cambiando el nombre del archivo a ZIP y luego extrayendo su contenido al disco.

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

* [[MS-XLSX] - Formato de archivo .Xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

