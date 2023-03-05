{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "archivo", "extensión", "formato de archivo", "Excel", "Hoja de cálculo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tu guía de formato de archivo para saber qué es un archivo XLS y las API que puedes crear y abrir",
  "title" :"¿Qué es el formato de archivo XLS? ¡Aprende de los expertos en formato de archivo!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## ¿Qué es un archivo XLS?

Los archivos con extensión XLS representan el formato de archivo binario de Excel. Estos archivos pueden crearse con Microsoft Excel, así como con otros programas de hojas de cálculo similares, como OpenOffice Calc o Apple Numbers. El archivo guardado por Excel se conoce como Libro de trabajo, donde cada libro de trabajo puede tener una o más hojas de trabajo. Los datos se almacenan y muestran a los usuarios en formato de tabla en la hoja de trabajo y pueden abarcar valores numéricos, datos de texto, fórmulas, conexiones de datos externos, imágenes y gráficos. Las aplicaciones como Microsoft Excel le permiten exportar datos de libros de trabajo a varios formatos diferentes, incluidos [PDF](/es/pdf/), [CSV](/es/spreadsheet/csv/), [XLSX](/es/spreadsheet/xlsx/), [TXT](/es/ procesamiento de textos/txt/), [HTML](/es/web/html/), [XPS](/es/page-description-language/xps/) y varios otros. El formato de archivo XLS se reemplazó con un formato más abierto y estructurado, XLSX, con el lanzamiento de Microsoft Excel 2007. Las últimas versiones aún brindan soporte para crear y leer archivos XLS, aunque XLSX es la primera opción de uso ahora.

## Breve historia

XLS fue creado por Microsoft para su uso con Microsoft Excel y también se conoce como formato de archivo de intercambio binario (BIFF). Este tipo de archivo se introdujo por primera vez al hacerlo parte de Excel para Windows en 1987. Las especificaciones del formato de archivo XLS se hicieron públicas por primera vez en junio de 2008 como Revisión 1. Después de eso, las especificaciones se actualizaron continuamente y la última revisión estuvo disponible. es a partir de agosto de 2018 que está marcado como Revisión 8.0. Una breve historia de las diferentes versiones del formato de archivo XLS es la siguiente:

* Versión 7.0 (lanzada con Office 95): esta versión de Excel fue la más robusta y rápida entre todas las versiones y las reescrituras de secuencias internas se actualizaron a 32 bits.
* Versión 8 (lanzada con Office 97): VBA se introdujo como lenguaje estándar y las etiquetas de lenguaje natural eliminadas se incorporaron en esta versión por primera vez. También presentó por primera vez un asistente de oficina con clip para papel.
* Versión 9 (lanzada con Office 2000): solo hubo cambios menores en la versión 9, donde el asistente de oficina con clip para papel podía sostener simultáneamente múltiples objetos que antes no eran posibles.
* Versión 10 (lanzada con Office XP): esta versión no contenía ninguna mejora notable.
* Versión 11 (lanzada con Office 2003): la actualización principal en la versión 11, Excel 2003 fue la introducción de nuevas tablas.

## Especificaciones del formato de archivo XLS ##

Los datos se organizan en un archivo XLS como flujos binarios en forma de un archivo compuesto como se describe en [MS-CFB]. Los datos se almacenan en el archivo compuesto mediante el uso de almacenamientos, flujos y subflujos que contienen información sobre el contenido y la estructura de un libro de trabajo, incluidos los datos del libro de trabajo, como las definiciones de hojas de trabajo. Cada flujo o subflujo contiene una serie de registros binarios. Cada registro binario contiene cero o más campos estructurados que contienen los datos del libro. Esta sección brinda una breve descripción general de la estructura de archivos XLS, pero para obtener especificaciones detalladas de formato de archivo, se deben consultar las [Especificaciones de formación de archivos XLS](https://msdn.microsoft.com/en-us/library/cc313154(v#office .12).aspx) documento de Microsoft.

#### Transmisión y transmisión secundaria ####

Un libro de trabajo está representado por la secuencia del libro de trabajo. Cada hoja de trabajo en un libro de trabajo está representada por subsecuencias. Además, tiene Subflujo de hoja de gráfico, Subflujo de hoja de macro o Subflujo de hoja de diálogo que sigue al Subflujo global. Cada flujo binario o subflujo que contiene datos del libro DEBE escribirse como una serie de registros binarios.

#### Registro ####

La información sobre las características de un libro de trabajo se almacena como un registro que es una secuencia de bytes de longitud variable. Un registro binario consta de los siguientes tres componentes:

**Tipo de registro:** El tipo de registro es un entero sin signo de dos bytes que especifica qué tipo de información especifica el registro y cómo se ordena y estructura la estructura de los datos de registro específicos de este registro. Los valores de tipo de registro DEBEN ser un valor de la Enumeración de registro (sección 2.3) o el registro DEBE hacer uso de la futura arquitectura de registro (sección 2.1.6).

**Tamaño del registro**: el tamaño del registro es un número entero sin signo de dos bytes que especifica el recuento de bytes que especifica el tamaño total de los datos del registro. El tamaño del registro DEBE ser mayor o igual a 0 y DEBE ser menor o igual a 8224.

**Datos de registro:** El componente de datos de registro contiene campos que corresponden a un tipo de registro en particular y comprenden el resto del registro. El orden y la estructura de los campos para un tipo de registro dado se especifican en la sección correspondiente para ese tipo de registro. El tamaño del componente de datos del registro DEBE ser igual al tamaño del registro. Los campos en el componente de datos de registro pueden contener valores simples, matrices de valores, estructuras de varios campos, matrices de campos y matrices de estructuras.

#### Tabla de celdas ####

Las celdas son los bloques fundamentales de un libro de trabajo que almacenan el contenido del libro de trabajo como texto, fórmulas y datos numéricos. Las celdas mantienen el registro de los datos almacenados a través de una estructura de datos llamada Tabla de celdas. La propia tabla de celdas se almacena en la secuencia de registros que se ajustan a las reglas de CELLTABLE definidas en el documento de especificaciones. Consiste en una serie de bloques de filas donde las filas están dispuestas en bloques de filas. Cada bloque de filas contiene filas desde la primera fila que contiene datos hasta la última fila que contiene datos.

El formato de datos o filas se guarda en un registro de Fila para cada bloque de fila. Cada celda que contiene datos o formato de celda individual está representada por un registro. El formato asociado con una celda se puede derivar del formato de celda individual, el formato de fila, el formato de columna o el formato de celda predeterminado. El orden de prioridad para el formato es el formato de celda individual con la prioridad más alta, seguido del formato de fila, luego el formato de columna y luego el formato de celda predeterminado. Las celdas que no contienen datos y no contienen formato individual no se guardan.

#### Fórmulas ####

Una fórmula es una secuencia de valores, referencias de celda, nombres, funciones u operadores en una celda que juntos producen un nuevo valor. Las fórmulas se almacenan en una representación tokenizada conocida como "expresiones analizadas". Una expresión analizada se convierte en una fórmula textual en tiempo de ejecución para su visualización y edición por parte del usuario. Las fórmulas de celda se especifican mediante el registro Fórmula. Las fórmulas de matriz se especifican mediante el registro de matriz. Las fórmulas compartidas se especifican mediante el registro ShrFmla.

#### Gráficos ####

La hoja de gráfico especifica un gráfico, un gráfico que muestra datos o las relaciones entre conjuntos de datos de forma visual, y un caché de datos de gráfico, falta una copia local de los datos que se utilizan en el gráfico o si hay enlaces a datos externos. las fuentes de datos están rotas. El gráfico especifica uno o dos grupos de ejes, un conjunto de ejes contra los que se trazan los datos del gráfico y el conjunto de series, líneas de tendencia y barra de error especificadas en el gráfico. Cada grupo de ejes especifica de uno a cuatro grupos de gráficos que especifican el tipo de visualización utilizada para mostrar los datos. Cada serie, línea de tendencia y barra de error especifica un grupo de gráfico al que está asociado.

#### Metadatos ####

Los metadatos son datos adicionales asociados con una celda en particular o su contenido. Los metadatos se registran en BIFF8 solo con fines de extensibilidad futura.

#### Tablas dinamicas ####

Una tabla dinámica es un mecanismo para resumir los datos de origen para obtener una descripción general de la distribución de esos datos. En una tabla dinámica, las columnas aplicables de los datos de origen se convierten en campos que se pueden usar para resumir datos. Cuando los datos de origen de la tabla dinámica son datos de origen OLAP, las jerarquías OLAP y algunas otras entidades OLAP se convierten en campos de la tabla dinámica.
Una tabla dinámica tiene dos partes principales, una caché dinámica y una vista de tabla dinámica. Puede haber varias vistas de tabla dinámica basadas en una única caché dinámica no OLAP.

#### Estilos ####

Esta descripción general describe cómo se especifica la información de formato y protección para las celdas de una hoja (1). El formato de celda se compone de varios conjuntos de propiedades:

* Propiedades de fuente (negrita, cursiva, color de fuente, tamaño de fuente, etc.)
* Propiedades de relleno (color de primer plano, color de fondo, patrón, degradado, etc.)
* Propiedades de alineación (izquierda, centro, alineación derecha, etc.)
* Propiedades del borde (izquierda, derecha, arriba, abajo, grueso o delgado, color, etc.)
* Propiedades de formato de números (fecha, hora, número de lugares decimales, etc.)
* Propiedades de protección (bloqueadas, ocultas, etc…)

Estas propiedades, en conjunto, describen cómo se muestra e imprime una celda en particular.

## Referencias ##

* [[MS-XLS] - Estructura de formato de archivo binario de Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Formato de archivo binario de archivo compuesto](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

