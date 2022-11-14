{
  "date" : "2021-04-08",
  "keywords" :[ "lz4-bestand", "lz4-bestandsindeling", "wat is een lz4-bestand", "bestand", "lz4-voorbeeld", "lz4-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - LZ4 gecomprimeerd bestandsformaat",
  "description":"Meer informatie over LBR-bestandsindeling en API's die LZ4-bestanden kunnen maken en openen.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Wat is een LZ4-bestand?

Een bestand met de extensie .lz4 is een gecomprimeerd archiefbestand dat is gemaakt met toepassingen/hulpprogramma's die [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))-compressie ondersteunen. Het LZ4-algoritme richt zich op de afweging tussen snelheid en compressieverhouding. Gecomprimeerde LZ4-archieven kunnen worden gemaakt met behulp van het LZ4-opdrachtregelhulpprogramma en kunnen met hetzelfde worden gedecomprimeerd.

## LZ4-bestandsindeling

Het LZ4-bestandsformaat, gebaseerd op het LZ4-compressiealgoritme, is onafhankelijk van het CPU-type, het besturingssysteem, het bestandssysteem en de tekenset. Het is geschikt voor bestandscompressie en streamingcompressie met behulp van het LZ4-algoritme. De initiële implementatie van het LZ4-formaat werd uitgevoerd in de taal [C](/nl/programming/c/) door Yann Collet in 2011 en is beschikbaar voor ontwikkelaarreferentie op [Github](https://github.com/lz4/lz4) .

### LZ4 Frame-indeling

De algemene structuur van het LZ4-bestandsformaat is zoals hieronder weergegeven.

|MagischNb|F. Descriptor| Blokkeren|(...)|EndMark |C. Controlesom|
---|---|---|---|---|---|
|4 bytes| 3-15 bytes||| 4 bytes| 0-4 bytes|

#### Magisch nummer

4 bytes, Little endian-formaat. Waarde: 0x184D2204

#### Framebeschrijving

De framedescriptor bestaat uit 3 tot 15 bytes en is het belangrijkste onderdeel van de specificaties. Samen worden de velden Magic_Number en Frame_Descriptor LZ4 Frame Header genoemd, en de grootte varieert tussen 7 en 19 bytes. Het is zoals hieronder weergegeven.

|FLG| BD| (Inhoudsgrootte)| (Woordenboek-ID)| HC|
---|---|---|---|---|
|1 byte| 1 byte| 0 - 8 bytes| 0 - 4 bytes| 1 byte|

#### Gegevensblokken

Elk gegevensblok volgt de volgende volgorde.

|Blokgrootte| gegevens| (Blokcontrolesom)|
---|---|---|
|4 bytes| |0 - 4 bytes|

#### EndMark

De stroom van blokken eindigt wanneer het laatste gegevensblok wordt gevolgd door de 32-bits waarde 0x00000000.

#### Inhoudscontrolesom

De Content_Checksum verifieert de geldigheid van de inhoud die correct wordt gedecodeerd en wordt uitgevoerd met behulp van het resultaat van het xxHash-32-algoritme. Het valideert de resultaten van een succesvolle verzending van alle blokken in de juiste volgorde en zonder fouten.

## Referenties

* [LZ4 Frame-indeling](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [LZ4-compressiealgoritme - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

