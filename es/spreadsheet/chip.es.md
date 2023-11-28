{
"fecha": "2023-03-01",
  "keywords": [
"archivo de chip",
"¿Qué es un archivo de chip?",
"archivo",
"cómo abrir un archivo de chip",
"extensión de archivo de chip",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo CHIP - Archivo de anotación de microarrays",
  "description":"Obtenga más información sobre el formato de archivo CHIP y las API que pueden crear y abrir archivos CHIP.",
"linktitle" :  "CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip",
"parent" : "spreadsheet"
}
},
"lastmod": "2023-03-01"
}

## ¿Qué es un archivo CHIP?

El archivo CHIP es un archivo de anotación de microarrays y está relacionado con el software Gene Set Enrichment Analysis (GSEA). GSEA es un método computacional que evalúa si un conjunto predefinido de genes (un conjunto de genes) muestra diferencias estadísticamente significativas entre dos estados biológicos, como tejido sano versus tejido enfermo o células tratadas con medicamentos versus no tratadas. Para realizar GSEA, necesita un conjunto de datos de expresión genética y una base de datos de conjuntos de genes. La base de datos de conjuntos de genes contiene información sobre los genes de los conjuntos de genes, como su función, vía o expresión específica de tejido.

Un archivo CHIP es un tipo específico de base de datos de conjuntos de genes que utiliza GSEA. Contiene información sobre los genes y conjuntos de genes que son relevantes para la plataforma de microarrays que se utiliza en el experimento. El archivo CHIP proporciona anotaciones para cada sonda en el microarray, como el símbolo del gen, el nombre del gen, la descripción del gen y la ubicación cromosómica. Esta información se utiliza para hacer coincidir las sondas con los genes en el conjunto de datos de expresión genética y asignarlas a los conjuntos de genes apropiados para el análisis GSEA.

Para utilizar un archivo CHIP en GSEA, debe importarlo al software y vincularlo a su conjunto de datos de microarrays. GSEA admite varias plataformas de microarrays y proporciona archivos CHIP prediseñados para muchas de ellas. Sin embargo, también puede crear su propio archivo CHIP utilizando bases de datos de anotaciones de fuentes externas, como NCBI o Ensembl.

## Más información

Un archivo CHIP no es una hoja de cálculo, pero se puede abrir y editar en un programa de hoja de cálculo como Microsoft Excel o Google Sheets. Un archivo CHIP es un tipo de archivo de texto que contiene datos delimitados por tabulaciones, que se pueden importar fácilmente a un programa de hoja de cálculo para verlos y editarlos.

En un programa de hoja de cálculo, puede manipular los datos en un archivo CHIP para agregar, eliminar o modificar anotaciones para los genes y conjuntos de genes en el microarray. Por ejemplo, puede utilizar un programa de hoja de cálculo para agregar anotaciones personalizadas para los genes que no están incluidos en el archivo CHIP original, o para fusionar varios archivos CHIP de diferentes fuentes en un solo archivo.

Sin embargo, es importante tener en cuenta que un archivo CHIP tiene un formato y una estructura específicos que deben mantenerse para que sean compatibles con el software GSEA. Si modifica el contenido de un archivo CHIP en un programa de hoja de cálculo, debe asegurarse de que las modificaciones no alteren el formato o el contenido del archivo de una manera que pueda afectar la precisión o validez del análisis GSEA.

## ¿Cómo abrir el archivo CHIP?

Dado que el archivo CHIP contiene datos delimitados por tabulaciones, si desea ver los datos de la hoja de cálculo, puede abrirlos en Microsoft Excel.

## Referencias
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
