{
  "date" : "2020-08-20",
  "keywords" :[ "archivo otf", "formato de archivo otf", "qué es un archivo otf", "archivo", "ejemplo otf", "extensión de archivo otf","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - Formato de archivo de fuente TrueType",
  "description":"Obtenga información sobre el formato de archivo OTF y las API que pueden crear y abrir archivos OTF",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## ¿Qué es un archivo OTF?

Un archivo con extensión .otf se refiere al formato de fuente OpenType. El formato de fuente OTF es más escalable y amplía las características existentes de los formatos [TTF](/es/font/ttf/) para tipografía digital. Desarrollado por Microsoft y Adobe, OTF combina las características de los formatos de fuente PostScript y TrueType. Esto hace que el formato OTF se adapte a la mayoría de los sistemas de escritura y es por eso que se usa uniformemente en las principales plataformas informáticas. El formato de fuente OpenType es compatible con Mac OS X y Windows 2000 y versiones posteriores.

## Breve historia

El requisito de fuentes OpenType se originó como un requisito para un formato de fuente más expresivo que pudiera manejar tipografía fina. Además, tenía como objetivo cumplir con los requisitos de comportamiento complejo de muchos de los sistemas de escritura del mundo. Microsoft intentó licenciar la tecnología tipográfica avanzada de Apple, conocida como Tipografía GX, a principios de la década de 1990. Esto no salió bien y, como resultado, Microsoft comenzó a mejorar su propia tecnología de fuente TrueType en 1994. Las modificaciones también incluyeron la introducción de un formato de fuente más adecuado que también cumple con las características de los formatos de fuente Type 1 (PostScript) de Adobe.

Adobe, en 1996, se unió a Microsoft en sus esfuerzos por reemplazar tanto el TrueType de Apple como su propio formato de fuente Type 1. Esto resultó en la combinación de ambos formatos de fuentes subyacentes para superar las limitaciones y agregar nuevas extensiones. Esta nueva tecnología se introdujo el mismo año con el nombre **OpenType**.

## Especificaciones del formato de archivo OTF

Las especificaciones OTF están disponibles públicamente por Microsoft y se pueden consultar desde la perspectiva del desarrollador. Al igual que TTF, utiliza la misma estructura de contenedor 'sfnt' y es compatible con las especificaciones de TrueType. Los datos dentro de un archivo de fuente OpenType se utilizan para diferentes propósitos, como calcular el diseño del texto, definir glifos como contornos TrueType o Compact Font Format (CFF), proporcionar mapas de bits monocromáticos o en color o documentos SVG como descripciones alternativas de glifos e información de metadatos.

### Tipos de datos OTF
Los archivos OTF utilizan los siguientes tipos de datos, todos en Big Endian.

|Tipo de datos| Descripción|
---|---|
|uint8| Entero sin signo de 8 bits.|
|int8| Entero con signo de 8 bits.|
|uint16| Entero sin signo de 16 bits.|
|int16| Entero con signo de 16 bits.|
|uint24| Entero sin signo de 24 bits.|
|uint32| Entero sin signo de 32 bits.|
|int32| Entero con signo de 32 bits.|
|Fijo| número de punto fijo con signo de 32 bits (16.16)|
|FALDA| int16 que describe una cantidad en unidades de diseño de fuente.|
|UFPALABRA| uint16 que describe una cantidad en unidades de diseño de fuente.|
|F2DOT14| Número fijo con signo de 16 bits con los 14 bits bajos de fracción (2.14).|
|FECHAHORALARGA| Fecha y hora representadas en número de segundos desde las 12:00 de la noche del 1 de enero de 1904, UTC. El valor se representa como un entero de 64 bits con signo.|
|Etiqueta| Matriz de cuatro uint8 (longitud = 32 bits) utilizada para identificar una tabla, un eje de variación de diseño, un script, un sistema de lenguaje, una función o una línea base|
|Desplazamiento16| Desplazamiento corto a una tabla, igual que uint16, desplazamiento NULL = 0x0000|
|Desplazamiento32| Desplazamiento largo a una tabla, igual que uint32, desplazamiento NULL = 0x00000000|
|Versión16Punto16| Valor empaquetado de 32 bits con números de versión principales y secundarios. (Consulte Números de versión de la tabla).|

### Directorio de tablas OTF

Un archivo OTF comienza con un directorio de tabla. Este directorio es la colección de nivel superior de las tablas en el archivo de fuente. Dependiendo de la cantidad de fuentes en un archivo, el directorio de la tabla puede estar ubicado en una ubicación diferente en el archivo. Por ejemplo, en caso de que el archivo de fuente tenga solo una fuente, el directorio de la tabla comienza en el byte 0 del archivo. En el caso de varias colecciones de fuentes OpenType,
el comienzo del directorio de la tabla se indica en TTCHeader.

|Tipo |Nombre |Descripción|
---|---|---|
|uint32 |versión sfnt| 0x00010000 o 0x4F54544F ('OTTO')|
|uint16| numTables |Número de tablas.|
|uint16| searchRange |Potencia máxima de 2 menor o igual que numTables, multiplicado por 16 ((2\**floor(log2(numTables))) * 16, donde “**” es un operador de exponenciación).|
|uint16 |entrySelector Log2 de la potencia máxima de 2 menor o igual a numTables (log2(searchRange/16), que es igual a floor(log2(numTables))).|
|uint16 |rangeShift |numTables multiplicado por 16, menos searchRange ((numTables * 16) - searchRange).|
|tableRecord| tableRecords[numTables] |Array de registros de tabla: uno para cada tabla de nivel superior en la fuente|


### Registro de tabla

Para cada tabla de nivel superior en la fuente, hay un registro de tabla que consta de los siguientes campos.

|Tipo| Nombre| Descripción|
---|---|---|
|Etiqueta| etiqueta de tabla | Identificador de tabla.|
|uint32| suma de control| Suma de comprobación para esta tabla.|
|Desplazamiento32| compensar| Desplazamiento desde el principio del archivo de fuentes.|
|uint32| longitud Longitud de esta tabla.|

Cada tabla en el archivo de fuente OpenType está representada por nombres conocidos como etiquetas de tabla. Es imprescindible que todos los registros de la matriz se ordenen en orden ascendente por etiqueta.

## Referencias
* [Especificaciones de fuentes OpenType de Microsoft](https://docs.microsoft.com/en-us/typography/opentype/spec/overview)
* [Descripción general de TrueType](https://docs.microsoft.com/en-us/typography/truetype/)

