{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - ¿Qué es un archivo APPX?",
  "description":"Obtenga información sobre el formato de archivo APPX y las API que pueden crear y abrir archivos APPX",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## ¿Qué es un archivo APPX?

Un archivo APPX es un formato de archivo de paquete distribuible que se utiliza para la distribución e instalación de una aplicación. Se introdujo con Windows 8 para ser publicado en Microsoft Windows Store. Contiene todos los archivos necesarios para instalar una aplicación de Windows. Estos incluyen metadatos, archivos e información de credenciales. Un formato de archivo de empaquetado más moderno es MSIX, que actualmente se usa más comúnmente en comparación con APPX.

## Formato de archivo APPX - Más información

Los archivos APPX se guardan como archivos comprimidos en formato de archivo [ZIP](/es/compression/zip/). Esto hace que todo el paquete sea un archivo de almacenamiento con un tamaño de archivo reducido que es fácil de cargar en Microsoft Store.

## ¿Cómo ver archivos en un archivo APPX?

Para ver los contenidos o archivos dentro de un archivo APPX, se deben seguir los siguientes pasos.

1. Dado que los archivos APPX se almacenan como archivos ZIP comprimidos, cambie el nombre del archivo a la extensión .zip
1. Use cualquier herramienta de descompresión como 7-Zip, WinZip o WinRAR para extraer los archivos contenidos en el archivo APPX

## ¿Cómo crear un archivo APPX?

Hay dos métodos que se pueden utilizar para crear archivos APPX.

1. Usando MakeApp.exe - [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) se usa para crear ambos paquetes de aplicaciones (.msix o .appx) y archivos de paquete de paquetes de aplicaciones .msixbundle o .appxbundle). Además, puede extraer archivos de un paquete de aplicaciones. MakeApp.exe está disponible con Windows 10 SDK y se puede usar desde el símbolo del sistema.
1. Usar Microsoft Visual Studio: los desarrolladores generalmente [crean archivos APPX] (https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) usando Microsoft Visual Studio. Una vez que se completa el desarrollo de la aplicación y la aplicación está lista para publicarse, se puede crear el archivo del paquete APPX publicándolo desde Visual Studio.

## Referencias

* [Cree un paquete o paquete MSIX con MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Cree archivos APPX con Microsoft Visual Studio] (https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

