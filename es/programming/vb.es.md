{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "archivo", "extensión", "formato de archivo", "Visual Basic", "Guía de programación" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Archivo de código de Visual Basic",
  "description":"Obtenga información sobre el formato de archivo VB y las API que pueden crear y abrir archivos VB",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo VB?

Un archivo VB es un archivo de código fuente creado en lenguaje Visual Basic creado por Microsoft para el desarrollo de aplicaciones .NET. Otro lenguaje similar con una sintaxis diferente es C#, cuyos archivos se guardan con la extensión de archivo [.CS](/es/programming/cs/). El formato de archivo proporciona el lenguaje de programación de bajo nivel para escribir código que se compila para generar el archivo de salida final en forma de EXE o DLL. Estos se pueden crear y compilar con Microsoft Visual Studio. Microsoft Visual Studio Express también se puede usar para crear y actualizar dichos archivos, que es un IDE gratuito. Un proyecto simple de Visual Studio [solución] (/es/programación/sln/) creado con el lenguaje VB puede comprender uno o más de estos archivos. Los archivos marcados para su inclusión en la compilación se enumeran en el archivo [CSPROJ](/es/programming/csproj/) que forma parte del proyecto y le dice al compilador que use los archivos marcados.

## Formato de archivo VB: más información

Los archivos VB son formatos de archivo basados en texto que se pueden abrir en cualquier editor de texto para editarlos. Sin embargo, cuando se abre en un IDE compatible con el resaltado de sintaxis adecuado, el código es fácil de leer y organizar. Un archivo VB simple contiene:

* Declaración de espacios de nombres: para referirse a una funcionalidad particular definida por ese espacio de nombres específico
* Declaración de variables: para declarar variables de nivel de clase para la implementación particular
* Declaración de métodos: para declarar la declaración de métodos para la funcionalidad particular

## Ejemplo de formato de archivo VB

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



