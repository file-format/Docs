{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "extensión", "archivo", "formato", "sistema", "Controlador", "Archivo de sistema", "programas", "computadora", "aplicación" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Formato de archivo del sistema",
  "description":"Obtenga información sobre el formato de archivo SYS y las API que pueden crear y abrir archivos SYS",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## ¿Qué es un archivo SYS? ##

Los archivos SYS son "archivos de sistema" utilizados en el sistema operativo Windows y aplicaciones MS-DOS. Estos archivos no se pueden abrir directamente y consisten en el controlador y la configuración del dispositivo. Los archivos SYS son responsables de contener archivos de funciones básicas del sistema operativo. Estos se consideran archivos críticos del controlador del dispositivo y también se pueden usar cuando se debe resolver cualquier problema del controlador de carreras. Estos son los responsables del buen funcionamiento de un sistema informático, y los archivos .sys deben ser correctos y completos.


## Especificación técnica ##

Los archivos .sys son en realidad el subconjunto del formato [BMP](/es/image/bmp/), ya que solo permite combinaciones específicas. El formato habitual de estos archivos es como LOGOS.SYS, LOGOW.SYS y LOGO.SYS. Cualquier otro archivo no tiene este formato.

Estos archivos se utilizan principalmente en el directorio *C* de Windows en el momento de la instalación. La mayoría de los problemas relacionados con los controladores de dispositivos se resuelven actualizando el sistema operativo Windows. Los detalles y la información de estos archivos se pueden ver utilizando los programas integrados del sistema operativo Windows. Estos también comprenden las referencias a diferentes módulos en un sistema operativo.
Algunos de los ejemplos de archivos del sistema son:

* IO.SYS (Estos almacenan controladores de dispositivos del sistema operativo del disco)
* MSDOS.SYS (Estos contienen kernel o el código central del sistema operativo)
* CONFIG.SYS (Estos contienen varias opciones de configuración)
* KEYBOARD.SYS (Estos contienen información relacionada con el diseño del teclado)
* COUNTRY.SYS (Estos contienen información relacionada con el país y la página de códigos)

## Formato de archivo SYS ##

Microsoft desarrolló los archivos con extensiones .sys. Las variables y funciones se incluyen en los archivos SYS. Estos son utilizados principalmente por el sistema operativo de Microsoft. Estos archivos se encuentran principalmente en el directorio raíz del disco:

* C:\Windows\system32\drivers
* C:\Windows\WinSxS

Algunas advertencias comunes sobre los archivos SYS son las siguientes:

* Los nombres de estos archivos no deben cambiarse ya que estos archivos son responsables de las funciones principales y las variables del sistema operativo.
* Estos archivos no deben eliminarse porque su ausencia puede causar errores
* Los archivos .sys no deben descargarse de Internet hasta que esté seguro de la legitimidad de la fuente
* Uno no debe meterse con estos archivos ya que cambiarlos o jugar con estos causa errores serios en el sistema
* Si estos archivos se corrompen por algún virus o malware, estos deben ser reinstalados

## Ejemplo de sistema ##

El siguiente es un ejemplo de un archivo de configuración del sistema SYS simple:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
