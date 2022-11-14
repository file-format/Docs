{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "extensión", "archivo", "formato", "sistema", "archivo TMP", "documentos TMP", "archivos TMP", "archivo temporal", "aplicación", "programas" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Formato de archivo temporal",
  "description":"Obtenga información sobre el formato de archivo TMP y las API que pueden crear y abrir archivos TMP",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## ¿Qué es un archivo TMP? ##

Un archivo TMP se refiere a una copia de seguridad transitoria, almacenamiento u otro sistema de archivos generado por un programa de software. Ocasionalmente se crea como un archivo invisible y con frecuencia se destruye cuando se cierra el programa. Los archivos TMP también se pueden usar para almacenar información temporalmente mientras se construye un nuevo archivo.

## Formato de archivo TMP ##

Un archivo TMP generalmente se compone de datos sin procesar que se utilizan como una fase en el proceso de conversión de material de un estilo a otro. Microsoft Word y Apple Safari son dos aplicaciones que pueden producir y usar el formato de archivo TMP.

Los documentos TMP generados deberían, en teoría, eliminarse automáticamente cuando se cierra el programa o se apaga la máquina. En la práctica, esto no siempre es así. Como resultado, mientras navega por los documentos de su programa, puede encontrar archivos transitorios que el sistema o cualquier otro software no utiliza activamente.

### Memoria auxiliar ###

La memoria virtual se usa en los sistemas operativos, sin embargo, los programas que utilizan grandes volúmenes de información pueden necesitar crear documentos temporales.

### Comunicación entre procesos ###

La mayoría de los sistemas operativos proporcionan primitivas para pasar datos entre programas, como conductos, sockets o memoria principal, pero el método más simple es transferir archivos a un archivo temporal y avisar a la aplicación receptora de la ubicación del archivo temporal.


## Especificación técnica ##

La obtención de nombres de documentos temporales distintivos generalmente la proporcionan los sistemas operativos y los programas de software.
Los archivos temporales se pueden generar de forma segura en sistemas POSIX utilizando las funciones de biblioteca mkstemp o tmpfile. Algunos sistemas incluyen la aplicación mktemp anterior de POSIX (desaparecida). Estos archivos generalmente se encuentran en el directorio temporal regular en plataformas Unix en /TMP, o %TEMP% (es específico para iniciar sesión) en máquinas con Windows.

Cuando el programa se detiene o el documento se cierra, el archivo transitorio generado con tmpfile se elimina automáticamente. GetTempFileName (Windows) o tmpnam (POSIX) se pueden usar para crear un nombre de archivo temporal que durará más que el programa que lo creó.

## Referencia ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
