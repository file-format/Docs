{
  "date" : "2019-12-09",
  "keywords" :[ "zip-bestand", "zip-bestandsformaat", "wat is een zip-bestand", "bestand", "zip-voorbeeld", "zip-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIP",
  "description":"Wat is een ZIP-bestand en API's die ZIP-bestanden kunnen maken en openen.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Wat is een ZIP-bestand? ##

Een bestand met de extensie .zip is een archief dat een of meer bestanden of mappen kan bevatten. Het archief kan compressie hebben toegepast op de opgenomen bestanden om de ZIP-bestandsgrootte te verkleinen. Het ZIP-bestandsformaat werd in februari 1989 openbaar gemaakt door Phil Katz voor het archiveren van bestanden en mappen. Het formaat is onderdeel gemaakt van het hulpprogramma [PKZIP](https://www.pkware.com/pkzip), gemaakt door PKWARE, Inc. Direct na de beschikbaarheid van [beschikbare specificaties](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), maakten veel bedrijven het ZIP-bestandsformaat onderdeel van hun softwarehulpprogramma's, waaronder Microsoft (sinds Windows 7), Apple (Mac OS X) en vele anderen.

## Korte geschiedenis van ZIP-bestandsindeling

De geschiedenis van het ZIP-bestandsformaat gaat terug tot het geval van een rechtszaak die werd aangespannen door System Enhancement Associates (SEA) tegen PKWARE voor het gebruik van het ARC-hulpprogramma zonder toestemming voor zijn handelsmerk en de auteursrechten van het uiterlijk en de gebruikersinterface van het product. Daarvoor had Phil Katz de broncode van SEA herschreven en PKXARC, een ARC-extractor, en PKARC, een bestandscompressor, uitgebracht als freeware voor op MS-DOS gebaseerde systemen. PKWARE verloor van de rechtszaak en kon niets meer gebruiken dat met ARC te maken had. Dit is waar de creatie van een nieuwe bestandscompressie tot stand kwam, genaamd ZIP, die onderdeel werd van het PKZIP-hulpprogramma bij PKWARE, Inc.

Katz heeft de specificaties van het ZIP-bestandsformaat vrijgegeven in het publieke domein, met behoud van de eigendomsrechten op zijn compressie- en extractiehulpprogramma, namelijk PKZIP. Het ZIP-compressiesysteem was (en is) in staat om bestanden in een map te archiveren door middel van een 32-bits cyclische redundantiecontrole ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) algoritme om het bestand te comprimeren maten. In tegenstelling tot ARC bevatten .ZIP-mappen een directorybestand dat de rol speelde van het codeboek van een cryptograaf, met de informatie die nodig is om de gecomprimeerde bestanden weer te geven.

## Ondersteunde compressiemethoden in ZIP

Volgens de specificaties van de .ZIP-bestandsindeling worden de volgende compressiemethoden ondersteund.

* Opslaan - impliceert geen compressie
* Krimpen
* Reductie (Dit impliceert compressiefactoren variërend van niveau 1 tot niveau 4)
* Imploderen
* Leeglopen
* Deflat64
*BZIP2
* LZMA (EFS)
* WavPack
* PPMd versie I, Rev 1

DEFLATE is de veelgebruikte compressiemethode, een lossless datumcompressiealgoritme dat een combinatie van de LZ77- en Huffman-codering gebruikt en wordt beschreven in [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Specificaties ZIP-bestandsindeling

ZIP-bestanden hebben de mogelijkheid om meerdere bestanden op te slaan met behulp van verschillende compressietechnieken en ondersteunen tegelijkertijd het opslaan van een bestand zonder enige compressie. Elk bestand wordt afzonderlijk opgeslagen/gecomprimeerd, wat helpt om ze uit te pakken of nieuwe toe te voegen, zonder compressie of decompressie toe te passen op het hele archief.

### Algemeen ZIP-bestandsformaat

Elk zip-bestand is als volgt gestructureerd:


|ZIP-bestandsindeling
---|
|Lokale bestandskop 1
|Bestandsgegevens 1
|Gegevensbeschrijving 1
|Lokale bestandskop 2
|Bestandsgegevens 2
|Gegevensbeschrijving 2
| ....
| ....
|Lokale bestandskop N
|Bestandsgegevens nr
|Gegevensbeschrijving nr
|Archief decoderingskoptekst
|Archief extra gegevensrecord
|Centraal telefoonboek

ZIP-bestandsindeling gebruikt een 32-bits CRC-algoritme voor archiveringsdoeleinden. Om de gecomprimeerde bestanden weer te geven, bevat een ZIP-archief een map aan het einde die de vermelding van de ingesloten bestanden en hun locatie in het archiefbestand bewaart. Het speelt dus de rol van codering voor het inkapselen van informatie die nodig is om de gecomprimeerde bestanden weer te geven. ZIP-lezers gebruiken de map om de lijst met bestanden te laden zonder het hele ZIP-archief te lezen. Het formaat bewaart dubbele kopieën van de directorystructuur om een betere bescherming te bieden tegen gegevensverlies.

Elk bestand in een ZIP-archief wordt weergegeven als een afzonderlijk item waarbij elk item bestaat uit een Local File Header gevolgd door de gecomprimeerde bestandsgegevens. De directory aan het einde van het archief bevat de verwijzingen naar al deze bestandsitems. ZIP-bestandslezers moeten het lezen van de lokale bestandsheaders vermijden en alle soorten bestandslijsten moeten uit de directory worden gelezen. Deze directory is de enige bron voor geldige bestandsinvoer in het archief, aangezien bestanden ook tegen het einde van het archief kunnen worden toegevoegd. Dat is de reden waarom als een lezer vanaf het begin lokale headers van een ZIP-archief leest, deze ongeldige (verwijderde) vermeldingen ook kan lezen die geen deel uitmaken van de directory die uit het archief wordt verwijderd.

De volgorde van de bestandsitems in de centrale directory hoeft niet samen te vallen met de volgorde van de bestandsitems in het archief.

### ZIP-bestandsvermeldingen

De vermeldingen in het ZIP-bestand zijn achter elkaar gerangschikt, waarbij elke vermelding bestaat uit:

* Lokale bestandskop
* Optionele extra gegevensvelden
* Gebruikersgegevens (optioneel gecomprimeerd/optioneel versleuteld)

De lokale bestandskop van elk item vertegenwoordigt informatie over het bestand, zoals commentaar, bestandsgrootte en bestandsnaam. De extra gegevensvelden (optioneel) kunnen informatie bevatten voor uitbreidbaarheidsopties van het ZIP-formaat.

#### Lokale bestandskop

De Local File Header heeft een specifieke veldstructuur die bestaat uit waarden van meerdere bytes. Alle waarden worden opgeslagen in little-endian bytevolgorde waarbij de veldlengte de lengte in bytes telt. Alle structuren in een ZIP-bestand gebruiken handtekeningen van 4 bytes voor elke bestandsinvoer. Het einde van de handtekening van de centrale directory is 0x06054b50 en kan worden onderscheiden met behulp van zijn eigen unieke handtekening. Hieronder volgt de volgorde van de informatie die is opgeslagen in Local File Header.


|Offset|Bytes|Beschrijving
---|---|---|
|0|4|Lokale bestandskophandtekening # 0x04034b50 (lees als een little-endian-nummer)
|4|2|Versie nodig om te extraheren (minimaal)
|6|2|Bitvlag voor algemeen gebruik
|8|2|Compressiemethode
|10|2|Laatste wijzigingstijd ingeven
|12|2|Laatste wijzigingsdatum invullen
|14|4|CRC-32
|18|4|Gecomprimeerde grootte
|22|4|Ongecomprimeerde grootte
|26|2|Bestandsnaam lengte (n)
|28|2|Extra veldlengte (m)
|30|n|Bestandsnaam
|30+n|m|Extra veld

#### Centrale map Bestandskop


|Offset|Bytes|Beschrijving
---|---|---|
|0|4|Centrale directory bestandsheader handtekening # 0x02014b50
|4|2|Versie gemaakt door
|6|2|Versie nodig om te extraheren (minimaal)
|8|2|Bitvlag voor algemeen gebruik
|10|2|Compressiemethode
|12|2|Laatste wijzigingstijd ingeven
|14|2|Laatste wijzigingsdatum invullen
|16|4|CRC-32
|20|4|Gecomprimeerde grootte
|24|4|Ongecomprimeerde grootte
|28|2|Bestandsnaam lengte (n)
|30|2|Extra veldlengte (m)
|32|2|Lengte van bestandscommentaar (k)
|34|2|Schijfnummer waar het bestand begint
|36|2|Interne bestandskenmerken
|38|4|Externe bestandskenmerken
|42|4|Relatieve offset van lokale bestandskop. Dit is het aantal bytes tussen het begin van de eerste schijf waarop het bestand voorkomt en het begin van de lokale bestandskop. Hierdoor kan software de centrale directory lezen om de positie van het bestand in het ZIP-bestand te lokaliseren.
|46|n|Bestandsnaam
|46+n|m|Extra veld
|46+n+m|k|Bestand toevoegen

#### Einde van centraal telefoonboekrecord


|Offset|Bytes|Beschrijving
---|---|---|
|0|4|Einde van handtekening centrale directory # 0x06054b50
|4|2|Nummer van deze schijf
|6|2|Schijf waar de centrale directory begint
|8|2|Aantal centrale directory-records op deze schijf
|10|2|Totaal aantal centrale telefoonboekrecords
|12|4|Grootte van centrale directory (bytes)
|16|4|Verschuiving van begin van centrale directory, ten opzichte van begin van archief
|20|2|Commentaar lengte (n)
|22|n|Commentaar

## Referenties

* [PKWARE ZIP-bestandsformaatspecificaties](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Structuur van PKZip-bestand](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)
