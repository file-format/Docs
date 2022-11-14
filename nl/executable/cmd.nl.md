{
  "date" : "2021-07-12",
  "keywords" :[ "cmd-bestand", "wat is een cmd-bestand", "bestand", "cmd-voorbeeld", "cmd-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over de CMD-bestandsindeling en API's die CMD-bestanden kunnen maken en openen.",
  "title" :"CMD - Windows-opdrachtbestandsindeling",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Wat is een CMD-bestand?
Een CMD-bestand bestaat uit een script met een of meerdere opdrachten in de vorm van platte tekst die worden uitgevoerd om verschillende taken uit te voeren. Het is vergelijkbaar met een [BAT](/nl/executable/bat/)-bestand, dat over het algemeen ook wordt gebruikt om een reeks uitvoerbare opdrachten op te slaan. De CMD-bestanden worden veel gebruikt in het Microsoft Windows-besturingssysteem. Deze bestanden zijn bijna in de jaren 90 geïntroduceerd, maar worden nog steeds gebruikt in het nieuwste Windows-besturingssysteem. Deze bestanden zijn over het algemeen geschreven om meer dan één opdracht achter elkaar uit te voeren.

## CMD-bestandsindeling
CMD is een bestandsindeling die wordt gebruikt door uitvoerbare programma's in CP/M-stijl. Het is over het algemeen vergelijkbaar met [COM](/nl/executable/com/) in CP/M-80 en [EXE](/nl/executable/exe/) in DOS. Een CMD-bestand bevat 1 tot 8 groepen code of gegevens en een header van 128 bytes. Elke groep kan maximaal 1 mb groot zijn. CMD-bestanden kunnen in latere versies ook verplaatsingsinformatie en Resident System Extensions (RSX's) bevatten. De CMD is een nieuwkomer in vergelijking met het [BAT](/nl/executable/bat/)-bestand; gebruikt voor MS-DOS vóór de release van Windows In MS-DOS. Hoewel u vandaag de dag nog steeds bestanden kunt opslaan met de extensie .bat, gebruiken veel mensen de extensie .cmd om hun uitvoerbare scripts op te slaan.

### CMD-formaat Specificatie:

Het begin van de koptekst bevat de lijst van de groepen die in het bestand aanwezig zijn, samen met hun typen. Elk type kan maximaal één keer worden gebruikt. Deze soorten zijn:

- Code
- Gegevens
- Extra's
- Stapel
- Gebruiker 1
- Gebruiker 2
- Gebruiker 3
- Gebruiker 4
- Gedeelde code

Evenzo Program Segment Prefix in DOS, de eerste 256 bytes van de datagroep zijn nul. Ze worden gevuld door CP/M-86 met de nulpagina. Als er geen datagroep is, worden in plaats daarvan de eerste 256 bytes van de codegroep gebruikt.
## CMD-bestand voorbeeld
Hieronder volgt een voorbeeld van een CMD-script om systeeminformatie weer te geven.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Referenties

* [Een CMD-script schrijven](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [CMD-bestand (CP/M) - door Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

