{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC: formato de archivo de colección TrueType",
  "description":"Un archivo TrueType Collection (TTC) combina varias fuentes en un solo archivo. Tanto Apple como Microsoft usaban TTF en los sistemas operativos Mac y Windows",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## ¿Qué es un archivo TTC?
El TTC se abrevia como TrueType Collection y es una extensión del formato True Type. Un archivo TTC puede combinar varios archivos de fuentes en él. Estos archivos son útiles para combinar varias fuentes que comparten muchos glifos en común. Antes de Windows 2000, los archivos TTC se usaban en las versiones de Windows en chino, japonés y coreano, pero más tarde la compatibilidad estuvo disponible para todas las regiones.


## La estructura del archivo de colección de fuentes
Un archivo TTC consta de una tabla de encabezado TTC, directorios de tablas y varias tablas OpenType. El encabezado TTC debe encontrarse al comienzo del archivo. Debe existir un directorio de tabla completo para cada fuente. El formato de TableDirectory debe ser similar al que existía en un archivo que no es de colección. Los recuentos de tablas en todos los directorios dentro de un archivo TTC se calculan desde el inicio de un archivo TTC.
Las tablas en un archivo TTC se referencian a través del directorio de tablas de sus respectivas fuentes. Algunas de las tablas OpenType deben aparecer varias veces, una para cada fuente agregada en el TTC. Mientras que las otras tablas pueden ser compartidas por varias fuentes en el archivo TTC.

### Encabezado TTC
Dos versiones de la tabla de encabezado TTC están disponibles hasta el momento:
- La versión 1.0 se utiliza para archivos TTC sin firmas digitales.
- La versión 2.0 se puede utilizar para archivos TTC con o sin firmas digitales.
Aquí están las tablas de encabezado TTC de ambas versiones:

**Encabezado TTC Versión 1.0:**

|Tipo|Nombre|Descripción|
---|---|---|
|TAG|ttcTag|Cadena de ID de colección de fuentes: 'ttcf' (utilizado para fuentes con contornos CFF o CFF2, así como contornos TrueType)|
|uint16|majorVersion|Versión principal del encabezado TTC, = 1.|
|uint16|minorVersion|Versión secundaria del encabezado TTC, = 0.|
|uint32|numFonts|Número de fuentes en TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Matriz de compensaciones al TableDirectory para cada fuente desde el principio del archivo|

**Encabezado TTC Versión 2.0:**

|Tipo|Nombre|Descripción|
---|---|---|
|TAG|ttcTag |Cadena de ID de colección de fuentes: 'ttcf'|
|uint16| majorVersion |Versión principal del encabezado TTC, = 2.|
|uint16| minorVersion |Versión menor del encabezado TTC, = 0.|
|uint32| numFonts |Número de fuentes en TTC|
|Desplazamiento32| tableDirectoryOffsets[numFonts] |Array de desplazamientos al TableDirectory para cada fuente desde el principio del archivo|
|uint32| dsigTag |Etiqueta que indica que existe una tabla DSIG, 0x44534947 ('DSIG') (nulo si no hay firma)|
|uint32| dsigLength |La longitud (en bytes) de la tabla DSIG (nula si no hay firma)|
|uint32| dsigOffset |El desplazamiento (en bytes) de la tabla DSIG desde el principio del archivo TTC (nulo si no hay firma)|

## Referencias
* [El archivo de fuentes OpenType](https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

