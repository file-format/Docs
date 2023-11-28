{
"fecha": "2023-05-15",
  "keywords": [
"archivo csx",
"¿Qué es un archivo csx?",
"¿Qué contiene el archivo csx?",
"¿Cuál es el formato del archivo csx?",
"archivo",
"extensión de archivo csx",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo CSX - Script de Visual C#",
  "description":"Obtenga más información sobre el formato CSX y las API que pueden crear y abrir archivos CSX.",
"linktitle" :  "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
"parent" : "programming"
}
},
"última modificación": "2023-05-15"
}

## ¿Qué es un archivo CSX?

Visual C# Script (también conocido como CSX) es un formato de archivo utilizado por el motor de secuencias de comandos Roslyn en el ecosistema .NET de Microsoft. Los archivos CSX contienen código C# que se puede ejecutar directamente sin necesidad de un paso de compilación por separado.

El formato CSX es específico del ecosistema de Microsoft y no es un formato de archivo ampliamente utilizado en la programación general. Los archivos CSX se utilizan a menudo en escenarios donde se requiere la creación rápida de prototipos o funcionalidad de secuencias de comandos. Le permiten crear y ejecutar programas C# de una manera más liviana en comparación con la creación de una aplicación compilada completa.

Para ejecutar archivos CSX, puede utilizar herramientas como .NET Interactive Notebooks, que proporcionan un entorno interactivo para ejecutar código C#. Visual Studio Code con la extensión C# y .NET Core SDK también se puede utilizar para trabajar con archivos CSX.

## ¿Qué contiene el archivo CSX?

Un archivo CSX (C# Script) contiene código C# que se puede ejecutar directamente. Puede incluir cualquier código C# válido, como declaraciones de variables, funciones, clases y otras construcciones de programación.

A continuación se muestra un ejemplo de lo que podría contener el archivo CSX:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

Los archivos CSX también pueden incluir declaraciones de importación, referencias de bibliotecas externas y otras características del lenguaje C# para respaldar la funcionalidad del código. El código se interpreta y ejecuta sobre la marcha sin necesidad de compilación, lo que lo hace adecuado para tareas de creación rápida de scripts y prototipos.

## ¿Cuál es el formato del archivo CSX?

El formato CSX (C# Script) sigue un formato simple basado en texto. Por lo general, tiene la extensión de archivo .csx para diferenciarlo de los archivos de código fuente C# normales (.cs).

Los archivos CSX se pueden editar utilizando cualquier editor de texto o entorno de desarrollo integrado (IDE) que admita el resaltado de sintaxis de C#. Una vez que el archivo CSX esté listo, se puede ejecutar utilizando herramientas como .NET Interactive Notebooks, la interfaz de línea de comandos (CLI) de .NET Core o un IDE con soporte para secuencias de comandos C#.

## Referencias
* [Programación C# con Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

