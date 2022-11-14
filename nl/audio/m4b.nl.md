{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "bestand", "extensie", "formaat", "wat is m4b-bestandsformaat", "muziek", "m4b-bestandsformaat", "M4b vs MP3", "specificatie m4b-bestandsformaat "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over M4B-bestandsindelingen en API's die M4B-bestanden kunnen maken, converteren en openen.",
  "title" :"M4B - MPEG-4 Audioboek-bestandsindeling",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Wat is een M4B-bestand?

Het bestand met de extensie .m4b is een audioboek dat over het algemeen wordt gebruikt door Apple Books en iTunes. De audio die in dit formaat wordt gebruikt, wordt opgeslagen in MPEG-4 en gecomprimeerd met behulp van AAC-codering. Een M4B-bestand lijkt erg op M4A, maar ondersteunt de audioboekgerelateerde functies, zoals bladwijzers en hoofdstukafbrekingen. De M4B-bestanden zijn beschikbaar in zowel DRM-enabled als DRM-vrije versies. DRM-gecodeerde audioboeken zijn meestal betaalde audioboeken van de iTunes Store. Terwijl DRM-vrij gemakkelijk via internet te vinden is.

## M4B-bestandsindeling

De audioboekbestanden die metadata, afbeeldingen, bladwijzers en hyperlinks bevatten, kunnen worden opgeslagen met de extensie .m4a, maar over het algemeen wordt de extensie .m4b gebruikt tijdens het opslaan, alleen om aan te geven dat het bestand een audioboekbestandsindeling heeft. Fairplay DRM (Digital Rights Management) wordt gebruikt door Apply om hun M4B-bestanden te beschermen. De bestanden die zijn gedownload van iTunes kunnen dus alleen worden afgespeeld op geautoriseerde apparaten of computers.


## M4B versus M4A

Zowel M4B als [MP3](https://docs.fileformat.com/audio/mp3/) zijn bestandsindelingen met alleen audio.

**M4B**: wint in vergelijking met MP3 in termen van kwaliteit als beide met dezelfde bitsnelheid worden gecodeerd. De M4B is een audioboekbestand dat is gecomprimeerd met AAC-codering. Het wordt in feite geassocieerd met "MPEG-4 Audio Layer", bestanden met de extensie .m4b zijn de audiolaag van MPEG-4-films, maar met extra audioboekgerelateerde functies. Het doel is om MP3 in te halen en de nieuwe standaard te worden in audiocompressie. Het ligt in veel opzichten dicht bij MP3, maar is ontwikkeld om een betere kwaliteit te hebben in dezelfde of zelfs kleinere bestandsgrootte. Het M4B-formaat werd voor het eerst geïntroduceerd door Apple. Het formaattype wordt ook gerealiseerd als de Apple lossless Encoder (ALE).

Daarom kon de M4B momenteel niet het mainstream-succes van de MP3 krijgen, omdat het audioformaat nog niet algemeen kan worden afgespeeld.

**Mp3**: een digitaal audioformaat dat iedereen goed kent. Een allereerste compressieformaat op het toneel en werd erg beroemd onder muziekluisteraars. Het mainstream-succes is zo snel dat het bestandstype universeel kan worden afgespeeld en compatibel is met bijna alles, hardware of software. In algemene zin zal de M4A een betere geluidskwaliteit produceren, maar velen zouden beweren dat, of het waar is of niet, het geluidsverschil niet vergelijkbaar is, en het zou tijdverspilling zijn om MP3-bestanden naar M4A-bestanden te converteren. Ten slotte zorgt de conversie ervoor dat u de oorspronkelijke geluidskwaliteit verliest.

## Specificatie van M4B-bestandsindeling

Net als bij [M4A](/nl/audio/m4a/), bestaan de M4B-bestanden ook uit opeenvolgende chunks. Elke chunk heeft een header van 8 bytes en is onderverdeeld als:
- Brokkengrootte van 4 bytes (big-endian, eerst hoge byte)
- 4-byte chunk-type - een van de vooraf gedefinieerde handtekeningen: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "skip", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT ", "scpt", "ssrc".

Net als bij M4A is de eerste chunk in M4B van het type "ftype" en heeft een subtype op offset 8. De M4B gedefinieerd door subtype dat "M4B_" moet zijn.

Het herhalen van chunks, totdat een onbekend type wordt gedetecteerd, zal het een M4B-bestand (MPEG-4 Audio) samenstellen.

## Referenties

* [MPEG-4 Deel 14 - Door Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery-voorbeeld](https://www.file-recovery.com/m4a-signature-format.htm)

