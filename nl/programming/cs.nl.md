{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "bestand", "extensie", "bestandsformaat", "CSharp", "Programmeertaal"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - CSharp-codebestand",
  "description":"Meer informatie over CS-bestandsindeling en API's die CS-bestanden kunnen maken en openen.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een CS-bestand?

Bestanden met de extensie .cs zijn broncodebestanden voor de programmeertaal C#. Geïntroduceerd door Microsoft voor gebruik met het .NET Framework, biedt het bestandsformaat de programmeertaal op laag niveau voor het schrijven van code die is gecompileerd om het uiteindelijke uitvoerbestand te genereren in de vorm van EXE of een DLL. Deze kunnen worden gemaakt en gecompileerd met Microsoft Visual Studio. Microsoft Visual Studio Express kan ook worden gebruikt om dergelijke bestanden te maken en bij te werken, wat een gratis IDE is. CS-bestanden worden gebruikt voor applicatieontwikkeling die kan variëren van eenvoudige desktopapplicaties tot complexere programma's. Een eenvoudig Visual Studio-project [oplossing](/nl/programming/sln/) gemaakt met C#-taal kan uit een of meer van dergelijke bestanden bestaan. Bestanden die zijn gemarkeerd voor opname in compilatie worden weergegeven in het bestand [CSPROJ](/nl/programming/csproj/) dat deel uitmaakt van het project en de compiler vertelt om de gemarkeerde bestanden te gebruiken.

## CS-bestandsindeling ##

CS-bestanden zijn op tekst gebaseerde bestandsindelingen die in elke teksteditor kunnen worden geopend om te bewerken. Wanneer de code echter wordt geopend in een ondersteunde IDE met de juiste syntaxisaccentuering, is de code gemakkelijk te lezen en te rangschikken. Een eenvoudig CS-bestand bevat:

* Naamruimtedeclaratie - Voor het verwijzen naar een bepaalde functionaliteit gedefinieerd door die specifieke naamruimte
* Variabelendeclaratie - Om variabelen op klasseniveau te declareren voor de specifieke implementatie
* Methodenverklaring - Om methodeverklaring voor de specifieke functionaliteit te declareren:

### Syntaxis ###

* Puntkomma's worden gebruikt om het einde van een instructie aan te duiden.
* accolades worden gebruikt om uitspraken te groeperen. Verklaringen worden gewoonlijk gegroepeerd in methoden (functies), methoden in klassen en klassen in naamruimten.
* Variabelen worden toegewezen met een isgelijkteken, maar vergeleken met twee opeenvolgende isgelijktekens.
* Vierkante haken worden gebruikt bij arrays, zowel om ze te declareren als om een waarde te krijgen bij een bepaalde index in een ervan.

### Voorbeeld ###

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

