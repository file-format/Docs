{
  "date" : "2020-03-16",
  "keywords" :[ "Archivo DXF", "Formato de archivo", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo DXF y las API que pueden crear y abrir archivos DXF",
  "title" :"Formato de archivo DXF",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo DXF?

DXF, formato de intercambio de dibujos o formato de intercambio de dibujos, es una representación de datos etiquetados del archivo de dibujo de AutoCAD. Cada elemento en el archivo tiene un número entero de prefijo llamado código de grupo. Este código de grupo en realidad representa el elemento que sigue e indica el significado de un elemento de datos para un tipo de objeto determinado. DXF permite representar casi toda la información especificada por el usuario en un archivo de dibujo.

El formato de archivo DXF fue desarrollado por Autodesk como formato de archivo de datos CAD para la interoperabilidad de datos entre AutoCAD y otras aplicaciones. Por lo tanto, los datos se pueden importar desde otros formatos a DXF a AutoCAD según las especificaciones de interoperabilidad del formato de archivo DXF.

## Breve historia ##


La historia del formato de archivo DXF se remonta a 1982, cuando se introdujo como parte de AutoCAD 1.0. Las versiones iniciales de AutoCAD solo admiten el formato de archivo ASCII de DXF. Con la versión 10 de AutoCAD (y superior) en 1988, se introdujo en AutoCAD la compatibilidad con el formato de archivo ASCII y DXF binario. En las etapas anteriores, Autodesk no compartía ninguna especificación de formato de archivo y, debido a esto, la importación correcta de archivos DXF no era fácil. Sin embargo, Autodesk ahora publica las especificaciones DXF y está disponible para el público en general.

## Especificaciones de formato de archivo ##

El formato de archivo DXF utiliza el código de grupo y los pares de valores para organizar el contenido en secciones. Cada sección se compone de registros donde cada registro consta de un código de grupo y un elemento de datos. Cada código de grupo y valor están en su propia línea en el archivo DXF. Cada sección comienza con un código de grupo 0 seguido de la cadena SECCIÓN. A esto le sigue un código de grupo 2 y una cadena que indica el nombre de la sección (por ejemplo, SECCIÓN1). Cada sección se compone de códigos de grupo y valores que definen sus elementos. Una sección termina con un 0 seguido de la cadena ENDSEC.

El formato de archivo DXF considera objetos diferentes de entidades. Los objetos no tienen representación gráfica aquí, pero las entidades la tienen. Por lo tanto, las entradas en DXF se denominan objetos gráficos, mientras que los objetos se denominan objetos no gráficos. Las secciones BLOQUE y ENTIDADES del archivo DXF contienen Entidades y el uso de códigos de grupo en estas dos secciones es idéntico. El final de una entidad se indica mediante el siguiente grupo 0, que comienza la siguiente entidad o indica el final de la sección.

### Estructura del archivo ###

Las secciones de un archivo DXF se organizan en el siguiente orden:

|Sección|Descripción básica
---|---|
|Encabezado|Esta sección contiene información general sobre el dibujo. Es como la funcionalidad de Configuración en su teléfono, que contiene las diferentes variables asociadas con el dibujo y sus valores asociados. Por ejemplo, la sección Encabezado definirá qué versión de AutoCAD usa el archivo DXF (la variable $ACADVER) o la unidad utilizada para medir ángulos en el archivo (la variable $AUNITS)
|Clases|La sección CLASES contiene la información de las clases definidas por la aplicación cuyas instancias aparecen en las secciones BLOQUES, ENTIDADES y OBJETOS de la base de datos.
|Tablas|Esta sección contiene definiciones para varias tablas diferentes, cada una de las cuales contiene varias entradas de símbolos diferentes. Por ejemplo, el [tipo de línea](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/AutoCAD-Core/files/GUID-20B4D4B3-1220-426A- 847B-5BBE36EC6FDF-htm.html) (LTYPE) define el patrón de guiones, puntos, texto y símbolos en el archivo DXF y cómo se escalan. Aquí hay una lista completa de las tablas que se encuentran en esta sección:<ul><li> Tabla de ID de aplicación (APPID)</li><li> Tabla de registro de bloques (BLOCK_RECORD)</li><li> Tabla Estilo de cota (DIMSTYPE)</li><li> Tabla de capas (LAYER)</li><li> Tabla de tipo de línea (LTYPE)</li><li> Tabla de estilos de texto (STYLE)</li><li> Tabla del sistema de coordenadas de usuario (UCS)</li><li> Ver (VER) tabla</li><li> Tabla de configuración de ventana gráfica (VPORT)</li></ul>
|Bloques|Esta sección contiene los objetos gráficos y las entidades de dibujo que forman cada referencia a bloque en el dibujo.
|Entidades|Esta sección contiene los datos reales del objeto y las entidades gráficas del dibujo. Esto puede incluir datos sin procesar; por ejemplo, una entidad circular se define por su grosor, el punto central, su radio y la dirección de extrusión.
|Objetos|Aquí encontrará las partes no gráficas del dibujo. Por ejemplo, los diccionarios de AutoCAD se almacenan aquí.

## Referencias ##

* [Especificaciones del archivo DXF](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF de Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

