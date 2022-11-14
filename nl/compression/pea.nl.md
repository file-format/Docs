{
  "date" : "2021-04-21",
  "keywords" :[ "pea file", "pea file format", "wat is een pea file", "file", "pea example", "pea file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - PeaZip Archief Bestandsformaat",
  "description":"Meer informatie over PEA-bestandsindeling en API's die PEA-bestanden kunnen maken en openen.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Wat is een PEA-bestand?

Een bestand met de extensie .pea, acroniem voor Pack, Encrypt, and Authenticate, is een [zip](/nl/compression/zip/)-archief gemaakt met de [PeaZip](https://peazip.github.io/) archiveringssoftwaretoepassing. Het beschikt over compressie en uitvoer van meerdere volumes, en biedt een flexibel beveiligingsmodel door middel van geauthenticeerde versleuteling en cryptografie. Dit zorgt voor zowel privacy als authenticatie van de gegevens. Het PeaZip-hulpprogramma is beschikbaar als open-source-engine die kan worden gecompileerd voor verschillende besturingssystemen volgens de vereisten.

## PEA-bestandsindeling

De [PEA-specificaties voor bestandsindelingen](https://peazip.github.io/pea_help.pdf) zijn openbaar beschikbaar ter referentie van de ontwikkelaar. PEA-archieven zijn binaire bestanden met een flexibel beveiligingsmodel en redundante integriteitscontroles, variërend van checksums tot cryptografisch sterke hashes. Dit definieert drie verschillende communicatieniveaus die moeten worden beheerd:

* Streams - de feitelijke uitvoergegevensstroom die wordt gevormd door meerdere invoerbestanden en kan worden geschreven naar meerdere uitvoervolumes
* Objecten - invoerbestanden en mappen verzonden naar .pea-archief
* Volumes - uitvoerarchiefbestand dat kan worden overspannen tot door de gebruiker gedefinieerde grootte

Elk van deze is optioneel en kan worden opgenomen volgens de vereisten van de gebruiker. Het PEA-bestandsformaat kan een enkele stream met onbeperkte objecten opslaan. Elke stream is maximaal 2^64 bytes groot.

PEA-bestanden bieden optionele integriteitscontrole en geverifieerde codering met AES in EAX- of HMAC-modus, of Twofish en Serpent in EAX-modus.

### PEA Archief Header

De archiefkop is 10 bytes en is als volgt opgebouwd.

|Bytes|Beschrijving|
---|---|
|1 | Magisch byteveld voor het ondubbelzinnig maken van bestandsformaat: $EA|
|1 | Versienummer|
|1 | Revisienummer|
|1 | Volumeregeling |
|1 | Het besturingssysteem aangeven waar de stream is gebouwd|
|1 | Datum- en tijdcodering van het besturingssysteem aangeven|
|1 | Declareren van objecten naam tekencodering|
|1 | CPU-type aangeven (gecodeerd in 7 bit) en endianness (in msb)|
|1 | Gereserveerd voor toekomstig gebruik|

## Referenties

* [PEA-bestandsindelingspecificaties](https://peazip.github.io/pea_help.pdf)
* [PEA-bestandsindeling](https://peazip.github.io/pea-file-format.html#.pea_specifications)

