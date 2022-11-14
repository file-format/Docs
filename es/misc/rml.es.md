{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Archivo de plantilla de informe de elixir",
  "description":"Obtenga información sobre el archivo RML y las API que pueden crear y abrir archivos RML",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## ¿Qué es un archivo RML?

Un archivo RML es un archivo de plantilla de informes con el motor de informes [Elixir Repertoire](https://elixirtech.com/repertoire-2/). El archivo de plantilla se utiliza para generar informes con la fuente de datos conectada a Elixir FileSystem. Los datos se leen y completan en el archivo de plantilla RML y se pueden exportar a varios formatos de archivo diferentes, como [PDF](/es/pdf/), [RTF](/es/word-processing/rtf/) y hoja de cálculo [XLS] (/es/hoja de cálculo/xls/). El motor de informes de Elixir Repertoire se puede conectar a una amplia variedad de fuentes de datos JDBC.

## Formato de archivo RML

Los detalles de la estructura de archivo interna del formato de archivo RML no están disponibles públicamente. Los archivos son generados y guardados internamente por la aplicación Elixir Repertoire para generar informes con datos de las fuentes de datos conectadas. El archivo de plantilla RML contiene el diseño general y la información de marcadores de posición del informe final que se generará a partir de los datos.

## ¿Cómo crear un archivo de plantilla RML?

Para generar una plantilla RML en Elixir Repertoire, se pueden seguir los siguientes pasos.

1. Conecte una fuente de datos JDBC al sistema de archivos.
1. Inicie el Asistente para plantillas de informes
1. Use el software para ubicar el archivo .ds de la fuente de datos
1. Elija el informe tabular como opción de exportación
1. Seleccione los campos que se incluirán en la plantilla de informe
1. Finalmente, al hacer clic en el botón Finalizar, First report.rml se agrega al repositorio y se abre para mostrar la pestaña Diseño.

## Referencias

* [Repertorio de Elixir](https://elixirtech.com/repertoire-2/)

