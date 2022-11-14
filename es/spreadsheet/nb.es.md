{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "archivo", "extensión", "formato de archivo", "Mathematica", "Hoja de cálculo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre las API de archivos NB que pueden crear y abrir archivos NB",
  "title" :"NB - Formato de archivo de cuaderno de Mathematica",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## ¿Qué es un archivo NB?

Un archivo con extensión .nb es un formato de archivo de cuaderno Wolfram que guarda instrucciones para instrucciones matemáticas en un archivo de texto. Puede contener muchos tipos diferentes de datos, como computación en vivo, interfaces dinámicas arbitrarias, entrada de composición tipográfica completa, entrada de imagen, anotación automática de código, una interfaz programática completa de alto nivel y miles de funciones y opciones cuidadosamente organizadas. Las instrucciones textuales son entradas y salidas de Mathematica que se generan y actualizan a medida que las declaraciones de entrada se colocan en el archivo.

## Formato de archivo Wolfram Notebook NB - Más información

Los archivos Wolfram Notebook NB se guardan en formato de texto sin formato, que es un formato de archivo legible por humanos. El contenido de un cuaderno está organizado en secciones como texto sin formato, donde cada una está representada por grupos de celdas, similar a una hoja de cálculo. El rango de estos grupos está definido por un corchete hacia el final de cada celda. El estilo asignado a una celda determina su rol dentro del cuaderno como se detalla a continuación.

### Cuadernos como Wolfram Language

Cuando se pretende guardar el Notebook que consta de instrucciones matemáticas para que Wolfram Language Kernal las ejecute, a las celdas del documento se les asigna automáticamente el estilo de texto "Entrada". Esto le dice al núcleo que las considere como instrucciones que se ejecutan cuando el usuario emite una combinación de teclas `Shift+Return`. Un cuaderno de Mathematica es como se muestra en el siguiente ejemplo.

{{< figure src="../Wolfram Notebook.jpeg" alt="Formato de archivo de cuaderno Wolfram" >}}

### Cuadernos como documentos

Los cuadernos de Mathematica pueden estar en formato de documento para dar una idea de lo que ve y lo que obtiene (WYSIWYG). Estos documentos son los mismos que se ven en la pantalla o en un papel impreso, y son interactivos. Para ello, se asigna el `Estilo de Texto` a la celda para mostrar el contenido sin ejecutar las sentencias del Kernel.

## Exportar cuadernos de Mathematica

Los cuadernos de Mathematica se pueden exportar a muchos formatos de archivo diferentes, como PDF, gráficos, GIS, comprimidos y hojas de cálculo.

## Referencias

* [Conceptos básicos de Mathematica Notebook](https://reference.wolfram.com/language/guide/NotebookBasics.html)

