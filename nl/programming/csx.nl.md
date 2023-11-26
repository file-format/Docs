{
"datum": "15-05-2023",
  "keywords": [
"csx-bestand",
"wat is een csx-bestand",
"wat bevat het csx-bestand",
"wat is het formaat van het csx-bestand",
"bestand",
"csx bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"CSX-bestandsindeling - visueel C#-script",
  "description":"Leer meer over het CSX-formaat en API's waarmee CSX-bestanden kunnen worden gemaakt en geopend.",
"linktitel": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
"parent":"programmeren"
}
},
"laatste mod": "2023-05-15"
}

## Wat is een CSX-bestand?

Visual C# Script (ook bekend als CSX) is een bestandsindeling die wordt gebruikt door de Roslyn-scriptengine in het .NET-ecosysteem van Microsoft. CSX-bestanden bevatten C#-code die direct kan worden uitgevoerd zonder dat er een aparte compilatiestap nodig is.

Het CSX-formaat is specifiek voor het Microsoft-ecosysteem en geen veelgebruikt bestandsformaat bij algemene programmering. CSX-bestanden worden vaak gebruikt in scenario's waarin snelle prototyping- of scriptfunctionaliteit vereist is. Ze stellen u in staat om C#-programma's op een lichtere manier te maken en uit te voeren vergeleken met het maken van een volwaardige gecompileerde applicatie.

Om CSX-bestanden uit te voeren, kunt u tools zoals .NET Interactive Notebooks gebruiken, die een interactieve omgeving bieden voor het uitvoeren van C#-code. Visual Studio Code met de C#-extensie en .NET Core SDK kan ook worden gebruikt om met CSX-bestanden te werken.

## Wat bevat het CSX-bestand?

Een CSX-bestand (C# Script) bevat C#-code die direct kan worden uitgevoerd. Het kan elke geldige C#-code bevatten, zoals variabeledeclaraties, functies, klassen en andere programmeerconstructies.

Hier is een voorbeeld van wat het CSX-bestand zou kunnen bevatten:

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

CSX-bestanden kunnen ook importinstructies, externe bibliotheekreferenties en andere C#-taalfuncties bevatten om de functionaliteit van de code te ondersteunen. De code wordt on-the-fly geïnterpreteerd en uitgevoerd zonder dat compilatie nodig is, waardoor deze geschikt is voor scripting en snelle prototyping-taken.

## Wat is het formaat van een CSX-bestand?

Het CSX-formaat (C# Script) volgt het eenvoudige, op tekst gebaseerde formaat. Het heeft doorgaans de bestandsextensie .csx om het te onderscheiden van gewone C#-broncodebestanden (.cs).

CSX-bestanden kunnen worden bewerkt met elke teksteditor of geïntegreerde ontwikkelomgeving (IDE) die C#-syntaxisaccentuering ondersteunt. Zodra het CSX-bestand gereed is, kan het worden uitgevoerd met behulp van tools zoals .NET Interactive Notebooks, de .NET Core opdrachtregelinterface (CLI) of een IDE met ondersteuning voor C#-scripts.

## Referenties
* [C# programmeren met Visual Studio Code](https://code.visualstudio.com/docs/linguals/csharp)

