{
  "date" : "2019-10-11",
  "keywords" :[ "archivo rar", "formato de archivo rar", "qué es un archivo rar", "archivo", "ejemplo rar", "extensión de archivo rar","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"¿Qué es una extensión de archivo RAR y las API que pueden crear y abrir archivos RAR?",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo RAR?

Los archivos con extensión .rar son archivos de almacenamiento que se crean para almacenar información en forma comprimida o normal. RAR, que significa formato de archivo Roshal ARchive, es un formato de archivo patentado creado por Eugene Roshal en 1995, un ingeniero de software ruso. El formato se utiliza para archivar archivos con diferentes métodos, incluidas varias técnicas de compresión. Hay varias aplicaciones de software disponibles para Windows, Linux y MacOS para la extracción de archivos RAR. El software WinRAR, de RARLab, es la utilidad de archivado de archivos shareware (gratis durante 40 días) para la plataforma Microsoft Windows; el software fue portado a Linux (solo como extractor) por el mismo autor, Eugene Roshal.

## Historial de versiones del formato de archivo RAR

* v1.3 (original, no tiene la firma "Rar!")
* v1.5
* v2.0 - publicado con WinRAR 2.0 y Rar para MS-DOS 2.0
* v2.9 - publicado en WinRAR versión 3.00
* v5.0 - compatible con WinRAR 5.0 y posterior

## Características clave del formato RAR

RAR ha estado en el campo durante bastante tiempo y ha sido uno de los formatos de archivos de archivo favoritos. Las características clave del formato RAR son:

**`Relación de compresión alta:`** Superior en comparación con [ZIP](/es/compression/zip/), comparable con los formatos 7z y zipx.

**`Cifrado de archivos sólido por diseño:`** Los archivos RAR4 cifrados se basan en el cifrado basado en AES-128, mientras que los archivos RAR5 cifrados se basan en el cifrado AES-256 con programación de claves mejorada

**`Capacidades avanzadas de corrección de errores y recuperación de datos:`** registros de recuperación opcionales durante la creación del archivo

**`Tamaño del archivo:`** Mínimo 20 bytes y máximo 2^63 bytes de tamaño (8 exabytes del tamaño total del archivo)

**`Archivos RAR de varios volúmenes:`** Posibilidad de dividir archivos grandes en varios archivos más pequeños para facilitar la transferencia a través de la red. En tal caso, las extensiones de archivo se incrementan en 1 para representar volúmenes divididos

## Formato de archivo RAR

Las especificaciones completas del formato RAR no están disponibles públicamente y es por eso que los detalles sobre el formato no se pueden formular de manera concisa.

### Diseño de archivo general

El diseño general de un formato de archivo RAR introducido en la versión 5.0 es el siguiente:

|Formato de archivo
---|
|Módulo autoextraíble (opcional)
|RAR 5.0 Firma
|Encabezado de cifrado de archivo (opcional)
|Encabezado del archivo principal
|Encabezado del servicio de comentarios de archivo (opcional)
Encabezado de archivo 1
|Encabezados de servicio (NTFS ACL, secuencias, etc.) para el archivo anterior (opcional)
|...
|Encabezado de archivo N
|Encabezados de servicio (NTFS ACL, secuencias, etc.) para el archivo anterior (opcional)
|Registro de recuperación (opcional)
|Encabezado de fin de archivo

Puede encontrar información sobre cada sección del archivo RAR mencionado anteriormente en el documento [Especificaciones del formato de archivo RAR 5.0] (https://www.rarlab.com/technote.htm#arcstruct).

#### Archivos RAR autoextraíbles

Si el archivo RAR en sí es autoextraíble, la información autoextraíble se encuentra al comienzo del archivo que precede a la firma del archivo. Su tamaño y contenido no están definidos.

#### Firma RAR 5.0

La firma RAR es un encabezado de 8 bytes que consta del siguiente número mágico:

0x52 61 72 21 1A 07 00

dónde

0x6152 - CABEZA_CRC

0x72 - TIPO DE CABEZA

0x1A21 - CABEZA_BANDERAS

0x0007 - TAMAÑO_CABEZA

## Referencias

* [Formato de archivo RAR 5.0] (https://www.rarlab.com/technote.htm)
* [RAR - Por Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))

