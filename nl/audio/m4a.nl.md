{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "bestand", "extensie", "formaat", "wat is m4a-bestandsformaat", "muziek", "m4a-bestandsformaat", "M4A vs MP3", "specificatie m4a-bestandsformaat "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over M4A-bestandsindeling en API's die M4A-bestanden kunnen maken, converteren en openen.",
  "title" :"M4A - MPEG-4 audiobestand",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Wat is een M4A-bestand?

De **M4A-bestandsindeling** is een audiobestand dat is gemaakt met behulp van AAC (Advanced Audio Coding), wat bekend staat als compressie met verlies. Het woord M4A afgekort als MPEG 4 Audio. Deze audiobestanden hebben meestal de bestandsextensie .m4a. Dit geldt met name voor niet-beveiligde inhoud. Het kan verschillende soorten audio-inhoud opslaan, zoals audioboeken, liedjes en podcasts. M4A wordt meestal gerealiseerd als een geavanceerder formaat dan MP3, dat niet typisch was ontworpen voor alleen audio. Het is slechts een audiolaag in MPEG 1- of 2-videobestanden.

Het M4A-formaat is gecodeerd door FairPlay Digital Rights Management, aangezien het via de iTunes Store werd verkocht met de .m4p-extensie. De Apple iPhones gebruiken MPEG-4-audio voor hun beltonen, maar die audiobestanden gebruiken de .m4r-extensie.


## M4A versus MP3

Zowel M4A als [MP3](https://docs.fileformat.com/audio/mp3/) zijn bestandsindelingen met alleen audio.

**M4A**: Beter dan MP3 in termen van kwaliteit en grootte bij codering met dezelfde bitsnelheid. De bestandsextensie .m4a is zo gewoon omdat ze door Apple zijn gebruikt voor gebruik in de iTunes Music Store. De M4A is een audiobestand dat is gecomprimeerd met behulp van MPEG-4-technologie; een algoritme voor lossy compressie. Het wordt in feite geassocieerd met "MPEG-4 Audio Layer", bestanden met de extensie .m4a zijn de audiolaag van MPEG-4-films. Het is bedoeld om MP3 in te halen en de nieuwe standaard te worden in audiocompressie. Het komt in veel opzichten dicht bij MP3, maar is geïntroduceerd om een betere kwaliteit te hebben in een zelfde of zelfs kleinere bestandsgrootte. Het M4A-formaat werd voor het eerst geïntroduceerd door Apple. Het formaattype wordt ook gerealiseerd als de Apple lossless Encoder (ALE).

Daarom kon de M4A momenteel niet het mainstream-succes van de MP3 krijgen, omdat het audioformaat over het algemeen nog niet kan worden afgespeeld. Het is op de een of andere manier alleen beperkt tot MacOS, iPod en andere Apple-producten.

**Mp3**: het meest bekende digitale audioformaat. Het was ook een van de eerste compressieformaten in de scene en werd erg populair onder muziekliefhebbers. Het mainstream-succes is zo snel dat het bestandstype universeel en met bijna alles kan worden afgespeeld, hardware of software. In algemene zin zal de M4A een betere geluidskwaliteit produceren, maar velen zouden beweren dat, of het waar is of niet, het geluidsverschil niet te onderscheiden is, en het zou tijdverspilling zijn om MP3-bestanden naar M4A-bestanden te converteren. Uiteindelijk zal de conversie ervoor zorgen dat je de oorspronkelijke geluidskwaliteit verliest.

## Specificatie van M4A-bestandsindeling

De M4A-bestanden bestaan uit opeenvolgende chunks. Elke chunk heeft een header van 8 bytes en is onderverdeeld als:
- Brokkengrootte van 4 bytes (big-endian, eerst hoge byte)
- 4-byte chunk-type - een van de vooraf gedefinieerde handtekeningen: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

Het eerste blok is van het type "ftype" en heeft een subtype op offset 8. De M4A gedefinieerd door het subtype moet "M4A_" zijn, voor M4B moet het subtype "M4B_" zijn en voor M4P moet het subtype "M4P_" zijn.

Het herhalen van chunks, totdat een onbekend type wordt gedetecteerd, zal het een M4A-bestand (MPEG-4 Audio) samenstellen.

## Referenties ##

* [MPEG-4 Deel 14 - Door Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery-voorbeeld](https://www.file-recovery.com/m4a-signature-format.htm)

