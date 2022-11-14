{
  "date" : "2022-04-01",
  "keywords" :[ "nkit file", "nkit file format", "wat is een nkit file", "file", "nkit example", "nkit file extension","extension", "format", "nkit footer", "file formaat van nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Meer informatie over NKIT-bestandsindelingen en API's die NKIT-bestanden kunnen maken en openen.",
  "title" :"NKIT - Bestandsindeling schijfkopie",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Wat is een NKIT-bestand?

Een NKIT-bestand is een schijfkopie van gegevens die zijn geëxtraheerd uit NintendoWii- en GameCube-spellen. NKIT is voor Nintendo Toolkit-formaat. Het resulterende compressiebestand [ISO](/nl/compression/iso/) gebruikt de belangrijkste gegevens van deze spellen om te worden uitgevoerd met emulatorprogramma's zoals Dolphin, Swiss en Nintendont. NKit wordt geleverd in onbewerkte (iso) en gecomprimeerde (gcz) bestandsindelingen die beide zijn ontworpen om de speelbaarheid en grootte in het oog te houden.

## NKIT-bestandsindeling

NKit-bestandsindeling is een indeling zonder verlies en wordt gebruikt voor het verkleinen en herstellen van Nintendo Wii- en GameCube-afbeeldingen. De formaten zijn beschikbaar in ISO- en GCZ-bestandsformaten voor elk van de GameCube- en Wii-spellen.

|Systeem |Formaat |Hardware ondersteund |Dolphin ondersteund |Restorable 1:1 |Notes|
---|---|---|---|---|---|
|GameCube| nkit.iso| Ja |Ja| Ja |Zelfde als gecomprimeerde GameCube iso|
|GameCube| nkit.gcz| Nee| Ja| Ja |GCZ is Dolphin's eigen doorzoekbare compressieformaat voor blokken|
|Wii| nkit.iso| Nee Ja| Ja| RVT-H-formaat alleen speelbaar in Dolphin|
|Wii| nkit.gcz| Nee Ja| Ja| RVT-H in GCZ alleen speelbaar in Dolphin|

### NKIT-koptekst

De header van het NKIT-bestandsformaat is als volgt.

|Offset |Lengte |Naam|
---|---|---|
|0x200 |0x4 |NKit Header 'NKIT'|
|0x204 |0x4 |NKit-versie ' v01'|
|0x208 |0x4 |Bronafbeelding origineel CRC32|
|0x20C |0x4 |NKit CRC - maakt het NKit-bestand CRC32 gelijk aan de bron-CRC op 0x208 (op 0x4 in GCZ)|
|0x210 |0x4 |Bron afbeelding lengte|
|0x214 |0x4 |Geforceerde junk-ID (wanneer schijf-ID verschilt - zeldzaam - alleen GameCube)|
|0x218 |0x4 |Wii-partitie CRC32 bijwerken indien verwijderd bij conversie|

## Referenties ##

* [NKIT-bestandsindeling - door gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

