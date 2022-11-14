{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "bestand", "extensie", "bestandsindeling", "Visual Basic", "Programmeergids" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Visual Basic-codebestand",
  "description":"Meer informatie over VB-bestandsindelingen en API's die VB-bestanden kunnen maken en openen.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een VB-bestand?

Een VB-bestand is een broncodebestand gemaakt in Visual Basic-taal dat door Microsoft is gemaakt voor de ontwikkeling van .NET-toepassingen. Een andere vergelijkbare taal met een andere syntaxis is C# waarvan de bestanden zijn opgeslagen met de bestandsextensie [.CS](/nl/programming/cs/). Het bestandsformaat biedt de programmeertaal op laag niveau voor het schrijven van code die is gecompileerd om het uiteindelijke uitvoerbestand te genereren in de vorm van EXE of een DLL. Deze kunnen worden gemaakt en gecompileerd met Microsoft Visual Studio. Microsoft Visual Studio Express kan ook worden gebruikt om dergelijke bestanden te maken en bij te werken, wat een gratis IDE is. Een eenvoudig Visual Studio-project [oplossing](/nl/programming/sln/) gemaakt met VB-taal kan uit een of meer van dergelijke bestanden bestaan. Bestanden die zijn gemarkeerd voor opname in compilatie worden weergegeven in het bestand [CSPROJ](/nl/programming/csproj/) dat deel uitmaakt van het project en de compiler vertelt om de gemarkeerde bestanden te gebruiken.

## VB-bestandsindeling - Meer informatie

VB-bestanden zijn op tekst gebaseerde bestandsindelingen die in elke teksteditor kunnen worden geopend om te bewerken. Wanneer de code echter wordt geopend in een ondersteunde IDE met de juiste syntaxisaccentuering, is de code gemakkelijk te lezen en te rangschikken. Een eenvoudig VB-bestand bevat:

* Naamruimtedeclaratie - Voor het verwijzen naar een bepaalde functionaliteit gedefinieerd door die specifieke naamruimte
* Variabelendeclaratie - Om variabelen op klasseniveau te declareren voor de specifieke implementatie
* Methodenverklaring - Om methodeverklaring voor de specifieke functionaliteit te declareren:

## Voorbeeld van VB-bestandsindeling

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



