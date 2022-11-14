{
  "date" : "2019-10-11",
  "keywords" :[ "png-bestand", "png-bestandsindeling", "wat is een png-bestand", "bestand", "png-voorbeeld", "png-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PNG-bestandsindeling - Rasterafbeeldingsbestand",
  "description":"Meer informatie over PNG-bestandsindeling en API's die PNG-bestanden kunnen maken en openen.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een PNG-bestand?

Een **PNG**-bestand (Portable Network Graphics) is een bestandsindeling voor rasterafbeeldingen die compressie zonder verlies gebruikt. Dit bestandsformaat is gemaakt als vervanging van Graphics Interchange Format ([GIF](/nl/image/gif/)) en heeft geen copyrightbeperkingen. Het PNG-bestandsformaat ondersteunt echter geen animaties. Het PNG-bestandsformaat ondersteunt beeldcompressie zonder verlies, waardoor het populair is onder zijn gebruikers. Met het verstrijken van de tijd is PNG geëvolueerd als een van de meest gebruikte afbeeldingsbestandsindelingen.

## Korte geschiedenis van PNG-bestandsindeling

De belangrijkste reden achter het maken van het PNG-bestandsformaat was het gepatenteerde compressiealgoritme, Lempel-Ziv-Welch, dat in het GIF-bestandsformaat wordt gebruikt. Dit samen met andere GIF-beperkingen zorgde ervoor dat het [**GIF**](/nl/image/gif/) bestandsformaat moest worden vervangen. Het eerste voorstel en de eerste naam voor PNG-bestandsindelingen kwamen in januari 1995. De belangrijkste gebeurtenissen met betrekking tot PNG-bestandsindelingen worden hieronder vermeld:

* Oktober 1996: PNG-specificaties Versie 1.0 werd uitgebracht en verscheen later als [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Hetzelfde werd een W3C-aanbeveling in oktober 1996.
* December 1998: Versie 1.1, met enkele kleine wijzigingen en de toevoeging van drie nieuwe chunks, werd uitgebracht.
* Augustus 1999: Versie 1.2, met een extra brok, werd uitgebracht.
* November 2003: PNG werd een internationale norm (ISO/IEC 15948:2003). Deze versie van PNG verschilt slechts in geringe mate van versie 1.2 en voegt geen nieuwe chunks toe.
* Maart 2004: ISO/IEC 15948:2004

## Functionele vergelijking van GIF en PNG

Het PNG-bestandsformaat is ontworpen om eenvoudig en draagbaar, juridisch onbezwaard, uitwisselbaar, flexibel en robuust te zijn. De volgende tabel bevat de GIF-functies die naast nieuwe functies worden overgenomen door de PNG-bestandsindeling.

|Feature|GIF|PNG|
---|---|---|
|Indexkleurenafbeeldingen tot 256 kleuren|Ja|Ja|
|Ondersteuning voor streaming|Ja|Ja|
|Transparantie|Ja|Ja|
|Aanvullende informatie|Ja|Ja|
|Harware en platformonafhankelijkheid|Ja|Ja|
|Effectief|Ja|Ja|
|Truecolor-afbeeldingen tot 48 bits per pixel|Nee|Ja|
|Grijswaardenafbeeldingen tot 16 bits per pixel|Nee|Ja|
|Volledig alfakanaal (algemene transparantiemaskers)|Nee|Ja|
|Afbeelding gamma-informatie|Nee|Ja|
|Betrouwbaarheid|Nee|Ja|
|Sneller eerste presentatie|Nee|Ja|

## PNG-bestandsstructuur

Bijna alle besturingssystemen hebben ondersteuning voor het openen van PNG-bestanden. Microsoft Windows-viewer heeft bijvoorbeeld de mogelijkheid om PNG-bestanden te openen, aangezien het besturingssysteem standaard de ondersteuning heeft die beschikbaar is als onderdeel van de installatie. Een PNG-bestand bestaat uit een PNG-handtekening gevolgd door een reeks //brokken//.

### PNG-bestandskop

De eerste acht bytes van een PNG-bestand bevatten altijd de volgende (decimale) waarden:

{{{137 80 78 71 13 10 26 10 }}}

Deze handtekening geeft aan dat de rest van het bestand een enkele PNG-afbeelding bevat, bestaande uit een reeks chunks die beginnen met een IHDR-chunk en eindigen met een IEND-chunk.

### Brokken ###

Elk blok bestaat uit vier delen:

**Lengte:** Een niet-ondertekend geheel getal van 4 bytes dat het aantal bytes in het gegevensveld van de chunk aangeeft. De lengte telt alleen het gegevensveld, niet zichzelf, de chunk-typecode of de CRC. Nul is een geldige lengte. Hoewel encoders en decoders de lengte als niet-ondertekend moeten beschouwen, mag de waarde niet groter zijn dan 231 bytes.

**Chunktype:** Een code van het type chunk van 4 bytes. Voor het gemak bij de beschrijving en bij het onderzoeken van PNG-bestanden, mogen typecodes beperkt zijn tot ASCII-letters in hoofdletters en kleine letters (AZ en az, of 65-90 en 97-122 decimaal). Encoders en decoders moeten de codes echter behandelen als vaste binaire waarden, niet als tekenreeksen. Het zou bijvoorbeeld niet correct zijn om de typecode IDAT weer te geven door de EBCDIC-equivalenten van die letters. Aanvullende naamgevingsconventies voor chunk-types worden besproken in de volgende sectie.

**Chunkgegevens:** De gegevensbytes die geschikt zijn voor het type chunk, indien aanwezig. Dit veld kan een lengte hebben van nul.

**CRC:** Een 4-byte CRC (Cyclic Redundancy Check) berekend op de voorgaande bytes in de chunk, inclusief de chunktypecode en chunkgegevensvelden, maar exclusief het lengteveld. De CRC is altijd aanwezig, zelfs voor chunks die geen data bevatten.

De lengte van de chunkgegevens kan een willekeurig aantal bytes zijn tot het maximum; daarom kunnen uitvoerders er niet vanuit gaan dat chunks zijn uitgelijnd op grenzen die groter zijn dan bytes.

Chunks kunnen in elke volgorde verschijnen, afhankelijk van de beperkingen die aan elk type chunk zijn gesteld. (Een opvallende beperking is dat IHDR als eerste moet verschijnen en IEND als laatste; de IEND-chunk dient dus als een einde-bestandsmarkering.) Meerdere brokken van hetzelfde type kunnen verschijnen, maar alleen als dit specifiek is toegestaan voor dat type.

#### Broktypes

De Chunk Types zijn onderverdeeld in **Critical** en **Ancillary** chunks op basis van de 4-byte hoofdlettergevoelige ASCII-waarde die aan het Chunk Type is toegewezen. Alle implementaties moeten de standaard kritische chunks begrijpen en succesvol weergeven. Een geldige PNG-afbeelding moet een IHDR-chunk, een of meer IDAT-chunks en een IEND-chunk bevatten.

### Compressie

PNG-compressiemethode 0 (de enige compressiemethode die momenteel voor PNG is gedefinieerd) specificeert deflate/inflate-compressie met een schuifvenster van maximaal 32768 bytes. Deflate-compressie is een LZ77-derivaat dat wordt gebruikt in zip-, gzip-, pkzip- en gerelateerde programma's. Er is uitgebreid onderzoek gedaan ter ondersteuning van de patentvrije status. De gecomprimeerde gegevens in de zlib-gegevensstroom worden opgeslagen als een reeks blokken, die elk onbewerkte (niet-gecomprimeerde) gegevens, LZ77-gecomprimeerde gegevens gecodeerd met vaste Huffman-codes of LZ77-gecomprimeerde gegevens gecodeerd met aangepaste Huffman-codes kunnen vertegenwoordigen. Een markeringsbit in het laatste blok identificeert het als het laatste blok, waardoor de decoder het einde van de gecomprimeerde datastroom kan herkennen.

#### Pre-compressiefiltering

Pre-compressiefilters worden toegepast om de beeldgegevens voor te bereiden op optimale compressie. De PNG-filtermethode definieert als volgt vijf basisfiltertypen:

|Filtertype|Naam|Voorspelde waarde|
---|---|---|
|0|Geen|De scanlijn wordt ongewijzigd verzonden|
|1|Sub|Verzendt het verschil tussen elke byte en de waarde van de corresponderende byte van de voorgaande pixel.|
|2|Up|Het Up()-filter is net als het Sub()-filter, behalve dat de pixel direct boven de huidige pixel, in plaats van alleen links, wordt gebruikt als de voorspeller.|
|3|Average|Het filter Average() gebruikt het gemiddelde van de twee aangrenzende pixels (links en hoger) om de waarde van een pixel te voorspellen.|
|4|Paeth|Het Paeth()-filter berekent een eenvoudige lineaire functie van de drie aangrenzende pixels (links, boven, linksboven) en kiest vervolgens als voorspeller de naburige pixel die het dichtst bij de berekende waarde ligt.|

Filteralgoritmen worden toegepast op `bytes`, niet op pixels, ongeacht de bitdiepte of het kleurtype van de afbeelding. De filteralgoritmen werken op de bytereeks gevormd door een scanlijn. Als de afbeelding een alfakanaal bevat, worden de alfagegevens op dezelfde manier gefilterd als de afbeeldingsgegevens.

Wanneer het beeld geïnterlinieerd is, wordt elke passage van het interlacepatroon behandeld als een onafhankelijk beeld voor filterdoeleinden. De filters werken op de bytereeksen die worden gevormd door de pixels die daadwerkelijk tijdens een doorgang zijn verzonden, en de "vorige scanlijn" is degene die eerder in dezelfde doorgang is verzonden, niet de aangrenzende in het volledige beeld. Merk op dat de subafbeelding die in een enkele doorgang wordt verzonden, altijd rechthoekig is, maar een kleinere breedte en/of hoogte heeft dan de volledige afbeelding. Er wordt niet gefilterd als deze subafbeelding leeg is.

## Referenties ##

* [PNG - Startpagina](http://www.libpng.org/pub/png/)

