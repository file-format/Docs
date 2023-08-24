{
  "date" : "2021-07-12",
  "keywords" :[ "archivo cmd", "qué es un archivo cmd", "archivo", "ejemplo de cmd", "extensión de archivo cmd","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo CMD y las API que pueden crear y abrir archivos CMD",
  "title" :"CMD - Formato de archivo de comandos de Windows",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## ¿Qué es un archivo CMD?
Un archivo CMD consta de un script que contiene uno o varios comandos en forma de texto sin formato que se ejecutan para ejecutar varias tareas. Es similar a un archivo [BAT](/es/executable/bat/), que generalmente también se usa para almacenar un lote de comandos ejecutables. Los archivos CMD son ampliamente utilizados en el sistema operativo Microsoft Windows. Estos archivos se introdujeron casi en los años 90, pero aún se usan en el último sistema operativo Windows. Estos archivos generalmente se escriben para ejecutar más de un comando en una secuencia.

## formato de archivo cmd
CMD es un formato de archivo utilizado por programas ejecutables de estilo CP/M. Generalmente es comparable con [COM](/es/executable/com/) en CP/M-80 y [EXE](/es/executable/exe/) en DOS. Un archivo CMD contiene de 1 a 8 grupos de código o datos y un encabezado de 128 bytes. Cada grupo puede tener un tamaño de hasta 1 mb. Los archivos CMD también pueden contener información de reubicación y Extensiones del sistema residente (RSX) en sus versiones posteriores. El CMD es un recién llegado en comparación con el archivo [BAT](/es/executable/bat/); utilizado para MS-DOS antes del lanzamiento de Windows en MS-DOS. Aunque todavía puede guardar archivos con la extensión .bat hoy, muchas personas usan la extensión .cmd para guardar sus scripts ejecutables.

### Especificación del formato CMD

El inicio del encabezado contiene la lista de los grupos presentes en el archivo junto con sus tipos. Cada tipo se puede utilizar una vez como máximo. Estos tipos son:

- Código
- Datos
- Extra
- Pila
- Usuario 1
- Usuario 2
- Usuario 3
- Usuario 4
- Código compartido

Del mismo modo, el Prefijo de segmento de programa en DOS, los primeros 256 bytes del grupo de datos son cero. Serán rellenados por CP/M-86 con la página cero. Si no hay ningún grupo de datos, se utilizarán en su lugar los primeros 256 bytes del grupo de códigos.
## ejemplo de archivo CMD
El siguiente es un ejemplo de un script CMD para mostrar información de sistemas.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Referencias

* [Cómo escribir un script CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [Archivo CMD (CP/M) - por Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

