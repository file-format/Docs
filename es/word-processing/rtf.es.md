{
  "date" : "2019-10-11",
  "keywords" :[ "archivo rtf", "formato de archivo rtf", "qué es un archivo rtf", "archivo", "ejemplo de rtf", "extensión de archivo rtf","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Formato de texto enriquecido",
  "description":"Obtenga información sobre el formato de archivo RTF y las API que pueden crear y abrir archivos RTF",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo RTF?

Presentado y documentado por Microsoft, el formato de texto enriquecido (**RTF**) representa un método de codificación de texto y gráficos con formato para su uso dentro de las aplicaciones. El formato facilita el intercambio de documentos multiplataforma con otros Productos de Microsoft, cumpliendo así el propósito de la interoperabilidad. Esta capacidad lo convierte en un estándar de transferencia de datos entre software de procesamiento de texto y, por lo tanto, los contenidos se pueden transferir de un sistema operativo a otro sin perder el formato del documento. Las especificaciones de formato de archivo están disponibles por Microsoft para [descarga] pública (https://www.microsoft.com/en-us/download/details.aspx?id#10725) y se pueden consultar desde la perspectiva del desarrollador.

## Breve historia del formato de archivo RTF ##

El formato de archivo RTF ha sufrido varias revisiones desde su publicación. Su versión oficial de lectura/escritura se publicó como parte de Microsoft Word 3.0 para Macintosh con las especificaciones de la versión 1.0. La versión final de las especificaciones, 1.9.1, fue publicada por Microsoft en marzo de 2008. No se realizan más mejoras a las especificaciones después de esto. En la actualidad, casi todos los sistemas operativos tienen más aplicaciones ricas en funciones que han minimizado/erradicado el uso del formato de archivo RTF.

## Especificaciones del formato de archivo RTF ##

RTF sirve como un estándar de transferencia de datos entre el software de procesamiento de texto y la transferencia de contenido de un sistema operativo a otro. Esto se logra utilizando palabras de control que fueron introducidas por Microsoft Office Word hasta 2007. Un archivo RTF estándar consta de ASCII para representar texto enriquecido y con caracteres que no son ASCII que se convierten en valores de código apropiados. Las versiones más nuevas de Word pueden leer archivos RTF generados con versiones anteriores, mientras que las versiones anteriores ignoran las palabras de control y los grupos que no entienden.

### Comprender los fundamentos de RTF ###

Los archivos RTF utilizan texto sin formato ASCII de 7 bits, que consta de:

* palabras de control
* símbolos de control, y
* grupos.

Estos actúan como bloques de construcción para la representación de datos RTF como texto comprensible y codificación de caracteres.

#### Palabra de control ####

Estos representan comandos con formato especial que se utilizan para marcar caracteres para mostrar y no pueden tener más de 32 letras. Una palabra de control se define por:

\<ASCII Letter Sequence> //<//Delimiter//> //

Cada palabra de control distingue entre mayúsculas y minúsculas y comienza con una barra invertida. La secuencia de letras ASCII puede contener alfabetos ASCII (de la a a la z y de la A a la Z). los<Delimite> marca el final del nombre de la palabra de control y puede ser uno de los siguientes:

* Un espacio. Esto sirve solo para delimitar una palabra de control y se ignora en el procesamiento posterior.
* Un dígito numérico o un signo menos ASCII, que indica que un parámetro numérico está asociado con la palabra de control. La secuencia digital subsiguiente está entonces delimitada por cualquier carácter que no sea un dígito ASCII (comúnmente otra palabra de control que comienza con una barra invertida). El parámetro puede ser un número decimal positivo o negativo. El rango de valores para el número es nominalmente –32768 a 32767, es decir, un entero de 16 bits con signo. Una pequeña cantidad de palabras de control toman valores en el rango‌ −2,147,483,648 a 2,147,483,647 (entero con signo de 32 bits). Estas palabras de control incluyen **\binN**, **\revdttmN//**, **\rsidN** palabras de control relacionadas y algunas propiedades de imagen como **\bliptagN**. Aquí **N** representa el parámetro numérico. Un analizador RTF debe permitir hasta 10 dígitos precedidos opcionalmente por un signo menos. Si el delimitador es un espacio, se descarta, es decir, no se incluye en el procesamiento posterior.
* Cualquier carácter que no sea una letra o un dígito. En este caso, el carácter delimitador termina la palabra de control y no forma parte de la palabra de control. Como una barra invertida "\", que significa que sigue una nueva palabra de control o un símbolo de control.

#### Símbolo de control ####

Un símbolo de control representa una ocurrencia especial que tiene un significado específico según su contenido. Consiste en una barra invertida seguida de un carácter especial (carácter no alfabético) y no tiene delimitadores.

#### Grupo ####

Un grupo puede constar de texto, palabras de control o símbolos de control encerrados entre llaves (**{ }**). La llave de apertura (**{**) indica el inicio del grupo y la llave de cierre (**}**) indica el final del grupo. Cada grupo especifica el texto afectado por el grupo y los diferentes atributos de ese texto.

### Estructura del archivo RTF ###

Un archivo RTF tiene la siguiente sintaxis estándar:

Presentado y documentado por Microsoft, el formato de texto enriquecido (**RTF**) representa un método de codificación de texto y gráficos con formato para su uso dentro de las aplicaciones. El formato facilita el intercambio de documentos multiplataforma con otros Productos de Microsoft, cumpliendo así el propósito de la interoperabilidad. Esta capacidad lo convierte en un estándar de transferencia de datos entre software de procesamiento de texto y, por lo tanto, los contenidos se pueden transferir de un sistema operativo a otro sin perder el formato del documento. Las especificaciones de formato de archivo están disponibles por Microsoft para [descarga] pública (https://www.microsoft.com/en-us/download/details.aspx?id#10725) y se pueden consultar desde la perspectiva del desarrollador.

#### Encabezado RTF ####

Un encabezado RTF tiene la siguiente representación.

|Campo|Descripción
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Las tablas de encabezado deben aparecer en este orden si existen. El archivo RTF puede incluir grupos de fuentes, estilos, color de pantalla, imágenes, notas al pie, comentarios (anotaciones), encabezados y pies de página, información resumida, campos, marcadores, propiedades de formato de documentos, secciones, párrafos y caracteres, matemáticas, imágenes y objetos. Si la fuente, el archivo, el estilo, el color, la marca de revisión y los grupos de información de resumen y las propiedades de formato del documento están incluidos en el archivo, deben aparecer en el encabezado RTF, que precede al cuerpo RTF. Si no se utiliza el contenido de algún grupo, se puede omitir el grupo. Cualquier grupo que use las propiedades definidas en otro grupo debe aparecer después del grupo que define esas propiedades. Por ejemplo, las propiedades de color y fuente deben preceder al grupo de estilo.

#### Versión RTF ####

Un documento RTF debe comenzar con estos seis caracteres:

```
{\rtf1
```
donde el 1 muestra el número de versión RTF.

#### Conjunto de caracteres ####

Después de {\rtf1, el documento debe declarar qué juego de caracteres usa. La forma de declarar un conjunto de caracteres es con uno de estos comandos:

`\ansi`: el documento está en el conjunto de caracteres ANSI, también conocido como página de códigos 1252, el conjunto de caracteres habitual de MSWindows.

`\mac`: el documento está en el conjunto de caracteres MacAscii, el conjunto de caracteres habitual en las versiones antiguas (anteriores a la 10) de Mac OS.

`\pc`: el documento se encuentra en la página de códigos 437 de DOS, el juego de caracteres predeterminado para MS-DOS. Los mecanógrafos con buena memoria muscular notarán que este es el conjunto de caracteres que todavía se usa para interpretar los códigos "Alt numéricos", es decir, cuando mantiene presionada la tecla Alt y escribe "130" en el teclado numérico, produce una é, porque el carácter 130 en CP437 es una é. Ese es el único uso que CP437 ve en estos días.

`\pca`: el documento se encuentra en la página de códigos 850 de DOS, también conocida como la página de códigos multilingüe de MS-DOS.

#### Comando de fuentes ####

La definición del conjunto de caracteres va seguida del comando `\deffN`. Esto define que el número de fuente N es la fuente predeterminada para este documento. El número de fuente N se refiere a la tabla de fuentes. El comando `\deffN` es técnicamente opcional, pero debería estar allí para estar seguro como un prólogo común como el siguiente, elige la fuente 0 como la fuente predeterminada.

`{\rtf1\ansi\deff0`

#### Tabla de fuentes ####

Todas las fuentes que se pueden usar en un documento se enumeran en una tabla de fuentes donde cada fuente está representada por un número de fuente. El documento debe tener una tabla de fuentes, aunque algunos programas también funcionarán sin ella.

La sintaxis de una tabla de fuentes es {\fonttbl //...declaraciones//...}, en la que cada declaración tiene esta sintaxis básica:

`{\fnumber\familycommand Nombre de fuente;}`

Una tabla de fuentes con cuatro declaraciones es la siguiente:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

En un documento con esa tabla de fuentes, `{\f2 cosas}` imprimiría "cosas" en Courier New. Una fuente no se puede usar en un documento hasta que se incluye en la tabla de fuentes.

### Fin del documento ###

Todo documento RTF debe terminar con un }, para cerrar el grupo abierto por el { que es el primer carácter del documento. Nada puede seguir al } final, excepto posiblemente una nueva línea.

## Referencias ##

* [Especificaciones de RTF 1.9.1](https://www.microsoft.com/en-us/download/details.aspx?id#10725)
* [Formato de texto enriquecido](https://en.wikipedia.org/wiki/Rich_Text_Format)

