{
  "date" : "2021-08-27",
  "keywords" :[ "wsh-fil", "wsh-filformat", "vad är en wsh-fil", "fil", "wsh-exempel", "wsh-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om WSH-filformat och API:er som kan skapa och öppna WSH-filer.",
  "title" :"WSH - Windows Script File",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## Vad är WSH fil?
En fil med filtillägget .wsh innehåller egenskaper och parametrar för ett visst programmeringsspråksskript som VB eller VBS etc. Det faktiska behovet av WSH är att använda dem för att anpassa exekveringen av vissa skript. WScript eller CScript krävs för att köras och båda dessa ingår i Windows operativsystem. WSH-filer tillhandahölls från början på Windows 95 på installationsskivorna som en valfri konfigurerbar och installerbar för kontrollpanelen, och sedan en standardkomponent i Windows 98.

## WSH filformat
WSH (Windows Script Host) kan användas för olika ändamål, inklusive administration, inloggningsskript och allmän automatisering. WSH etablerar en miljö för skript att köra. den anropar den lämpliga skriptmotorn och allokerar en uppsättning tjänster och objekt för skriptet att arbeta med. Dessa skript kan köras i GUI-läge, från ett COM-objekt eller kommandoradsläge, vilket ger användaren flexibilitet för både interaktiva och icke-interaktiva skript.

### Exempel
Här är ett mycket enkelt exempel som visar något VBScript som använder rot WSH COM-objektet "WScript" för att visa ett meddelande med en 'OK'-knapp. När detta skript kommer att startas kommer CScript- eller WScript-motorn att anropas och runtime-miljön kommer att etableras.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Referenser

* [Windows Script Host - av Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)



