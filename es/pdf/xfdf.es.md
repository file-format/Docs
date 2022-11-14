{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo XFDF - ¿Qué es un archivo XFDF?",
  "description":"Obtenga información sobre el archivo XFDF y las API que pueden crear y abrir archivos XFDF",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo XFDF?

Un archivo con extensión .xfdf es un formato de datos de formularios XML que se genera con el software Adobe Acrobat. Al igual que [FDF](/es/pdf/fdf/), XFDF contiene la descripción de los elementos del formulario y sus valores en formato XML. Esto puede incluir los nombres y valores de los campos de texto en el formulario PDF. Los XFDF se guardan en formato legible por humanos y se pueden leer programáticamente usando lenguajes de programación como C#.

## Formato de archivo XFDF - Más información

Los archivos XFDF se guardan en formato de archivo XML, que es un formato universal utilizado para importar y exportar datos. Una estructura de archivo XFDF consta de un encabezado, seguido de valores de campo y datos de elementos, como se muestra a continuación.

|Elemento|Atributo|Contenido|
---|---|---|
|\<XFDF> ||Elemento superior|
|\<fields> ||Todos los valores de campo para esta plantilla|
|<field (T)> |nombre |Nombre de campo|
|<value (V)> |valor |Valor del campo|

## Referencias

* [Compatibilidad con el formato FDF de Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroformas.html)
* [Recursos para desarrolladores de Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

