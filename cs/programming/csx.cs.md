{
"datum": "2023-05-15",
  "keywords": [
"csx soubor",
"co je soubor csx",
"co obsahuje soubor csx",
"jaký je formát souboru csx",
"soubor",
"přípona souboru csx",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru CSX - Visual C# Script",
  "description":"Další informace o formátu CSX a rozhraních API, která mohou vytvářet a otevírat soubory CSX.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
      "parent": "programming"
}
},
"lastmod": "2023-05-15"
}

## Co je soubor CSX?

Visual C# Script (také známý jako CSX) je formát souboru používaný skriptovacím strojem Roslyn v ekosystému .NET společnosti Microsoft. Soubory CSX obsahují kód C#, který lze spustit přímo bez nutnosti samostatného kompilačního kroku.

Formát CSX je specifický pro ekosystém společnosti Microsoft a není široce používaným formátem souborů v obecném programování. Soubory CSX se často používají ve scénářích, kde je vyžadována funkce rychlého prototypování nebo skriptování. Umožňují vám vytvářet a spouštět programy C# jednodušším způsobem ve srovnání s vytvářením plnohodnotné kompilované aplikace.

Ke spouštění souborů CSX můžete použít nástroje jako .NET Interactive Notebooks, které poskytují interaktivní prostředí pro spouštění kódu C#. Pro práci se soubory CSX lze také použít Visual Studio Code s příponou C# a .NET Core SDK.

## Co obsahuje soubor CSX?

Soubor CSX (C# Script) obsahuje kód C#, který lze přímo spustit. Může obsahovat jakýkoli platný kód C#, jako jsou deklarace proměnných, funkce, třídy a další programovací konstrukce.

Zde je příklad toho, co může soubor CSX obsahovat:

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

Soubory CSX mohou také obsahovat příkazy importu, odkazy na externí knihovny a další funkce jazyka C# pro podporu funkčnosti kódu. Kód je interpretován a spouštěn on-the-fly bez nutnosti kompilace, takže je vhodný pro skriptování a úlohy rychlého prototypování.

## Jaký je formát souboru CSX?

Formát CSX (C# Script) následuje jednoduchý textový formát. Obvykle má příponu souboru .csx, aby se odlišil od běžných souborů zdrojového kódu C# (.cs).

Soubory CSX lze upravovat pomocí libovolného textového editoru nebo integrovaného vývojového prostředí (IDE), které podporuje zvýrazňování syntaxe C#. Jakmile je soubor CSX připraven, lze jej spustit pomocí nástrojů jako .NET Interactive Notebooks, rozhraní příkazového řádku .NET Core (CLI) nebo IDE s podporou skriptování v C#.

## Reference
* [Programování v C# s kódem Visual Studio](https://code.visualstudio.com/docs/languages/csharp)

