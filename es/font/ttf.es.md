{
  "date" : "2020-08-20",
  "keywords" :[ "archivo ttf", "formato de archivo ttf", "qué es un archivo ttf", "archivo", "ejemplo ttf", "extensión de archivo ttf","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - Formato de archivo de fuente TrueType",
  "description":"Las fuentes TrueType (TTF) se basan en especificaciones de tecnología de fuentes digitales diseñadas inicialmente por Apple, Inc. Tanto Apple como Microsoft usaban TTF en los sistemas operativos Mac y Windows",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## ¿Qué es un archivo TTF?

Un archivo con la extensión .ttf representa archivos de fuentes basados en la tecnología de fuentes de especificaciones TrueType. Inicialmente fue diseñado y lanzado por Apple Computer, Inc para Mac OS y luego fue adoptado por Microsoft para Windows OS. Las fuentes TrueType brindan una visualización de la más alta calidad en pantallas de computadora e impresoras sin depender de la resolución. Todas las aplicaciones modernas que usan fuentes pueden trabajar con archivos TTF. Los archivos de fuentes TTF están disponibles gratuitamente en Internet y también se pueden convertir a otros formatos de archivos de fuentes, como OTF y WOFF.

## Breve historia

Diseñado por Apply Computer, Inc en la década de 1980 para MacOS, el formato de fuente TTF tenía como objetivo resolver algunas limitaciones técnicas del formato Tipo 1 de Adobe. Apple incluyó soporte para fuentes TrueType en Mac en 1991. El objetivo de diseño detrás de las fuentes TTF era la eficiencia en el almacenamiento y procesamiento, y la extensibilidad. Según esta extensibilidad, las fuentes existentes se pueden convertir al formato TrueType.

Microsoft utilizó por primera vez las fuentes TrueType en Windows 3.1 en abril de 1992 después de que Apple aceptara conceder la licencia de TrueType a Microsoft. Mejoró el mecanismo de rasterización y mejoró su eficiencia y rendimiento.

## Especificaciones del formato de archivo True Type

Un archivo de fuente TrueType es un archivo binario que consta de una secuencia de tablas concatenadas. Cada tabla es una secuencia de palabras y tiene un nombre conocido como `Tag`. Cada etiqueta es del tipo de datos uint32 y consta de cuatro caracteres. La primera tabla en el archivo es el directorio de fuentes que da acceso a otras tablas en el archivo de fuentes. Los datos de fuentes están contenidos en otras tablas seguidas después de la tabla del directorio de fuentes. Dado que se puede acceder a cada tabla por su etiqueta, las tablas pueden aparecer en cualquier orden en el archivo.

Las tablas requeridas y sus nombres de etiquetas se muestran en la siguiente tabla.

|**Etiqueta**|**Tabla**|
---|---|
|'mapa'| mapeo de caracteres a glifos |
|'glifo'| datos de glifos|
|'cabeza'| encabezado de fuente |
|'jeje'| encabezado horizontal|
|'hmtx'| métricas horizontales|
|'loco'| índice de ubicación|
|'maxp'| perfil maximo|
|'nombre'| nombrando|
|'publicar'| Posdata|

### Tipos de datos
Las fuentes TrueType usan el número entero estándar y tipos de datos adicionales como se muestra en la siguiente tabla.

|**Tipo de datos** | **Descripción** |
---|---|
|Fracción corta| fracción con signo de 16 bits |
|Fijo| Número de punto fijo con signo de 16,16 bits|
|FPalabra| Entero con signo de 16 bits que describe una cantidad en FUnits, la distancia medible más pequeña en el espacio em.|
|uFPalabra| Entero sin signo de 16 bits que describe una cantidad en FUnits, la distancia medible más pequeña en el espacio em.|
|F2Punto14| Número fijo de 16 bits con signo y los 14 bits inferiores representan una fracción.|
|fechahoralarga| El formato interno largo de una fecha en segundos desde las 12:00 de la noche del 1 de enero de 1904. Se representa como un entero de 64 bits con signo.|

### Directorio de fuentes

La primera tabla en la fuente TrueType es el directorio de fuentes que proporciona acceso a la información necesaria para acceder a los datos de otras tablas. Consta además de:

* `Subtabla de compensación`: mantiene un registro de las tablas en la fuente y proporciona información de compensación para acceder a cada tabla en el directorio
* `Table Directory` - Contiene entradas para cada tabla en la fuente

#### Subtabla compensada
La subtabla de compensación se muestra a continuación.

|**Tipo**|**Nombre**|**Descripción**|
---|---|---|
|uint32| tipo de escalador| Una etiqueta para indicar el escalador OFA que se utilizará para rasterizar esta fuente; consulte la nota sobre el tipo de escalador a continuación para obtener más información.|
|uint16| numTablas| número de mesas|
|uint16| rango de búsqueda | (potencia máxima de 2 <= numTables)*16|
|uint16| selector de entrada | log2(potencia máxima de 2 <= numTables)|
|uint16| rangoShift| numTables*16-searchRange|

#### Directorio de tablas
El directorio de la tabla viene justo después de la subtabla compensada. Su estructura es como se muestra en la siguiente tabla.

|**Tipo**|**Nombre**|**Descripción**|
---|---|---|
|uint32| etiqueta| identificador de 4 bytes |
|uint32| sumaverificar| suma de comprobación para esta tabla |
|uint32| compensar| desplazamiento desde el comienzo de sfnt|
|uint32| longitud| longitud de esta tabla en bytes (longitud real sin relleno)|

Cada tabla en un archivo de fuente debe tener su propia entrada de directorio de tablas. Las entradas de una tabla deben ordenarse en orden ascendente por etiqueta.


## Referencias
* [Manual de referencia de fuentes TrueType](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [Descripción general de TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

