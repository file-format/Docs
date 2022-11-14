{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "archivo", "extensión", "formato de archivo", "CSharp", "Lenguaje de programación" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - Archivo de código CSharp",
  "description":"Obtenga información sobre el formato de archivo CS y las API que pueden crear y abrir archivos CS",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo CS?

Los archivos con extensión .cs son archivos de código fuente para el lenguaje de programación C#. Introducido por Microsoft para su uso con .NET Framework, el formato de archivo proporciona el lenguaje de programación de bajo nivel para escribir código que se compila para generar el archivo de salida final en forma de EXE o DLL. Estos se pueden crear y compilar con Microsoft Visual Studio. Microsoft Visual Studio Express también se puede usar para crear y actualizar dichos archivos, que es un IDE gratuito. Los archivos CS se utilizan para el desarrollo de aplicaciones que pueden variar desde aplicaciones de escritorio simples hasta programas más complejos. Un proyecto simple de Visual Studio [solución](/es/programación/sln/) creado con el lenguaje C# puede incluir uno o más de estos archivos. Los archivos marcados para su inclusión en la compilación se enumeran en el archivo [CSPROJ](/es/programming/csproj/) que forma parte del proyecto y le dice al compilador que use los archivos marcados.

## Formato de archivo CS ##

Los archivos CS son formatos de archivo basados en texto que se pueden abrir en cualquier editor de texto para editarlos. Sin embargo, cuando se abre en un IDE compatible con el resaltado de sintaxis adecuado, el código es fácil de leer y organizar. Un archivo CS simple contiene:

* Declaración de espacios de nombres: para referirse a una funcionalidad particular definida por ese espacio de nombres específico
* Declaración de variables: para declarar variables de nivel de clase para la implementación particular
* Declaración de métodos: para declarar la declaración de métodos para la funcionalidad particular

### Sintaxis ###

* Los puntos y comas se utilizan para indicar el final de una declaración.
* Los corchetes se utilizan para agrupar declaraciones. Las declaraciones se agrupan comúnmente en métodos (funciones), métodos en clases y clases en espacios de nombres.
* Las variables se asignan usando un signo de igual, pero se comparan usando dos signos de igual consecutivos.
* Los corchetes se usan con arreglos, tanto para declararlos como para obtener un valor en un índice dado en uno de ellos.

### Ejemplo ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

