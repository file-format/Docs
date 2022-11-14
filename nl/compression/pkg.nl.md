{
  "date" : "2021-04-08",
  "keywords" :[ "pkg-bestand", "pkg-bestandsformaat", "wat is een pkg-bestand", "bestand", "pkg-voorbeeld", "pkg-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Uitbreidbaar archiefbestandsformaat",
  "description":"Meer informatie over PKG-bestandsindeling en API's die PKG-bestanden kunnen maken en openen.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Wat is een PKG-bestand?

Een bestand met de extensie .pkg is een installatiepakketbestand dat wordt gebruikt om software op macOS te installeren. Naast Macintosh-computers wordt het ook op de iPhone gebruikt. De ingebouwde Apple-installatietoepassing kan worden gebruikt om de inhoud van een PKG-bestand te installeren. Een PKG-bestand is vergelijkbaar met een MSI-bestand dat in het Windows-besturingssysteem wordt gebruikt voor de installatie van software. Tijdens de installatie kunnen deze pakketbestanden berichten loggen die u een idee geven welke extra dingen door dit pakket worden geïnstalleerd.

## PKG-bestandsindeling

PKR zijn binaire bestanden die zijn gecomprimeerd om de totale bestandsgrootte te verkleinen. Sinds OSX 10.5 zijn door Apple platte pakketten met enkele installatiebestanden geïntroduceerd. Deze zijn anders dan de eerdere verpakkingsformaten die als bundels werden geleverd in plaats van afzonderlijke bestanden. Deze gebundelde pakketten bevatten een gestructureerde directoryhiërarchie waarin bestanden werden opgeslagen op een manier die het ophalen ervan via een indexbestand vergemakkelijkt. Het platte PKG-bestandsformaat is eigenlijk een [XAR](/nl/compression/xar/)-archief met een:

* Header - Definieert de grootte, controlesom en versie-informatie
* Inhoudsopgave - Een XML-document dat is (en moet) worden gecodeerd als UTF-8 en wordt opgeslagen aan het begin van het bestand, waardoor het gemakkelijk is om door het archief te scannen om een afzonderlijk bestand uit te pakken
* Heap - ongestructureerde hoop gegevens waarnaar wordt verwezen door de TOC

## Referenties

* [Flat Package File Format](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

