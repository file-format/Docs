{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo MDMP - Formato de archivo de minivolcado de Windows",
  "description":"Obtenga información sobre el formato de archivo MDMP y las API que pueden crear y abrir archivos MDMP",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## ¿Qué es un archivo MDMP?

Un archivo MDMP es un volcado de memoria de una aplicación en Microsoft Windows que se crea cuando la aplicación se cierra de forma anormal o falla. Contiene información y volcados de datos que se pueden usar para depurar la causa del bloqueo. Los archivos MDMP son aplicables en aplicaciones creadas por cualquier plataforma como Java, C++, .NET y otras. Además de MDMP,

Las aplicaciones que pueden abrir archivos MDMP incluyen Microsoft Visual Studio Debugger.

## Formato de archivo MDMP

Los archivos MDMP se guardan como archivos binarios en el disco y se pueden abrir con el depurador de Microsoft Visual Studio. Contiene la siguiente información para ayudar a identificar el motivo del bloqueo.

* Detalles del mensaje Stop, sus parámetros y otros datos
* Lista de controladores cargados
* Contexto del procesador (PRCB) para el procesador que dejó de funcionar
* Información del proceso y contexto del núcleo (EPROCESS) para el proceso que se detuvo
* Información del proceso y contexto del núcleo (ETHREAD) para el subproceso que se detuvo
* Pila de llamadas en modo Kernel para el subproceso que se detuvo

Esta información ayuda a averiguar qué sucedió, solucionar el problema y evitar que vuelva a suceder.

### Analizar minivolcado

Windows requiere un archivo de paginación en el volumen de arranque para crear un archivo de volcado de memoria. El archivo de paginación se crea en el volumen de inicio y debe tener un tamaño mínimo de 2 megabytes (MB). El archivo de volcado se crea cuando una aplicación falla. En caso de un segundo problema, se crea un segundo archivo de volcado de memoria pequeño mientras se conserva el anterior. El nombre del archivo de volcado es distinto para evitar que se sobrescriba.

Windows mantiene una lista de todos los archivos de volcado de memoria en la carpeta %SystemRoot%\Minidump. Puede analizar archivos MDMP ejecutándolos en Visual Studio Debugger como se indica en los pasos a continuación.

## ¿Cómo abro un archivo MDMP en Visual Studio?

Los siguientes pasos se pueden usar para abrir un archivo MDMP en Visual Studio.

* En Visual Studio, en el menú Archivo, elija Abrir | Volcado por caída.
* Navegue hasta el archivo de volcado que desea abrir.
* Seleccione Abrir.

## Referencia

* [Cómo leer el archivo de volcado de memoria pequeña que crea Windows si se produce un bloqueo](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -expediente)

