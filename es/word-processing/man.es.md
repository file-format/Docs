{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Manual Unix",
  "description":"Obtenga información sobre el formato de archivo FODT y las API que pueden crear y abrir archivos MAN",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## ¿Qué es un archivo MAN?

Un archivo con la extensión .man significa página de manual, que es un manual de usuario de programación de Unix en forma de documentación de software. Es utilizado por la utilidad `Man`, incluida en Unix, que se utiliza para ver la documentación. La documentación del software contiene información en secciones y páginas que se pueden recuperar utilizando la utilidad Man desde el terminal de comandos emitiendo comandos. Al estar disponible en la computadora como copia electrónica de la documentación, no requiere ninguna copia impresa o conexión a Internet para acceder a ella.

## Formato de archivo manual de Unix Man: más información

Las páginas del manual se almacenan en formato de texto sin formato y se pueden crear y abrir en cualquier editor de texto para verlas o editarlas. En UNIX, la información de las páginas Man se recupera emitiendo comandos desde el terminal que incluyen referencias a los números de sección y página del manual.

### Secciones y páginas

Unix man es el manual del sistema donde cada argumento de página del comando se refiere al nombre de un programa, utilidad o función. el comando, si se le proporciona información de la sección, buscará la página en esa sección específica. Sin embargo, el comportamiento predeterminado es buscar la página en todas las secciones y mostrar la primera página independientemente de si existe en varias secciones.

### Números de sección

A continuación se encuentra la información sobre los números de sección del manual seguido de los tipos de páginas que contienen.

|Número de sección|Tipo de páginas|
---|---|
|1|Programas ejecutables o comandos de shell|
|2|Llamadas al sistema (funciones proporcionadas por el kernel)|
|3|Llamadas a bibliotecas (funciones dentro de bibliotecas de programas)|
|4|Archivos especiales (normalmente se encuentran en /dev)|
|5|Formatos de archivo y convenciones, por ejemplo, /etc/passwd|
|6|Juegos|
|7|Varios (incluidos paquetes de macros y convenciones), por ejemplo, man(7), groff(7)|
|8|Comandos de administración del sistema (generalmente solo para root)|
|9|Rutinas del núcleo [No estándar]|

## Ejemplo - ¿Cómo leer páginas MAN?

Aquí hay un ejemplo de cómo recuperar información sobre el comando MkDir usando el comando Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Referencias

* [Especificaciones técnicas de OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Página del manual de Linux](https://man7.org/linux/man-pages/man1/man.1.html)

