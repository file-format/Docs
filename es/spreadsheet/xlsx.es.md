{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "archivo", "extensión", "formato de archivo", "Excel", "Hoja de cálculo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre qué es un archivo XLSX y las API que pueden crear y abrir archivos XLSX",
  "title" :"Formato de archivo XLSX - ¿Qué es un archivo XLSX?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## ¿Qué es un archivo XLSX?

**XLSX** es un formato muy conocido para documentos de Microsoft Excel que introdujo Microsoft con el lanzamiento de Microsoft Office 2007. Basado en una estructura organizada de acuerdo con las convenciones de empaquetado abierto, como se describe en la [Parte 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) del estándar OOXML ECMA-376, el nuevo formato es un paquete zip que contiene varios archivos XML. La estructura subyacente y los archivos se pueden examinar simplemente descomprimiendo el archivo .xlsx.

## Breve historia del formato de archivo XLSX

El formato de archivo XLSX se introdujo en 2007 y utiliza el estándar Open XML adaptado por Microsoft en 2000. Antes de XLSX, el formato de archivo común utilizado era [XLS](/es/spreadsheet/xls/) que era un formato de archivo binario puro. El nuevo tipo de archivo ha agregado ventajas de tamaño de archivo pequeño, menos cambios de corrupción y representación de imágenes con buen formato. Fue a principios de 2000 cuando Microsoft decidió apostar por el cambio para adaptarse al estándar de **Office Open XML**. En 2007, este nuevo formato de archivo pasó a formar parte de Office 2007 y también se mantiene en las nuevas versiones de Microsoft Office.

## Especificaciones del formato de archivo XLSX

Las [especificaciones oficiales del formato de archivo XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) están disponibles en línea en Microsoft. Para ver lo que hay dentro del archivo XLSX, simplemente cámbiele el nombre a archivo [ZIP](/es/compression/zip/) cambiando su extensión y luego extráigalo para ver los archivos constituyentes de este libro de Excel. Un libro de trabajo en blanco, cuando se extrae a sus archivos, tiene los siguientes archivos y carpetas constituyentes.

### [Tipos_de_contenido].xml ###

Este es el único archivo que se encuentra en el nivel base cuando se extrae el zip. Enumera los tipos de contenido de las partes dentro del paquete. Todas las referencias a los archivos XML incluidos en el paquete se mencionan en este archivo XML.

### \_rels (Carpeta) ###

Esta es la carpeta Relaciones que contiene un solo archivo XML que almacena las relaciones a nivel de paquete. Los enlaces a las partes clave de los archivos Xlsx se encuentran en este archivo como URI. Estos URI identifican el tipo de relación de cada parte clave con el paquete. Esto incluye la relación con el documento principal de Office ubicado como xl/workbook.xml y otras partes dentro de docProps como propiedades principales y extendidas.

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

## Ejemplo de formato XLSX ##


Para cada hoja de cálculo de Excel contenida en un libro de trabajo, hay un archivo XML. Puede encontrar estos archivos XML en la carpeta xl/worksheets. Toda la información contenida en una hoja de trabajo está organizada en diferentes secciones en el archivo XML. Examinemos una hoja de trabajo de muestra de un libro de trabajo que se muestra en la siguiente imagen.

{{< figure src="../XLSX file format.png" alt="Formato de archivo XLSX" >}}

Como se puede ver, esta hoja de trabajo contiene contenido en las celdas A1 a B2 y una imagen. Además, la celda G13 es actualmente la celda activa en la hoja de trabajo. Ahora, examinemos el archivo xl/worksheets/sheet1.xml para ver cómo se representa esta información en el archivo XML. El contenido de este archivo XML se muestra a continuación.

{{< figure src="../XLSX File Format Details.png" alt="Formato de archivo XPS" >}}

1. La pestaña tiene el color del tema aplicado. Se menciona en el archivo XML con etiqueta.<tabColor> siguiendo la identificación del tema.
1. El valor tabSelected se establece en 1, lo que muestra que esta es la hoja seleccionada
1. Como se puede ver en la primera imagen de arriba, la celda G13 en la hoja de trabajo es una celda activa que también se menciona en el archivo XML.
1. La pestaña sheetData representa los datos contenidos en la hoja de cálculo. Sin embargo, puede ver que el contenido original de la hoja de trabajo no se encuentra en ninguna parte de esta sección. Esto se debe a que el texto se refiere indirectamente desde la hoja XML "sharedStrings". Esta vinculación garantiza que cada texto se guarde solo una vez y se pueda volver a referenciar para ahorrar espacio.
1. La imagen, como se puede ver, está referenciada por el ID de referencia "rId2"

## Contribuir

¿Tiene que compartir algo sobre los formatos de archivo XLSX o de hoja de cálculo? Puede publicar sus hallazgos en la sección [Noticias de formato de archivo de hoja de cálculo](https://news.fileformat.com/t/Spreadsheet).

## Referencias

* [[MS-XLSX] - Formato de archivo XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

