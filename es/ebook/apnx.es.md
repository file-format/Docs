{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Índice de números de página de Amazon", "extensión", "archivo", "formato", "eBook", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo Amazon APNX y las API que pueden crear y abrir archivos APNX",
  "title" :"APNX - Índice de números de página de Amazon",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## ¿Qué es un archivo APNX? ##

El archivo de índice de números de página de Amazon que utiliza la extensión .apnx es un tipo de archivo de libro electrónico; utilizado por Amazon Kindle. Estos archivos se conocen como archivos de paginación utilizados por los dispositivos Kindle. Por lo tanto, los archivos APNX generalmente se crean para marcar las páginas de los libros electrónicos Kindle. La función de paginación se ha iniciado en los dispositivos Amazon Kindle desde su firmware 3.1. Busca en el archivo APNX los índices de página y luego lo asigna con los números de página en el libro impreso original. Estos archivos se guardan en dispositivos Kindle junto con archivos de libros electrónicos de Amazon. No puede abrir ni editar los archivos APNX.

## Especificaciones del formato de archivo APNX ##

### Diseño

|bytes| contenido| comentarios|
---|---|---|
|4 |00010001 | Identificador de formato. Valor de 65537 little-endian.|
|4 |comienzo del siguiente | El desplazamiento después de la ubicación final del primer encabezado. Comienza una nueva secuencia de información de encabezado |
|4 |longitud| Longitud del primer encabezado|
|N |primer encabezado | Cadena que contiene el encabezado de contenido. Comienza la siguiente secuencia |
|2 |desconocido | Siempre 1|
|2 |longitud | Longitud del segundo encabezado |
|2 |recuento de páginas | Número total de bytes después del segundo encabezado que representan páginas. Este total incluye bytes que son ignorados por pageMap.|
|2 |desconocido | Siempre 32|
|N |segundo encabezado | Cadena que contiene el encabezado de asignación de página |
|4*N |relleno | El primer número dado en el encabezado de asignación de página indica el número de 0 bytes.|
|4*N |lista de páginas ||

### Encabezado de contenido

El encabezado de contenido consta de una cadena encerrada entre {} que contiene pares de clave y valor:

|contenido| comentarios|
---|---|
|contentGuid| Guía|
|asín | Identificador de Amazon para la versión Kindle del libro.|
|cdeTipo | Tipo de código MOBI. Siempre debe ser EBOK para libros electrónicos.|
|fileRevisionId | Revisión de este archivo.|

#### Ejemplo
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Encabezado de asignación de página
El encabezado de asignación de página consta de una cadena encerrada entre {} que contiene pares de clave y valor.

|contenido | comentarios|
---|---|
|asín | El ISBN 10 del libro en papel al que corresponden las páginas|
|paginaMapa| Tupla de tres valores. Parece: "(N,N,N)\
1) Número de bytes después del encabezado que inicia la secuencia de numeración de páginas\
2) desconocido\
3) desconocido\|
#### Ejemplo
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Lista de páginas

La lista de páginas es una secuencia de compensaciones en el código HTML sin formato. Cada
valor es el comienzo de una nueva página. Cada entrada es un big endian de 4 bytes
En t.



## Referencias

* [Formato de archivo Amazon APNX] (https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - por MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

