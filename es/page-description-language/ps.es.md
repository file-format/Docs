{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo PS",
  "description":"Obtenga información sobre el formato de archivo PS y las API que pueden crear y abrir archivos PS",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo .PS? ##

PostScript (PS) es un lenguaje de descripción de páginas de propósito general que se utiliza en el negocio de la publicación electrónica y de escritorio. El objetivo principal de PostScript (PS) es facilitar el diseño gráfico bidimensional. La mayoría de los lenguajes requieren una etapa de compilación distinta antes de la ejecución del código, mientras que el formato Post Script (PS) admite una interpretación directa en tiempo de ejecución. Su primera versión define las formas gráficas, diferentes apariencias de texto e imágenes modeladas en páginas impresas o páginas mostradas, siguiendo las reglas del modelo de imágenes de Adobe. Un programa de PS es capaz de intercomunicar una descripción de documento entre un sistema de composición e impresión manteniendo el dispositivo independiente y de alto nivel. Además, este programa también es capaz de gobernar la apariencia de texto y gráficos en una pantalla.

La descripción de la página de PostScript está disponible para renderizarse, mostrarse en la impresora y en otro dispositivo de salida con la ayuda del intérprete de PostScript del dispositivo. Como los comandos para imprimir caracteres, formas gráficas e imágenes son ejecutados por el intérprete, para ese dispositivo específico, la descripción de PostScript de alto nivel se convierte al formato de datos de trama de bajo nivel. Por lo general, diferentes aplicaciones como ilustradores, sistemas de composición de documentos y diseño asistido por computadora (CAD) se automatizan para generar descripciones de página PostScript. Generalmente, los programadores tienen que escribir programas PostScript en el momento de la creación de nuevas aplicaciones. Sin embargo, un programador puede aprovechar las capacidades del lenguaje PostScript que no son accesibles en ninguna aplicación al escribir un programa PS para esa situación especial.

## Breve historia ##

El concepto del lenguaje PostScript fue introducido por primera vez por John Warnock. En 1966 estaba trabajando en un proyecto del puerto de Nueva York. Estaba tratando de desarrollar un intérprete para un gran gráfico tridimensional para la base de datos de ese proyecto. Para procesar estos gráficos, John Warnock concibió el lenguaje Design System. Mientras tanto, Xerox PARC buscaba un medio estándar para definir imágenes de página para su primera impresora láser. Aunque Bob Sproull y William Newman en 1975-76 desarrollaron el formato Press (formato de datos) para controlar las impresoras láser, se necesitaba un lenguaje para una mayor flexibilidad. En 1978, Warnock se unió a Martin Newell en Xerox PARC y reescribió el lenguaje interpretativo, JaM, que luego creció y se extendió al lenguaje Interpress. Warnock fundó Adobe Systems en diciembre de 1982 con Chuck Geschke, Doug Brotz, Ed Taft y Bill Paxton. Comenzaron a trabajar en un lenguaje más simple llamado PostScript similar a Interpress, que se lanzó comercialmente en 1984. Steve Jobs de Apple los visitó y les aconsejó que adaptaran PostScript para manejar impresoras láser.

En marzo de 1985, la primera impresora con un intérprete PostScript integrado fue la LaserWriter de Apple, que revolucionó la autoedición (DTP). La solidez técnica y la amplia disponibilidad hicieron de PostScript, un lenguaje de elección para la publicación electrónica y de escritorio. Durante 1990, un intérprete para el lenguaje PostScript era una parte esencial de las impresoras láser.

## Principales características ##

Las capacidades del lenguaje PostScript para manejar gráficos interactivos y descripción de página poseen las siguientes características:

**Formas:** De naturaleza arbitraria, pueden constar de líneas rectas, curvas, cuadrados y curvas cúbicas que pueden ser tanto autoatravesantes como desconectadas (en secciones y orificios).

**Operadores de pintura:** permiten el contorno de la forma de cualquier grosor, color, relleno o permiten que la forma se dibuje como un recorte para permitir el recorte de cualquier otro gráfico.

**Colores:** tienen diversidad como escala de grises, RGB, CMYK y CIE. Los tipos especiales de colores se modelan como características diferentes: colores directos, mapeo de colores, incluso sombreado y patrones repetidos.

**Texto:** totalmente integrado con gráficos. Además, el modelo de imágenes de Adobe permite que los caracteres de texto se muestren como formas gráficas que pueden ser operadas por cualquier operador gráfico normal.

**Imágenes de muestra**: extraídas de fuentes originales (fotografías escaneadas) o pueden ser producidas sintéticamente. El lenguaje PostScript ofrece diversos medios para regenerar imágenes en cualquier resolución y según diferentes modelos de color en un dispositivo de salida.

Un lenguaje de programación de propósito general puede aprovechar las capacidades gráficas del lenguaje PostScript incorporando Ps en su marco. Los tipos de datos primitivos, como números, caracteres, matrices y cadenas; primitivas de control, como bucles, procedimientos y condicionales; y algunas características no convencionales, como los diccionarios, se especifican en el idioma. Estas características facilitan a los programadores escribir comandos para invocar operaciones de nivel superior. Estas operaciones de alto nivel satisfacen las necesidades de aplicaciones complejas. Tal práctica es más compacta y eficiente en lugar de utilizar un conjunto fijo de operaciones básicas.

Los programas escritos en PostScript se pueden producir, comunicar e interpretar en forma de texto fuente ASCII. Todo el idioma se puede definir en forma de caracteres imprimibles y espacios en blanco. Esta representación ayuda a los programadores a crear, manipular y comprender el lenguaje fácilmente. Además, el almacenamiento y la transmisión de archivos entre diversas computadoras y sistemas operativos se mantuvo conveniente a través de la independencia de la máquina.

Las formas codificadas en binario del lenguaje son posibles, cuando se garantiza que el programa tiene una ruta de comunicación totalmente transparente con el intérprete de PostScript. Adobe recomienda una coherencia estricta con la representación ASCII de los programas PS para el intercambio de documentos o el almacenamiento de archivos.

## Versiones ##

PS(.ps) es la extensión de archivo de un documento PostScript. Los Archivos Nacionales del Reino Unido clasifican cinco versiones cronológicas del archivo PostScript, definidas en la versión DSC: versiones 1.0, 2.0, 2.1, 3.0, 3.1. Cada versión define importantes comentarios de estructuración. El archivo PostScript encapsulado (EPS) es un subtipo especial de archivo PostScript que emplea el lenguaje para especificar un gráfico rectangular. El Manual de referencia del lenguaje PostScript describe un EPS como "Un archivo PostScript encapsulado (EPS) es un programa PostScript que describe como máximo una sola página en un formulario que otras aplicaciones pueden importar para incrustar dentro de un documento contenedor". Un archivo de documento PostScript puede encapsular un archivo EPS en él. Se menciona un uso adicional de PostScript como Display PostScript (DPS). DPS genera gráficos en pantalla a través de un motor de gráficos que utiliza el lenguaje y el modelo de imágenes PostScript.

## Referencias ##

* [Familia de formatos PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

