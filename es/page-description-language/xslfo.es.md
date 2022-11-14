{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "Objetos de formato XSL", "Archivo", "Extensión", "Formato de archivo", "Lenguaje de hoja de estilo extensible"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Obtenga información sobre el formato de archivo XSLFO y las API que pueden crear y abrir archivos XSLFO",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## ¿Qué es un archivo XSL-FO? ##

XSL-FO (XSL Formatting Objects) es un poderoso lenguaje de hojas de estilo para formatear documentos XML. La semántica de la forma limitada de papel e impresión se expresa mediante XSL-FO cuando las dimensiones son fijas. A diferencia de HTML, que representa la semántica de la forma ilimitada de una ventana de navegador con dimensiones variables. Los documentos XML formateados por XSL-FO se utilizan principalmente para generar archivos PDF. XSL (Extensible Stylesheet Language) es un conjunto de tecnologías W3C con funciones completas destinadas a diseñar para formatear e intercambiar documentos XML y XSL-FO como parte de este lenguaje. XSLT y XPath también son otras partes de XSL.

Se propone que los documentos XML se transformen primero en XSL-FO, PDF es un ejemplo de este criterio. En PDF, los resultados se procesan primero con XSLT y luego con el formateador XSL-FO. De esta manera, los documentos XML se pueden formatear aleatoriamente. Aunque XSL-FO aprovecha la ventaja de utilizar las propiedades de la hoja de estilo en cascada (CSS) y extenderlas donde sea necesario para el formato real, alberga la provisión de plantillas de página denominadas páginas maestras en la terminología de XSL-FO. XSL-FO también proporciona formato para documentos bastante sofisticados y admite la generación de índices.

## Historia y Conceptos Básicos ##

En enero de 2012 se actualizó por última vez el Borrador de Trabajo de XSL-FO y en noviembre de 2013 se cerró su Grupo de Trabajo. Una hoja de estilo XSL especifica la presentación de una clase de documentos XML al describir cómo una instancia de la clase se transforma en un documento XML que usa el vocabulario de formato. XSL-FO es un lenguaje de presentación integrado y no tiene marcas semánticas que se usan en HTML. Además, este lenguaje almacena todos los datos del documento dentro de sí mismo, a diferencia de CSS, que altera la configuración predeterminada de un documento HTML o XML externo.

El criterio general de uso de XSL-FO es que el usuario escribe un documento en un lenguaje XML en lugar de escribir en FO. Después de eso, se produce una transformación XSLT. Esta transformación XSLT es responsable de la conversión de XML en XSL-FO. Tan pronto como se genera el documento XSL-FO, se entrega a una aplicación llamada procesador FO. Los procesadores de FO son responsables de transformar este documento en un documento legible e imprimible. Los archivos PDF o PS son ejemplos de la salida más común de XSL-FO. Pero eso no significa que el procesador FO solo pueda producir estos dos tipos de formato como salida. Algunos procesadores FO pueden generar archivos RTF o incluso puede aparecer una ventana en la GUI del usuario, esta ventana muestra la secuencia de la página y su contenido.

Un documento XSL-FO es diferente de un PDF o un PS en el sentido de que, en última instancia, no define el diseño del texto en diferentes páginas. Tal vez, da estilo a las páginas y determina los lugares para mostrar los contenidos. Además, un procesador FO organiza el texto dentro de los límites especificados por el documento FO. Esta especificación incluso permite que diferentes procesadores de FO se comporten de acuerdo con las páginas creadas resultantes. Un ejemplo de este comportamiento es la separación silábica, pocos procesadores FO pueden separar palabras para ahorrar espacio cuando se rompe una línea, mientras que algunos procesadores no seleccionan esta opción. Depende de los procesadores elegir diferentes algoritmos de división de palabras que se ajusten a sus requisitos. Estos algoritmos de separación de palabras pueden ser muy simples o quizás más complejos. En algunas situaciones, la especificación XSL-FO sanciona explícitamente a los procesadores FO, cierto grado de elección en el contexto del diseño.

Esta variación entre los procesadores de FO genera resultados variados, sobre los cuales los procesadores a menudo no se preocupan. Porque el enfoque general de XSL-FO es producir documentos paginados/impresos. Los propios documentos XSL-FO normalmente actúan como intermediarios, su función principal es generar archivos PDF o un documento que se puede imprimir como salida para distribuir. En HTML/CSS o XSL-FO, distribuir el PDF como resultado final en lugar de ingresar el lenguaje de formato indica que los receptores no se ven afectados por la versatilidad resultante que se produce debido a las diferencias entre los intérpretes del lenguaje de formato. Por otro lado, es evidente que no existe una manera fácil de que un documento pueda satisfacer las diferentes necesidades de los destinatarios, por ejemplo, tamaño de página variable o tamaño de fuente deseado, o adaptación a la página o impresión.

## Formato de archivo XSLFO ##

Los documentos SL-FO son básicamente documentos XML, pero no siguen ningún esquema. En su lugar, los documentos SL-FO siguen la sintaxis definida en la especificación de su propio lenguaje. Hay dos secciones requeridas en cada documento XSL-FO:

1. Una sección que especifica una lista de diseños de página etiquetados.
1. Una sección con todos los detalles de los datos del documento, con marcado, que determina la visualización de contenidos en diferentes páginas a través de varios diseños de página.

Las propiedades de la página se mencionan en los diseños de página, que pueden definir la organización del texto, para cumplir con las convenciones del idioma específico. Además, el tamaño de la página, sus márgenes y las secuencias de páginas (que sancionan diferentes propiedades para las páginas pares e impares) también están definidos por los diseños de página.

La porción de datos del documento se divide en una serie de flujos, donde cada flujo está conectado a un diseño de página. Los flujos encierran una lista de bloques en ellos. Esta lista de bloques puede contener funciones de marcado en línea o una lista de datos de texto, o tal vez ambos al mismo tiempo. Los márgenes del documento también pueden mostrar los números de página o los títulos de los capítulos. La funcionalidad tanto de los bloques como de los elementos en línea sigue siendo la misma que en el CSS, aunque algunas reglas de margen y relleno son diferentes entre FO y CSS.

La dirección de orientación de la página está completamente especificada para la extensión de bloques y líneas, lo que hace que los documentos FO funcionen en idiomas diferentes al inglés. El lenguaje de la especificación de FO utiliza las palabras inicio y fin en lugar de izquierda y derecha para la descripción de las direcciones. El marcado de contenido básico y las reglas en cascada de XSL-FO se toman de CSS. El lenguaje de XSL-FO está de acuerdo con las siguientes especificaciones.

## Múltiples columnas ##

Una página puede tener varias columnas y bloques y puede extenderse de una columna a otra de forma predeterminada. Se permite que varias páginas tengan diferentes anchos y números de columnas. Todas las características de FO siguen los límites de una página de varias columnas.

### Listas ###

Una lista XSL-FO se establece mediante dos conjuntos de bloques dispuestos lado a lado. Conceptualmente, en una lista, un bloque a la izquierda indica un número, una viñeta o una cadena de texto, mientras que el bloque del lado derecho puede funcionar como se esperaba. La numeración de las listas XSL-FO generalmente la realiza el XSLT.

### Mesas ###

Una tabla FO es similar a una tabla HTML/CSS. El usuario puede seleccionar las filas de datos, información de estilo, color de fondo para cada celda individual. Usando información de estilo distinta, el usuario tiene el privilegio de seleccionar la primera fila como fila de encabezado de tabla. El procesador de FO puede ser informado explícitamente sobre la especificación de espacio de cada columna, o para autoajustar el texto en la tabla.

### Indexación ###

XSL-FO 1.1 tiene funciones que ayudan a generar un índice al hacer referencia a elementos marcados correctamente.

### Beneficios ###

* Apropiado para publicación basada en contenido
* Facilidad de uso
* Bajo costo

## Referencias ##

* [¿Qué es XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [Objetos de formato XSL](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

