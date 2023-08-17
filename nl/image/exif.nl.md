{
  "date" : "2019-10-11",
  "keywords" :[ "exif-bestand", "exif-bestandsindeling", "wat is een exif-bestand", "bestand", "exif-voorbeeld", "exif-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Meer informatie over EXIF-bestandsindeling en API's die EXIF-bestanden kunnen maken en openen.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een EXIF-bestand?
EXIF staat voor "Exchangeable Image File Format", de definitie die voor het eerst werd gegeven door [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) in 1985. De standaard wordt beheerd door Japan Electronics en Information Technology Industries Association (JEITA) vanaf vandaag. EXIF is een standaard voor de specificaties van beeld- en geluidsformaten die voornamelijk worden gebruikt door digitale camera's en scanners.

EXIF-standaard omvat de tagging en metadata-informatie met het afbeeldingsbestand. Metagegevens kunnen informatie bevatten zoals cameramodel, sluitertijd, datum en tijd, diafragma, fabrikant, belichtingstijd, X-resolutie, Y-resolutie enz. Normaal gesproken zijn de EXIF-gegevens standaard verborgen. Om de EXIF-gegevens te bekijken, moet men de weergave-eigenschappen selecteren in de toepassing voor het bekijken van afbeeldingen. Exif-metagegevens kunnen ook miniaturen bevatten, samen met technische en primaire afbeeldingsgegevens in een enkel afbeeldingsbestand.

## Geschiedenis en versies ##

* In oktober 1995 stelde JEIDA versie 1 op. In deze versie definieerde JEIDA de structuur, die bestaat uit het beeldgegevensformaat en attribuutinformatie, en basistags.
* Nov 1997, versie 1.1 werd geïntroduceerd met de meeste tags van versie 1, maar er werden ook voorzieningen toegevoegd voor optionele attribuutinformatie en formaatbewerking.
* Juni 1998, versie 2 met sRGB-kleurruimte, gecomprimeerde miniaturen en audiobestanden.
* December 1998, versie 2.1 met verbeterde opslag- en attribuutinformatie.
* Februari 2002, versie 2.2, verbeterde versie 2.1 met toevoeging van printafwerking.
* September 2003, versie 2.21 met optionele kleurruimte bekend als Adobe RGB.

## EXIF-bestandsindeling

EXIF gebruikt de volgende bestandsformaten met toevoeging van specifieke metadata.

1. [JPEG](/nl/image/jpeg/) - discrete cosinustransformatie (DCT) voor gecomprimeerde afbeeldingsbestanden.
1. [TIFF](/nl/image/tiff/) Rev. 6.0 (RGB of YCbCr) voor niet-gecomprimeerde afbeeldingsbestanden.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) voor audiobestanden (Lineair [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) of ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM voor ongecomprimeerde audiogegevens, en [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) voor gecomprimeerde audiogegevens).

### Markering gebruikt door EXIF ###

De markering 0xFFE0~~0xFFEF is "Application Marker", gebruikt door de gebruikerstoepassing. Oudere digicams gebruiken bijvoorbeeld JFIF (JPEG File Interchange Format) voor het opslaan van afbeeldingen. JFIF gebruikt APP0 (0xFFE0) Marker voor het invoegen van digi cam-configuratiegegevens en miniatuurafbeelding. Verder gebruikt EXIF ook een Application Marker voor het invoegen van gegevens, maar EXIF gebruikt APP1 (0xFFE1) Marker om een conflict met het JFIF-formaat te voorkomen. Elke EXIF-bestandsindeling begint met deze indeling.


|SOI-markering|APP1-markering|APP1-gegevens|Andere markering
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Het begint bij SOI (0xFFD8) Marker, dus het is een JPEG-bestand. Dan volgt direct APP1 Marker. Alle gegevens van EXIF worden opgeslagen in dit APP1-gegevensgebied. Het deel van "SSSS" op de bovenste tabel betekent de grootte van het APP1-gegevensgebied (EXIF-gegevensgebied). Houd er rekening mee dat de grootte "SSSS" ook de grootte van de descriptor zelf omvat. Na de "SSSS" starten de APP1-gegevens. Het eerste deel is een speciaal gegeven voor de identificatie of EXIF of niet, ASCII-teken "EXIF" en 2 bytes van 0x00 worden gebruikt. Na het APP1-markeringsgebied volgen de andere JPEG-markeringen.

### Exif-gegevensstructuur ###

Een ruwe structuur van EXIF-gegevens (APP1) wordt hieronder weergegeven. Zoals hierboven besproken, beginnen EXIF-gegevens vanaf ASCII-teken "EXIF" en 2 bytes van 0x00, daarna volgen EXIF-gegevens. EXIF gebruikt het TIFF-formaat om gegevens op te slaan.


|FFE1|APP1-markering
---|---|
|SSSS|APP1-gegevens|APP1-gegevensgrootte
|45786966 0000|Exif-koptekst
|49492A00 08000000|TIFF-koptekst
|XXXX. . . .|IFD0 (hoofdafbeelding)|Directory
|LLLLLLLL|Link naar IFD1
|XXXX. . . .|Gegevensgebied van IFD0
|XXXX. . . .|Exif SubIFD|Directory
|00000000|Einde van koppeling
|XXXX. . . .|Gegevensgebied van Exif SubIFD
|XXXX. . . .|IFD1(miniatuurafbeelding)|Directory
|00000000|Einde van koppeling
|XXXX. . . .|Gegevensgebied van IFD1
|FFD8XXXX. . . XXXFFD9|Miniatuurafbeelding

#### TIFF-koptekst ####

De 8-byte [TIFF](/nl/image/tiff/) bestandskop bevat de volgende informatie:

`Bytes 0-1:` De bytevolgorde die in het bestand wordt gebruikt. Wettelijke waarden zijn:“II”(4949.H)“MM” (4D4D.H).

In het "II"-formaat is de bytevolgorde altijd van de minst significante byte tot de meest significante byte, voor zowel 16-bits als 32-bits gehele getallen. Dit wordt de little-endian bytevolgorde genoemd. In de "MM"-indeling is de bytevolgorde altijd van meest significant tot minst significant, voor zowel 16-bits als 32-bits gehele getallen. Dit wordt big-endian bytevolgorde genoemd.

`Bytes 2-3:` Een willekeurig maar zorgvuldig gekozen nummer (42) dat het bestand verder identificeert als een TIFF-bestand. De bytevolgorde hangt af van de waarde van Bytes 0-1.

`Bytes 4-7:` De offset (in bytes) van de eerste IFD. De map mag zich op elke locatie in het bestand na de koptekst bevinden, maar moet beginnen op een woordgrens. In het bijzonder kan een afbeeldingsbestandsdirectory de afbeeldingsgegevens volgen die het beschrijft. Lezers moeten de aanwijzers volgen waar ze ook heen leiden. De term byte-offset wordt in dit document altijd gebruikt om te verwijzen naar een locatie ten opzichte van het begin van het TIFF-bestand. De eerste byte van het bestand heeft een offset van 0.

#### Afbeeldingsbestandsmap ####

Een IFD bevat informatie over de afbeelding en verwijzingen naar de daadwerkelijke afbeeldingsgegevens. Het bestaat uit een 2-byte telling van het aantal directory-items (dwz het aantal velden), gevolgd door een reeks van 12-byte-velditems , gevolgd door een 4-byte offset van de volgende IFD (of 0 als er geen is). Er moet minimaal 1 IFD in een TIFF-bestand zitten en elke IFD moet minimaal één item bevatten.

##### IFD-invoer #####

Elke IFD-invoer van 12 bytes heeft de volgende indeling.


|Bytes|Beschrijving
---|---|
|0-1|De tag die het veld identificeert
|2-3|Het veldtype
|4-7|Tellen van het aangegeven type
|8-11|De waardeverschuiving, de bestandsverschuiving (in bytes) van de waarde voor het veld. De waarde begint naar verwachting op een woordgrens; de corresponderende Value Offset zal dus een even getal zijn. Deze bestandsoffset kan overal in het bestand wijzen, zelfs na de afbeeldingsgegevens

Een TIFF-veld is een logische entiteit die bestaat uit een TIFF-tag en zijn waarde. Dit logische concept wordt geïmplementeerd als een IFD-invoer, plus de werkelijke waarde als deze niet past in het waarde/offset-gedeelte, de laatste 4 bytes van de IFD-invoer. De termen TIFF-veld en IFD-invoer zijn in de meeste contexten uitwisselbaar.

#### Miniatuurafbeelding ####

Exif-formaat bevat miniatuur van afbeelding (behalve Ricoh RDC-300Z). Meestal bevindt deze zich naast de IFD1. Er zijn 3 formaten voor thumbnails; JPEG-formaat (JPEG gebruikt YCbCr), RGB TIFF-formaat, YCbCr TIFF-formaat.

##### JPEG-formaat miniatuur #####

Als de waarde van Compression (0x0103) Tag in IFD1 '6' is, is het formaat van de miniatuurafbeelding JPEG. De meeste Exif-afbeeldingen gebruiken het JPEG-formaat voor miniatuur. In dat geval kunt u een verschuiving van de thumbnail krijgen door JpegIFOffset(0x0201) Tag in IFD1, grootte van de thumbnail door JpegIFByteCount(0x0202) Tag. Het gegevensformaat is het gewone JPEG-formaat, begint bij 0xFFD8 en eindigt bij 0xFFD9. Het lijkt erop dat het JPEG-formaat en de grootte van 160x120pixels het aanbevolen miniatuurformaat zijn voor Exif2.1 of hoger.

##### TIFF-formaat miniatuur #####

Als de waarde van Compression (0x0103) Tag in IFD1 '1' is, is het formaat van de miniatuurafbeelding geen compressie (TIFF-afbeelding genoemd). Startpunt van miniatuurgegevens is StripOffset (0x0111) Tag, grootte van miniatuur is de som vanStripByteCounts (0x0117) Tag.

## Referenties ##

* [EXIF - Door Wikipedia](https://en.wikipedia.org/wiki/Exif)
* [EXIF-bestandsindeling](https://www.media.mit.edu/pia/Research/deepview/exif.html)

