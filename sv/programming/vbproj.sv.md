{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "fil", "tillägg", "filformat", "VB-projektfil", "Programmeringsguide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Läs mer om VBPROJ-filformat och API:er som kan skapa och öppna VBPROJ-filer.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Vad är en VBPROJ fil?

En fil med tillägget .vbproj är en Microsoft Visual Basic-projektfil som används av Microsofts MSBuild-motor för att bygga projekten i en Visual Studio-lösning. Den liknar filen [CSPROJ](/sv/programming/csproj/) för .NET-projekt skrivna i [C#](/sv/programming/cs/). MSBuild-motorn läser information som finns i olika grupper från VBPROJ-filerna och genererar utdatafilen. En VBPROJ-fil kan innehålla information relaterad till globala identifierare, klasser och egenskaper som definierar projektet. VBPROJ-filer kan öppnas och redigeras med hjälp av Microsoft Visual Studio och alla vanliga textredigerare som Anteckningar på Windows och MacOS operativsystem.

## VBPROJ-filformat - Mer information

VBPROJ-filer är textfiler som är skrivna i [XML](/sv/web/xml/) filformat baserat på [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). En VBPROJ-fil innehåller information i form av XML-taggar som definierar information relaterad till den specifika gruppen av inställningar. Det rekommenderas starkt att öppna och redigera dessa inställningsfiler i Microsoft Visual Studio IDE.

### VBPROJ-element

Beståndsdelarna i en VB-inställningsfil är som visas i följande bild.

{{< figure src="../vbproj.png" alt="VBPROJ filformat" >}}

Följande tabell ger en kort beskrivning av dessa element.

|Element|Beskrivning|
---|---|
|Projekt| Rotelement i varje projektfil och kan inkludera attribut för att specificera startpunkterna för byggprocessen förutom att identifiera XML-schemat för projektfilen|
|Egenskaper och villkor| Egenskaper består av nyckel-värdepar och definieras i ett PropertyGroup-element. Egenskapselementets namn representerar egenskapsnyckeln och innehållet i elementet definierar egenskapsvärdet.|
|Items and ItemGroups|Objekt i en projektfil är indata till byggprocessen såsom filkodfiler, konfigurationsfiler, kommandofiler och annat som krävs som en del av byggprocessen. Objekt är och måste definieras inom ett ItemGroup-element.|
|Mål och uppgifter| Ett uppgiftselement representerar en individuell bygginstruktion (eller uppgift). MSBuild innehåller en mängd fördefinierade uppgifter som Copy, CSC, VBC, Exec. Uppgifter måste alltid finnas i ett `Target`-element som är en uppsättning av en eller flera uppgifter som exekveras sekventiellt, och en projektfil kan innehålla flera mål.|

## Referenser

* [Förstå projektfilen](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [MSBuild Schema Elements](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

