{
  "date" : "2020-08-20",
  "keywords" :[ "archivo cff2", "formato de archivo cff2", "qué es un archivo cff2", "archivo", "ejemplo cff2", "extensión de archivo cff2","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Formato de archivo de fuente compacta versión 2",
  "description":"Obtenga más información sobre el formato de archivo CFF2 y las API para crear y abrir archivos CFF2",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## ¿Qué es un archivo CFF2?

El formato de archivo CFF2 es la versión 2.0 del formato de archivo CFF y permite el almacenamiento eficiente de contornos de glifos y metadatos similares al formato de archivo CFF. CFF2 se diferencia de CFF en que está diseñado para usarse en el contexto de una fuente OpenType como una tabla 'sfnt' con la etiqueta CFF2. No se puede utilizar como un programa independiente y depende de los datos de otras tablas OpenType.

## Formato de archivo CFF2

Las [especificaciones de formato de archivo CFF2](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2) contienen detalles sobre el diseño de datos internos, tipos de datos, tablas y otra información interna sobre el formato de archivo. Se puede referir para referencia del desarrollador. Algunos de los detalles acerca de estos son los siguientes.

### Diseño de datos

Los datos binarios del formato de archivo CFF2 se organizan lógicamente como una serie de estructuras de datos separadas. El diseño dentro de los datos binarios es como se muestra en la siguiente tabla.

|Entrada |Comentarios|
---|---|
|Encabezado |Ubicación fija|
|Arriba DICT| Ubicación fija|
|ÍNDICE Global Subr| Ubicación fija|
|Variación |Tienda|
|FDSelect |Presente sólo si hay más de una fuente DICT en el ÍNDICE de fuentes DICT.|
|Fuente DICT ÍNDICE ||
|Matriz de fuente DICT| Incluido en Font DICT INDEX.|
|DICT Privado| Uno por Fuente DICT.|

Solo las primeras tres estructuras se basan en ubicaciones fijas. El resto se alcanza a través de compensaciones, y su ordenación se puede cambiar.

### Tipos de datos

El formato de archivo CFF2 utiliza los siguientes tipos de datos.

|Nombre |Rango |Descripción|
---|---|---|
|uint8 |0 a 255 |número sin signo de 8 bits|
|uint16 |0 a 65535| Número sin signo de 16 bits |
|uint32 |0 a 4294967295| Número sin signo de 32 bits |
|Compensación |varía| Desplazamientos de 1, 2, 3 o 4 bytes (especificados por el campo OffSize en una tabla de índice) |
|Tamaño reducido |1 a 4| El número sin signo de 1 byte especifica el tamaño de un campo o campos de compensación |

Almacena todos los datos numéricos de varios bytes y los campos de compensación en orden de bytes big-endian. El formato CFF2 está libre de bytes de relleno ya que no respeta ninguna restricción de alineación.

### Datos DICT

Los archivos CFF2 contienen los datos del diccionario de fuentes como pares clave-valor en un formato tokenizado compacto. Las claves del diccionario se codifican como operadores de 1 o 2 bytes y los valores del diccionario se codifican como operandos numéricos de tamaño variable. Hay tres estructuras que utilizan el formato de datos DICT: `Top DICT`, `Font DICT` y `Private DICT`. Se definen varios tipos de operandos enteros de diferentes tamaños y se codifican como se muestra en la siguiente tabla (el primer byte del operando es b0, el segundo es b1, etc.).

|Tamaño |rango b0 |Rango de valor |Cálculo de valor|
---|---|---|---|
|1 |32 a 246| -107 a +107 |b0 - 139|
|2 |247 a 250| +108 a +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 a 254| -1131 a -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 a +32767| b1 << 8 | b2|
|5 |29| -(2^31) a +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Encabezado

Los datos binarios comienzan con un encabezado que tiene el formato que se muestra en la siguiente tabla.

|Tipo |Nombre |Descripción|
---|---|---|
|uint8| versión principal| Formatear la versión principal. Establecer en 2.|
|uint8| versión menor| Formato de versión secundaria. Poner a cero.|
|uint8| Tamaño del encabezado | Tamaño del encabezado (bytes).|
|uint16| topDictLength| Longitud de la estructura DICT superior en bytes.|

## Referencias

* [Formato de archivo CFF2](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2)

