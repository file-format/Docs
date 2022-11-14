{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "extensie", "bestand", "formaat", "systeem", "TMP-bestand", "TMP-documenten", "TMP-bestanden", "Tijdelijk bestand", "toepassing", "programma's" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Tijdelijk bestandsformaat",
  "description":"Meer informatie over TMP-bestandsindelingen en API's die TMP-bestanden kunnen maken en openen.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Wat is een TMP-bestand? ##

Een TMP-bestand verwijst naar een tijdelijke back-up, opslag of ander bestandssysteem gegenereerd door een softwareprogramma. Het wordt af en toe gemaakt als een onzichtbaar bestand en wordt vaak vernietigd wanneer het programma wordt afgesloten. TMP-bestanden kunnen ook worden gebruikt om tijdelijk informatie op te slaan terwijl een nieuw bestand wordt gemaakt.

## TMP-bestandsindeling ##

Een TMP-bestand bestaat meestal uit onbewerkte gegevens die worden gebruikt als een fase in het conversieproces van materiaal van de ene stijl naar de andere. Microsoft Word en Apple Safari zijn twee apps die het TMP-bestandsformaat kunnen produceren en gebruiken.

Gegenereerde TMP-documenten zouden in theorie automatisch moeten worden verwijderd wanneer het programma wordt afgesloten of de machine wordt uitgeschakeld. In de praktijk is dit niet altijd het geval. Als gevolg hiervan kunt u tijdens het navigeren door de documenten van uw programma tijdelijke bestanden tegenkomen die niet actief door het systeem of andere software worden gebruikt.

### Hulpgeheugen ###

Virtueel geheugen wordt gebruikt in besturingssystemen, maar programma's die enorme hoeveelheden informatie gebruiken, moeten mogelijk tijdelijke documenten maken.

### Communicatie tussen processen ###

De meeste besturingssystemen bieden primitieven voor het doorgeven van gegevens tussen programma's, zoals buizen, sockets of het hoofdgeheugen, maar de eenvoudigste methode is om bestanden over te zetten naar een tijdelijk bestand en de ontvangende toepassing te informeren over de locatie van het tijdelijke bestand.


## Technische specificatie ##

Het verkrijgen van onderscheidende tijdelijke documentnamen wordt meestal geleverd door besturingssystemen en softwareprogramma's.
Tijdelijke bestanden kunnen veilig worden gegenereerd op POSIX-systemen met behulp van de bibliotheekfuncties mkstemp of tmpfile. Sommige systemen bevatten de vorige POSIX (inmiddels verdwenen) mktemp-toepassing. Deze bestanden zijn meestal te vinden in de reguliere tijdelijke map op Unix-platforms in /TMP, of %TEMP% (het is specifiek voor inloggen) op Windows-machines.

Wanneer het programma stopt of het document wordt gesloten, wordt het tijdelijke bestand dat met het tmp-bestand is gegenereerd, automatisch verwijderd. GetTempFileName (Windows) of tmpnam (POSIX) kan worden gebruikt om een tijdelijke bestandsnaam te maken die langer meegaat dan het programma dat deze heeft gemaakt.

## Referentie ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
