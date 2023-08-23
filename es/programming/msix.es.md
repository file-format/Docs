{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - ¿Qué es un archivo MSIX?",
  "description":"Obtenga información sobre el archivo MSIX y las API que pueden crear y abrir archivos MSIX",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## ¿Qué es un archivo MSIX?

Un archivo MSIX es un formato de paquete de aplicaciones de Windows que se usa para crear y distribuir aplicaciones en Windows 10. Este es el formato de archivo de paquete moderno en comparación con [APPX](/es/programming/appx/) y MSI que finalmente se eliminará gradualmente a este nuevo formato de archivo. Se puede usar para la implementación de aplicaciones Win32, WPF y Windows Forms. Los archivos MSIX son confiables y tienen como objetivo la optimización del espacio en disco y la red. Los desarrolladores los usan para distribuir programas a los usuarios finales a través de Microsoft Store (anteriormente conocida como Windows Store).

## Formato de archivo MSIX: más información

Los archivos MSIX están comprimidos [ZIP](/es/compression/zip/), con todos los archivos incluidos dentro del archivo empaquetado. Además de los archivos relacionados con la aplicación, el archivo MSIX contiene archivos de configuración [.xml](/es/web/xml/) que contienen información relacionada con la instalación de la aplicación.

## ¿Qué hay dentro de un paquete MSIX?

Un paquete MSIX consta de los siguientes archivos.

* `AppxBlockMap.xml`: conocido como el archivo de mapa de bloques del paquete, es un documento XML que contiene una lista de los archivos de la aplicación con índices y hashes criptográficos para cada bloque de datos almacenado en el paquete.
* `AppxManifest.xml`: un documento XML que contiene la información necesaria para la implementación, visualización y actualización de una aplicación MSIX. Esta información incluye la identidad del paquete, las dependencias del paquete, las capacidades requeridas, los elementos visuales y los puntos de extensibilidad.
* `AppxSignature.p7x` - Un archivo que se genera cuando se firma el paquete. Todos los paquetes de MSIX deben estar firmados antes de la instalación. Con AppxBlockmap.xml, la plataforma puede instalar el paquete y validarse.

## Referencias

* [Descripción general de MSIX](https://learn.microsoft.com/en-us/windows/msix/overview)
* [Cree archivos APPX con Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

