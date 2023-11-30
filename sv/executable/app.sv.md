{
"datum": "2023-02-02",
  "keywords": [
"app fil",
"vad är en app-fil",
"fil",
"hur man öppnar appfil",
"app filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
  "description":"Läs mer om APP-filformat och API:er som kan skapa och öppna APP-filer.",
"title": "APP-filformat - macOS Application Bundle",
"linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
      "parent": "executable"
}
},
"lastmod": "2023-02-02"
}

## Vad är en APP-fil?

En .app-fil på macOS är en speciell typ av katalog som innehåller alla filer som behövs för att köra ett specifikt program, inklusive den körbara koden, resurserna och metadata. Tillägget .app signalerar till operativsystemet att den här katalogen ska behandlas som en enda enhet, snarare än en samling separata filer, och att den kan startas direkt från Finder eller Dock.

Finder är standardfilhanteraren på macOS. Det låter dig bläddra och organisera filerna och katalogerna på din dator. Dock är en funktion i macOS som ger snabb åtkomst till ofta använda program och dokument. Både Finder och Dock låter dig starta applikationer genom att klicka på deras .app-filer, vilket öppnar motsvarande applikationspaket. När du startar en applikation körs den körbara koden i .app-paketet, vilket gör applikationen tillgänglig för användning. .app-filen är representationen av applikationen i filsystemet och ger användaren ett sätt att komma åt och starta applikationen.

När du högerklickar på en .app-fil i Finder på ett macOS-system och väljer "Visa paketinnehåll", kommer du att kunna se den interna strukturen för applikationspaketet. Detta är användbart om du vill komma åt resurser eller filer som används av programmet, eller om du vill inspektera innehållet i programmet i felsökningssyfte. Paketinnehållet i en .app-fil inkluderar vanligtvis kataloger för resurser som bilder och ljud, samt den körbara koden för programmet. Genom att utforska innehållet i en .app-fil kan du få djupare insikter i hur applikationen är sammansatt och vad den gör.

## Hur öppnar man filen APP?

För att öppna en .app-fil på macOS dubbelklickar du helt enkelt på filen i Finder. Detta kommer att starta programmet som finns i .app-paketet. Om programmet är installerat på ditt system och har associerats med .app-filtypen, bör du starta programmet automatiskt om du dubbelklickar på filen. Om programmet inte är associerat med .app-filtypen kan du behöva högerklicka på filen och välja "Öppna med" för att välja ett lämpligt program att öppna den med.

Du kan öppna en .app-fil på terminalen i macOS genom att använda kommandot "öppna". För att göra detta, navigera till katalogen där .app-filen finns med kommandot "cd" och kör sedan följande kommando:

```
open <AppName>.app 
```

var<AppName> är namnet på programmet du vill starta. Detta kommer att starta programmet som om du hade dubbelklickat på det i Finder. Kommandot "öppna" är ett allmänt verktyg som kan användas för att öppna många olika typer av filer, inklusive program, dokument och kataloger. När du använder kommandot "öppna" på en .app-fil, startar det programmet som finns i paketet.

## Referenser
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
