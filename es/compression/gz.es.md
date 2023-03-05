{
  "date" : "2019-10-11",
  "keywords" :[ "archivo gz", "formato de archivo gz", "qué es un archivo gz", "archivo", "ejemplo gz", "extensión de archivo gz","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo GZ - Archivo de archivo comprimido GNU",
  "description":"Obtenga información sobre qué es un archivo GZ y las API que pueden crear y abrir archivos GZ",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo GZ?

Un archivo GZ es un archivo comprimido que se crea utilizando el algoritmo de compresión estándar [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Puede contener múltiples archivos comprimidos, directorios y apéndices de archivos. Este formato se desarrolló inicialmente para reemplazar los formatos de compresión en los sistemas UNIX. y sigue siendo uno de los tipos de archivo más comunes en los sistemas Linux. Aplicaciones como [WinZip](https://www.winzip.com/en/) pueden abrir archivos GZ para ver su contenido tanto en Windows como en MacOS.

## Formato de archivo GZ - Más información

Gzip utiliza el algoritmo [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) para la compresión del archivo y se diferencia del formato de archivo [ZIP](/es/compression/zip/) en la aplicación del algoritmo de compresión en el archivo completo. en lugar de archivos individuales. Las especificaciones de formato de archivo GZIP versión 4.3 publicadas por el Grupo de trabajo de ingeniería de Internet (IETF) contienen información detallada sobre el formato de archivo. El formato de archivo consta de:

* Encabezado de archivo
* Encabezados opcionales
* Datos comprimidos
* Pie de página del archivo

## Encabezado del archivo GZ ##

El encabezado del archivo GZ consta de 10 bytes de la siguiente manera:

|Desplazamiento|Tamaño|Valor|Descripción
---|---|---|---|
|0|2|0x1f 0x8b|Número mágico que identifica el tipo de archivo
|2|1| |Método de compresión * 0-7 (Reservado) * 8 (Desinflado)
|3|1| |Banderas de archivo
|4|4| |marca de tiempo de 32 bits
|8|1| |Banderas de compresión
|9|1| |ID del sistema operativo

### Indicadores de archivo ###

|Valor|Identificador|Descripción
---|---|---|
|0x01|FTEXT|Si se establece, los datos sin comprimir deben tratarse como texto en lugar de datos binarios. Esta marca indica la conversión de final de línea para archivos de texto multiplataforma, pero no la impone.
|0x02|FHCRC|El archivo contiene una suma de comprobación de encabezado (CRC-16)
|0x04|FEXTRA|El archivo contiene campos adicionales
|0x08|FNAME|El archivo contiene una cadena de nombre de archivo original
|0x10|FCOMMENT|El archivo contiene un comentario
|0x20| |Reservado
|0x40| |Reservado
|0x80| |Reservado

### Sistema operativo ###

|Valor|Descripción
---|---|
|0|Sistema de archivos FAT (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (u OpenVMS)
|3|Unix
|4|VM/CMS
|5|TDS de Atari
|6|Sistema de archivos HPFS (OS/2, NT)
|7|Macintosh
|8|Sistema Z
|9|CP/M
|10|TOP-20
|11|sistema de archivos NTFS (NT)
|12|QDOS
|13|RISCOS DE BELLOTA
|255|desconocido

## Encabezados opcionales GZ ##

Los encabezados adicionales opcionales son los indicados por las banderas del archivo e incluyen información como el nombre del archivo original, campos adicionales, comentarios y suma de verificación del encabezado.

## Datos comprimidos ##

Esta sección contiene los datos comprimidos utilizando el algoritmo de compresión DEFLATE.

## Pie de página del archivo GZ ##

El pie de página del archivo tiene un tamaño de 8 bytes y contiene la siguiente información.

|Desplazamiento|Tamaño|Descripción
---|---|---|
|0|4|Suma de control (CRC-32)
|4|4|Valor del tamaño de los datos sin comprimir en bytes

## Referencias ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: especificación de formato de archivo GZIP](http://tools.ietf.org/html/rfc1952), por IETF.

