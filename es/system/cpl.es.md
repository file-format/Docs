{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "extensión", "archivo", "formato", "sistema", "Archivo del panel de control", "Windows", "programas", "computadora", "aplicación" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Archivo del panel de control",
  "description":"Obtenga información sobre el formato de archivo CPL y las API que pueden crear y abrir archivos CPL",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## ¿Qué es un archivo CPL? ##

Un archivo CPL es un tipo de archivo de "sistema". Es utilizado por el sistema operativo Windows. Un archivo CPL es la abreviatura de Archivo del panel de control. Estos archivos son archivos binarios que se abren con el panel de control en un sistema operativo Microsoft Windows y se utilizan para representar y abrir las herramientas disponibles en el panel de control, como Mouse, Displays, Networking, entre otras. Los archivos CPL generalmente se almacenan en la carpeta del sistema en su dispositivo. Estos archivos no deben abrirse manualmente.


## Formato de archivo CPL ##

Los diferentes archivos CPL en su sistema operativo Windows están conectados para representar diferentes elementos del panel de control. Todos los elementos del panel de control están vinculados a un archivo CPL y tienen el sufijo ".cpl" adjunto a sus elementos.

Algunos tipos comunes de archivos CPL con sus formatos son:

* Ietcpl.cpl: para propiedades de Internet en su dispositivo
* Appwiz.cpl: para agregar o eliminar propiedades de programas en su dispositivo
* Desk.cpl: para las propiedades de visualización
* Main.cpl: para propiedades relacionadas con el mouse, las fuentes, el teclado y las impresoras.
* Netcpl.cpl: para propiedades relacionadas con la red
* System.cpl: para propiedades relacionadas con el sistema y para agregar nuevo asistente de hardware
* TimeDate.cpl: para propiedades de fecha u hora
* Mlcfg32.cpl: para propiedades de Microsoft Exchange o Windows Messaging
* Intl.cpl: esto se refiere a las propiedades de configuración regional
* Modem.cpl: para propiedades relacionadas con el módem
* Themes.cpl: almacena temas y propiedades de escritorio.
* Password.cpl: para propiedades de contraseña
* Mmsys.cpl: para propiedades multimedia
* Wgpocpl.cpl: pertenece a la oficina de correos de Microsoft Mail

## Breve historia ##

El tipo de archivo CPL fue desarrollado por Microsoft Windows y es una parte integral del sistema operativo Windows desde Windows 1.0. Todavía se usa en todas las versiones de Windows y todas las propiedades de los elementos del panel de control se almacenan con este tipo de archivo.

## Ejemplo de CPL ##

A continuación se puede ver un archivo CPL de muestra:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
