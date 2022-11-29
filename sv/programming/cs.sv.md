{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "fil", "tillägg", "filformat", "CSharp", "Programmeringsspråk" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - CSharp Code File",
  "description":"Läs mer om CS-filformat och API:er som kan skapa och öppna CS-filer.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en CS fil?

Filer med filtillägget .cs är källkodsfiler för programmeringsspråket C#. Introducerat av Microsoft för användning med .NET Framework, tillhandahåller filformatet lågnivåprogrammeringsspråket för att skriva kod som kompileras för att generera den slutliga utdatafilen i form av EXE eller en DLL. Dessa kan skapas och kompileras med Microsoft Visual Studio. Microsoft Visual Studio Express kan också användas för att skapa och uppdatera sådana filer som är en gratis IDE. CS-filer används för applikationsutveckling som kan sträcka sig från enkla skrivbordsapplikationer till mer komplexa program. Ett enkelt Visual Studio-projekt [lösning](/sv/programmering/sln/) skapat med C#-språk kan bestå av en eller flera sådana filer. Filer markerade för att inkluderas i kompilering listas i filen [CSPROJ](/sv/programming/csproj/) som är en del av projektet och säger åt kompilatorn att använda de markerade filerna.

## CS-filformat ##

CS-filer är textbaserade filformat som kan öppnas i vilken textredigerare som helst för redigering. Men när den öppnas i en stödd IDE med korrekt syntaxmarkering är koden lätt att läsa och ordna. En enkel CS-fil innehåller:

* Namnutrymmesdeklaration - För att referera till en viss funktionalitet som definieras av det specifika namnområdet
* Variabeldeklaration - För att deklarera klassnivåvariabler för den specifika implementeringen
* Metoddeklaration - För att deklarera metoddeklaration för den specifika funktionaliteten

### Syntax ###

* Semikolon används för att beteckna slutet av ett påstående.
* Lockiga parenteser används för att gruppera uttalanden. Påståenden grupperas vanligtvis i metoder (funktioner), metoder i klasser och klasser i namnutrymmen.
* Variabler tilldelas med ett likhetstecken, men jämförs med två på varandra följande likhetstecken.
* Hakparenteser används med arrayer, både för att deklarera dem och för att få ett värde vid ett givet index i en av dem.

### Exempel ###

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

