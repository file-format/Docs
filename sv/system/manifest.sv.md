{
"datum": "2023-03-07",
  "keywords": [
"manifest fil",
"vad är en manifestfil",
"fil",
"manifest filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "MANIFEST-filformat - Windows Application Manifest-fil",
  "description":"Läs mer om MANIFEST-format och API:er som kan skapa och öppna MANIFEST-filer.",
  "linktitle": "MANIFEST",
  "menu": {
    "docs": {
      "identifier": "system-manifest",
      "parent": "system"
}
},
"lastmod": "2023-03-07"
}

## Vad är en MANIFEST fil?

En manifestfil är en fil som innehåller information om ett program eller ett paket. Filen heter vanligtvis filtillägget .manifest. Manifestfilen ger information om filerna som ingår i paketet, deras versionsnummer och eventuella beroenden som paketet har till andra programvarukomponenter.

Manifestfiler används vanligtvis på Windows-plattformen för att säkerställa att program är korrekt installerade och konfigurerade. De kan användas för att specificera saker som vilka versioner av delade bibliotek som ska användas, vilka konfigurationsfiler som ska inkluderas och vilka registernycklar som ska ändras under installationen.

Utöver Windows kan manifestfiler användas även i andra sammanhang, till exempel för webbapplikationer eller Android-applikationer. Det specifika formatet och innehållet i en manifestfil beror på plattformen och applikationen som paketeras.

## Mer information

Manifestfiler är i XML-format. XML är ett allmänt använt märkningsspråk för att skapa strukturerade dokument och data, och det används ofta i mjukvaruutveckling för att beskriva konfigurationer, inställningar och annan metadata.

I samband med programvaror innehåller en manifest XML-fil vanligtvis information om programmets beroenden, versionsinformation och andra konfigurationsinställningar. Filen används för att säkerställa att applikationen är korrekt installerad och att den har alla nödvändiga komponenter och resurser för att fungera korrekt.

Manifest XML-filen kan inkluderas i applikationspaketet eller som en separat fil som laddas ner under installationen. Den kallas vanligtvis med filtillägget ".manifest" och följer ett specifikt format som definieras av plattformen eller ramverket som applikationen är byggd på.

Till exempel, i Microsoft .NET Framework, används en manifest XML-fil för att beskriva beroenden och versionsinformation för ett program, och det ingår vanligtvis som en del av programmets sammansättning. Filen används av Common Language Runtime (CLR) för att fastställa de korrekta versionerna av sammansättningar som ska laddas och för att säkerställa att applikationen körs korrekt.

## Referenser
* [Manifestfil](https://en.wikipedia.org/wiki/Manifest_file)

