{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "archivo", "extensión", "formato de archivo", "Archivo de intercambio de datos", "Hoja de cálculo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Su guía de formato de archivo para saber qué es una extensión de archivo DIF y las API que pueden crear y abrir archivos DIF",
  "title" :"DIF - Formato de archivo de intercambio de datos",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## ¿Qué es un archivo DIF?

DIF significa Formato de intercambio de datos que se utiliza para importar/exportar datos de hojas de cálculo entre diferentes aplicaciones. Estos incluyen Microsoft Excel, OpenOffice Calc, StarCalc y muchos otros. Almacena los datos contenidos en una sola hoja de cálculo, que es la única limitación de este formato de archivo.

## Breve historia del formato de archivo DIF ##

El formato de archivo DIF fue desarrollado por Software Arts, Inc. a principios de la década de 1980. Las especificaciones de formato de archivo para DIF se incluyeron en VisiCalc, que fue el primer programa de hoja de cálculo para computadoras personales. Estas especificaciones tenían derechos de autor en 1981 y eran una marca registrada de Software Arts Products Corp.

## Formato de archivo DIF ##

DIF almacena el contenido de la hoja de cálculo en un archivo de texto ASCII que permite verlo y editarlo con un editor de texto. El formato posee su lugar en la lista de formatos de serialización de datos por sus características de intercambio de datos. Un archivo DIF consta de 2 secciones; un encabezado y datos.

Todo en DIF está representado por un fragmento de 2 o 3 líneas. Los encabezados obtienen un fragmento de 3 líneas; datos, 2.

* Los fragmentos de encabezado comienzan con un identificador de texto que está todo en mayúsculas, solo caracteres alfabéticos y menos de 32 letras. La siguiente línea debe ser un par de números y la tercera línea debe ser una cadena entre comillas.
* Los fragmentos de datos comienzan con un par de números y la siguiente línea es una cadena entre comillas o una palabra clave.

### Valores ###

Un valor ocupa dos líneas, la primera un par de números y la segunda una cadena o una palabra clave. El primer número del par indica el tipo:

* −1 – tipo de directiva, el segundo número se ignora, la siguiente línea es una de estas palabras clave:
** BOT – principio de tupla (inicio de fila)
** EOD – fin de datos
* 0 – tipo numérico, el valor es el segundo número, la siguiente línea es una de estas palabras clave:
** V – válido
** NA – no disponible
** ERROR – error
** VERDADERO: verdadero valor booleano
** FALSO – valor booleano falso
* 1 – tipo de cadena, el segundo número se ignora, la siguiente línea es la cadena entre comillas dobles

### Fragmento de encabezado DIF ###

El fragmento de encabezado de un archivo DIF se compone de una línea de identificación seguida de las dos líneas de un valor. Los valores numéricos en los fragmentos de encabezado usan solo una cadena vacía en lugar de las palabras clave de validez. Los detalles de estos fragmentos de encabezado son los siguientes.

* TABLA: sigue un valor numérico de la versión, la segunda línea en desuso del valor contiene un comentario del generador
* VECTORES - el número de columnas sigue como un valor numérico
* TUPLAS - el número de filas sigue como un valor numérico
* DATOS: después de un valor numérico ficticio 0, siguen los datos de la tabla, cada fila precedida por un valor BOT, la tabla completa termina con un valor EOD

### Ejemplo de DIF ###

El siguiente ejemplo muestra el contenido de una hoja de trabajo simple y su representación DIF equivalente.


|Nombre|Edad
---|---|
|Bob|34
|Hoja|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Referencias ##

* [ DIF - Por Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)

