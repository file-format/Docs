{
"date": "2023-05-15",
  "keywords": [
"csx-fil",
"vad är en csx-fil",
"vad innehåller csx-filen",
"vilket är formatet på csx-filen",
"fil",
"csx filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CSX-filformat - Visual C# Script",
  "description":"Läs mer om CSX-format och API:er som kan skapa och öppna CSX-filer.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
      "parent": "programming"
}
},
"lastmod": "2023-05-15"
}

## Vad är en CSX fil?

Visual C# Script (även känt som CSX) är ett filformat som används av Roslyns skriptmotor i Microsofts .NET-ekosystem. CSX-filer innehåller C#-kod som kan exekveras direkt utan behov av separat kompileringssteg.

CSX-format är specifikt för Microsofts ekosystem och inte ett allmänt använt filformat i allmän programmering. CSX-filer används ofta i scenarier där snabb prototyp- eller skriptfunktionalitet krävs. De gör att du kan skapa och köra C#-program på ett mer lättviktigt sätt jämfört med att skapa en fullfjädrad kompilerad applikation.

För att köra CSX-filer kan du använda verktyg som .NET Interactive Notebooks, som tillhandahåller en interaktiv miljö för att köra C#-kod. Visual Studio Code med tillägget C# och .NET Core SDK kan också användas för att arbeta med CSX-filer.

## Vad innehåller CSX-filen?

En CSX-fil (C# Script) innehåller C#-kod som kan köras direkt. Den kan inkludera vilken giltig C#-kod som helst som variabeldeklarationer, funktioner, klasser och andra programmeringskonstruktioner.

Här är ett exempel på vad CSX-fil kan innehålla:

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

CSX-filer kan också innehålla importsatser, externa biblioteksreferenser och andra C#-språkfunktioner för att stödja kodens funktionalitet. Koden tolkas och exekveras i farten utan behov av kompilering, vilket gör den lämplig för skript och snabba prototypuppgifter.

## Vilket är formatet på filen CSX?

Formatet CSX (C# Script) följer ett enkelt textbaserat format. Den har vanligtvis filtillägget .csx för att skilja den från vanliga C#-källkodsfiler (.cs).

CSX-filer kan redigeras med valfri textredigerare eller integrerad utvecklingsmiljö (IDE) som stöder C#-syntaxmarkering. När CSX-filen är klar kan den köras med hjälp av verktyg som .NET Interactive Notebooks, .NET Core kommandoradsgränssnitt (CLI) eller en IDE med C#-skriptstöd.

## Referenser
* [C#-programmering med Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

