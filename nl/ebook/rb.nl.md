{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "Nuvo Media's Rocket eBook-apparaat", "bestand", "extensie", "format", "eBook"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over het RB-bestandsformaat voor Nuvo Media's Rocket eBook-apparaat en API's die RB-bestanden kunnen maken en openen.",
  "title" :"RB - Rocket eBook-bestand",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Wat is een RB-bestand?

Het bestand met de extensie .rb bevat de Rocket eBook-inhoud. Het Rocket eBook is eigenlijk een apparaat gemaakt door Nuvo Media; ze hebben dit apparaat in 1998 uitgebracht. Hoewel Rocket eBook in staat is om afbeeldingen weer te geven, maar alleen in zwart-witweergave. Het heeft een scherm van 106 dpi of 480 x 320 pixels op een 4,5 x 3-inch touchscreen. Het Rocket eBook maakt verbinding met een computer via een seriële poortverbinding om eBooks in RB-bestandsindeling te downloaden. De RB-bestanden kunnen DRM gebruiken, maar deze technologie wordt niet gebruikt in moderne eBooks. Het RB-bestand bevat conventioneel een HTML-bestand met de afbeeldingen en een pseudo-OPF-bestand met alle metadata (.info).

## Technische specificatie van RB-bestandsindeling ##

Een magisch getal (in hex) verschijnt in de eerste 4 bytes van het bestand: B0 0C B0 0C.

Het lijkt erop dat de volgende twee bytes een versienummer zijn, zoals "02 00", wat staat voor hoofdversie 2 en secundaire versie 0.

De volgende vier bytes bevatten de tekst "NUVO", gevolgd door 4 bytes van 00h.

De volgende 4-byte is de datum waarop het boek is gemaakt, gecodeerd als een int16. Dit brengt ons op offset 0Eh. De oude versie van ORocketLibrary codeerde de volledige waarde van het jaar (dwz 1999 was "CF 07", 2000 was "D0 07"). In de recente versie wordt tm_year letterlijk opgeslagen, dwz 100 voor het jaar 2000 ("64 00"). Na het jaar komt een int8 die het 1-relatieve maandnummer vertegenwoordigt, en een int8 die de dag van de maand vertegenwoordigt.

De volgende 6 bytes zijn 00h. Voor het instellen van de tijd kunnen deze worden gereserveerd.

De absolute offset van de "Table of Contents" is opgenomen in een int32 op offset 18h.

Hierna is een int32 die de lengte van het .rb-bestand bevat. Dit wordt gebruikt om te bepalen of de bestanden compleet zijn of niet.

Dit hele stuk bytes (20u tot 128u) lijkt alleen nodig te zijn voor een titel die is gecodeerd. In niet-gecodeerde titels zijn ze altijd nul.

In de meeste gevallen volgt de inhoudsopgave (bij offset 128). Het begint met een int32-telling van het aantal "pagina"-items (.rb-bestandsecties) in de inhoudsopgave. Elk item bestaat uit een naam (zero-padded tot 32 bytes), gevolgd door 3 int32s: de lengte van het gegevenssegment, de positie in het .rb-bestand en een vlag voor dit item. Vanaf vandaag zijn de bekende waarden: 1 (versleuteld), 2 (informatiepagina) en 8 (leeggelopen). De namen zijn, indien nodig, allemaal op maat gemaakt om ervoor te zorgen dat ze allemaal uniek zijn.

## Referenties

* [E-Reader - Door MobileRead](https://en.wikipedia.org/wiki/E-reader)

