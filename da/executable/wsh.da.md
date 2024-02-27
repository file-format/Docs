{
  "date": "2021-08-27",
  "keywords": [
"wsh filen",
"wsh filformat",
"hvad er en wsh-fil",
"fil",
"wsh eksempel",
"wsh filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om WSH-filformat og API'er, der kan oprette og åbne WSH-filer.",
  "title": "WSH - Windows Script-fil",
  "linktitle": "WSH",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-dah"
}
},
  "lastmod": "2021-08-27"
}

## Hvad er WSH fil?
En fil med filtypenavnet .wsh indeholder egenskaber og parametre for et bestemt programmeringssprog script såsom VB eller VBS osv. Det faktiske behov for WSH er at bruge dem til at tilpasse udførelsen af visse scripts. WScript eller CScript er påkrævet for at køre, og begge disse er inkluderet i Windows-operativsystemet. WSH-filer blev oprindeligt leveret på Windows 95 på installationsdiskene som en valgfri konfigurerbar og installerbar for kontrolpanelet og derefter en standardkomponent i Windows 98.

## WSH filformat
WSH (Windows Script Host) kan bruges til forskellige formål, herunder administration, logon scripts og generel automatisering. WSH etablerer et miljø, hvor scripts kan køre. det påkalder den passende script-motor og tildeler et sæt tjenester og objekter, som scriptet kan arbejde med. Disse scripts kan køres i GUI-tilstand fra et COM-objekt eller kommandolinjetilstand, hvilket giver fleksibilitet til brugeren for både interaktive eller ikke-interaktive scripts.

### Eksempler
Her er et meget simpelt eksempel, som viser noget VBScript, som bruger rod WSH COM-objektet WScript til at vise en besked med en 'OK'-knap. Når dette script vil blive lanceret, vil CScript- eller WScript-motoren blive kaldt, og runtime-miljøet vil blive etableret.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Referencer 

* [Windows Script Host - af Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)




