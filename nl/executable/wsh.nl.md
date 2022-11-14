{
  "date" : "2021-08-27",
  "keywords" :[ "wsh-bestand", "wsh-bestandsformaat", "wat is een wsh-bestand", "bestand", "wsh-voorbeeld", "wsh-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over WSH-bestandsindeling en API's die WSH-bestanden kunnen maken en openen.",
  "title" :"WSH - Windows-scriptbestand",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## Wat is een WSH-bestand?
Een bestand met de extensie .wsh bevat eigenschappen en parameters voor een bepaald programmeertaalscript zoals VB of VBS enz. De werkelijke behoefte van WSH is om ze te gebruiken voor het aanpassen van de uitvoering van bepaalde scripts. WScript of CScript zijn vereist om te worden uitgevoerd en beide zijn inbegrepen bij het Windows-besturingssysteem. WSH-bestanden werden aanvankelijk geleverd op Windows 95 op de installatieschijven als optioneel configureerbaar en installeerbaar voor het Configuratiescherm, en vervolgens een standaardonderdeel van Windows 98.

## WSH-bestandsindeling
WSH (Windows Script Host) kan voor verschillende doeleinden worden gebruikt, waaronder administratie, aanmeldingsscripts en algemene automatisering. WSH creëert een omgeving waarin scripts kunnen worden uitgevoerd. het roept de geschikte script-engine aan en wijst een set services en objecten toe aan het script om mee te werken. Deze scripts kunnen worden uitgevoerd in GUI-modus, vanuit een COM-object of opdrachtregelmodus, waardoor de gebruiker flexibiliteit krijgt voor zowel interactieve als niet-interactieve scripts.

### Voorbeelden
Hier is een heel eenvoudig voorbeeld dat wat VBScript toont dat het root WSH COM-object "WScript" gebruikt om een bericht weer te geven met een 'OK'-knop. Wanneer dit script wordt gestart, wordt de CScript- of WScript-engine aangeroepen en wordt de runtime-omgeving tot stand gebracht.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Referenties

* [Windows Script Host - door Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)



