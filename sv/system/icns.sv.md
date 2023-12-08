{
"datum": "2023-03-08",
  "keywords": [
"icns fil",
"vad är en icns-fil",
"fil",
"icns filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "ICNS-filformat - macOS-ikonresurs",
  "description":"Läs mer om ICNS-format och API:er som kan skapa och öppna ICNS-filer.",
  "linktitle": "ICNS",
  "menu": {
    "docs": {
      "identifier": "system-icns",
      "parent": "system"
}
},
"lastmod": "2023-03-08"
}

## Vad är en ICNS fil?

En ICNS-fil är ett filformat som används på macOS för att lagra ikoner för program, mappar och andra objekt. Det är ett containerfilformat som kan innehålla flera bildstorlekar och upplösningar av samma ikon.

ICNS-filer innehåller vanligtvis bilder i flera upplösningar, från 16x16 pixlar till 1024x1024 pixlar, för att passa olika skärmstorlekar och upplösningar på macOS-enheter. Filformatet använder en komprimeringsalgoritm för att minska filstorleken på bilderna.

ICNS-filer kan skapas med hjälp av olika programvaruverktyg, såsom Icon Composer eller Sketch, och kan tilldelas olika objekt på ett macOS-system, som applikationer, mappar och dokument. När ett objekt väljs på ett macOS-system hämtar operativsystemet lämplig storlek och upplösning på ikonen från ICNS-filen och visar den på skärmen.

## ICNS-filformat - Mer information

ICNS-filer är containerfiler som kan innehålla flera bildstorlekar och upplösningar av samma ikon med en teknik som kallas "ikonfamilj". En ikonfamilj består av en grupp bildresurser som var och en representerar samma ikon men med olika storlekar eller upplösningar. Varje bildresurs inom en ikonfamilj har en unik typ och ID, som identifierar bildstorlek och upplösning. De olika bildstorlekarna och upplösningarna lagras i samma ICNS-fil med olika typer och ID:n.

När ett objekt väljs på ett macOS-system hämtar operativsystemet lämplig storlek och upplösning på ikonen från ICNS-filen med hjälp av dess typ och ID och visar den på skärmen. Detta gör att macOS-systemet kan visa högkvalitativa ikoner på skärmar med olika upplösningar, till exempel på Retina-skärmar, samtidigt som filstorleken är mindre.

ICNS-filer på macOS liknar .ICO-filer på Windows genom att de båda fungerar som filformat för lagring av ikoner. Precis som ICNS-filer kan ICO-filer innehålla flera bildstorlekar och upplösningar av samma ikon, som används för att visa ikonen på olika skärmstorlekar och upplösningar på Windows-enheter.

Det finns dock vissa skillnader mellan ICNS- och ICO-filer. Till exempel kan ICNS-filer lagra bilder med högre upplösning än ICO-filer, vilket gör dem bättre lämpade för användning på högupplösta skärmar, såsom Retina-skärmar på macOS-enheter. Dessutom kan ICNS-filer innehålla bilder med en alfakanal, vilket möjliggör transparenta bakgrunder, vilket inte stöds i ICO-filer.

## Referenser
* [ICNS-filformat](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)


