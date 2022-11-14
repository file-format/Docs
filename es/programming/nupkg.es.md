{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo NUPKG - Archivo de paquete NuGet",
  "description":"Obtenga información sobre el formato de archivo NUPKG y las API que pueden crear y abrir archivos NUPKG",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## ¿Qué es un archivo NUPKG?

Un archivo NUPKG es un archivo de paquete que contiene el código fuente que utilizará el software NuGet para crear paquetes que se utilizarán en proyectos .NET. El componente NuGet Package Manager se instala como parte de Microsoft Visual Studio para obtener paquetes del repositorio de alojamiento de paquetes en línea. Los archivos NUPKG ayudan a los desarrolladores a obtener los paquetes más recientes de [Nuget.org](https://nuget.org) mediante NuGet Package Manager en lugar de descargar e instalar manualmente los paquetes de desarrollo. Los archivos NUPKG se crean a partir de archivos NUSPEC y, cuando se recuperan, instalan el paquete en el sistema del usuario.

## Formato de archivo NUPKG

Los archivos NUPKG son archivos [ZIP](/es/compression/zip/) que contienen las bibliotecas empaquetadas en su interior. Cuando se descarga, se puede cambiar el nombre a .zip y extraerse con cualquier utilidad zip estándar como WinZIP, 7-Zip y Apple Archive Utility.

## Referencia

* [Nuget.org](https://nuget.org)
* [Inicio rápido: instalar y usar un paquete en Visual Studio (solo Windows)](https://docs.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- estudio)
* [Cómo crear y publicar un paquete Nuget](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)

