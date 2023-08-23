{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "fil", "tillägg", "filformat", "Visual Basic", "Programmeringsguide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Visual Basic Code File",
  "description":"Läs mer om VB-filformat och API:er som kan skapa och öppna VB-filer.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är VB fil?

En VB-fil är en källkodsfil skapad i Visual Basic-språket som skapades av Microsoft för utveckling av .NET-applikationer. Ett annat liknande språk med annan syntax är C# vars filer sparas med filtillägget [.CS](/sv/programming/cs/). Filformatet tillhandahåller programmeringsspråket på låg nivå för att skriva kod som kompileras för att generera den slutliga utdatafilen i form av EXE eller en DLL. Dessa kan skapas och kompileras med Microsoft Visual Studio. Microsoft Visual Studio Express kan också användas för att skapa och uppdatera sådana filer som är en gratis IDE. Ett enkelt Visual Studio-projekt [lösning](/sv/programming/sln/) skapat med VB-språk kan bestå av en eller flera sådana filer. Filer markerade för att inkluderas i kompilering listas i filen [CSPROJ](/sv/programming/csproj/) som är en del av projektet och säger åt kompilatorn att använda de markerade filerna.

## VB-filformat - Mer information

VB-filer är textbaserade filformat som kan öppnas i vilken textredigerare som helst för redigering. Men när den öppnas i en stödd IDE med korrekt syntaxmarkering är koden lätt att läsa och ordna. En enkel VB-fil innehåller:

* Namnutrymmesdeklaration - För att referera till en viss funktionalitet som definieras av det specifika namnområdet
* Variabeldeklaration - För att deklarera klassnivåvariabler för den specifika implementeringen
* Metoddeklaration - För att deklarera metoddeklaration för den specifika funktionaliteten

## Exempel på VB-filformat

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



