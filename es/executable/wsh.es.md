{
  "date" : "2021-08-27",
  "keywords" :[ "archivo wsh", "formato de archivo wsh", "qué es un archivo wsh", "archivo", "ejemplo de wsh", "extensión de archivo wsh","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo WSH y las API que pueden crear y abrir archivos WSH",
  "title" :"WSH - Archivo de secuencias de comandos de Windows",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## ¿Qué es un archivo WSH?
Un archivo con extensión .wsh contiene propiedades y parámetros para un determinado script de lenguaje de programación, como VB o VBS, etc. La necesidad real de WSH es usarlos para personalizar la ejecución de ciertos scripts. Se requiere WScript o CScript para ejecutarse y ambos se incluyen con el sistema operativo Windows. Los archivos WSH se proporcionaron inicialmente en Windows 95 en los discos de instalación como configurables e instalables opcionales para el Panel de control, y luego como un componente predeterminado de Windows 98.

## formato de archivo WSH
WSH (Windows Script Host) se puede usar para diversos fines, incluida la administración, los scripts de inicio de sesión y la automatización general. WSH establece un entorno para que se ejecuten los scripts. invoca el motor de secuencias de comandos adecuado y asigna un conjunto de servicios y objetos para que funcione la secuencia de comandos. Estos scripts se pueden ejecutar en modo GUI, desde un objeto COM o en modo de línea de comandos, lo que brinda flexibilidad al usuario para scripts interactivos o no interactivos.

### Ejemplos
Aquí hay un ejemplo muy simple que muestra algunos VBScript que usan el objeto raíz WSH COM "WScript" para mostrar un mensaje con un botón 'OK'. Cuando se inicie este script, se llamará al motor CScript o WScript y se establecerá el entorno de tiempo de ejecución.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Referencias

* [Windows Script Host - por Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)



