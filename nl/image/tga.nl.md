{
  "date" : "2019-10-11",
  "keywords" :[ "tga-bestand", "tga-bestandsformaat", "wat is een tga-bestand", "bestand", "tga-voorbeeld", "tga-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGA-bestandsindeling - een TARGA grafisch afbeeldingsbestand",
  "description":"Meer informatie over TGA-bestandsindelingen en API's die TGA-bestanden kunnen maken en openen.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een TGA-bestand?

Een bestand met de extensie .tga is een grafische rasterindeling en is gemaakt door Truevision Inc. Het is ontworpen voor de TARGA-kaarten (Truevision Advanced Raster Adapter) en biedt ondersteuning voor Highcolor/truecolor-weergave voor IBM-compatibele pc's. Het ondersteunt 8, 16, 24 en 32 bits per pixel en 8-bit alfakanaal. Het ondersteunt ook lossless RLE-compressie die kan worden toegepast om de afbeeldingsgrootte te verkleinen. Digitale foto's en texturen gebruiken het TGA-beeldformaat.

## Korte geschiedenis

De vorming van het TGA-bestandsformaat ontstond in 1984 door AT&T EPICenter (later geëxtraheerd en gevormd als een onafhankelijke entiteit die bekend staat als Truevision) dat werkte aan de marketing van nieuwe technologieën die door AT&T waren ontwikkeld voor kleurframebuffers. EPICenter werkte al aan zijn eerste twee kaarten, de VDA (Video Display Adapter) en ICB (image capture board) waarvoor al aan twee bestandstypen, .vda en .icb, werd gewerkt. Deze bestandsformaten werden gecodificeerd en het minder brede specifieke bestandsformaat TGA werd geïntroduceerd. TGA was een uitbreiding op wat al in gebruik was en leverde informatie zoals breedte, hoogte, pixeldiepte, bijbehorende kleurenkaart en beeldoorsprong.

TGA's 2.0-versie, gepubliceerd in 1989, bevatte verschillende verbeterde functies, zoals:

* Miniaturen
* Alfakanaal
* Gammawaarde
* Tekstuele metadata

De belangrijkste bijdragers aan TGA's 2.0-versie zijn Shawn Steiner, Kevin Fiedly en David Spoelstra van Truevision.

## Specificaties TGA TARGA-bestandsindeling

Een TGA-bestand bestaat uit 2 hoofdonderdelen:

* Koptekst
* Kleur Pixel-informatie

Alle waarden in een TGA-bestand zijn in littl-endian volgens de formaatspecificaties.

### TGA-koptekst

Een TGA-bestandsheader bestaat uit de volgende 5 velden.

|Veldnr.|Lengte |Veldnaam |Beschrijving|
---|---|---|---|
|1| 1 byte |ID lengte| Lengte van het afbeeldings-ID-veld (0-255)|
|2| 1 byte |Kleurkaarttype| Of er een kleurenkaart is opgenomen (0 - geeft aan dat er geen kleurenkaartgegevens bij deze afbeelding zijn inbegrepen. 1 - geeft aan dat er een kleurenkaart bij deze afbeelding is inbegrepen.)|
|3| 1 byte |Beeldtype| Compressie- en kleurtypes (0- Geen beeldgegevens inbegrepen. 1- Niet-gecomprimeerd, in kleur in kaart gebracht beeld, 2- Niet-gecomprimeerd, True Color-beeld, 9- Run-length gecodeerd, in kleur in kaart gebracht beeld, 11- Run-Length-gecodeerd, Zwart-wit beeld )|
|4| 5 bytes |Kleurkaartspecificatie| Beschrijft de kleurenkaart|
|5| 10 bytes |Beeldspecificatie| Afmetingen en formaat afbeelding|

### Afbeeldings- en kleurenkaartgegevens

|Veldnr. |Lengte |Veld |Beschrijving|
---|---|---|---|
|6 |Van afbeelding ID lengte veld| Afbeeldings-ID| Optioneel veld met identificatiegegevens|
|7 |Van kleurkaartspecificatieveld| Kleurenkaartgegevens| Opzoektabel met kleurkaartgegevens|
|8 |Van afbeeldingsspecificatieveld| Afbeeldingsgegevens| Opgeslagen volgens de afbeeldingsbeschrijving|

### Ontwikkelaarsgebied (optioneel)

TGA Versie 2.0 biedt ondersteuning voor aanvullende verbeteringen/extra's waarvan veel ontwikkelaars meer informatie wilden opslaan. De informatie is optioneel, zodat als een TGA-decoder deze niet kan interpreteren, deze wordt genegeerd.

### Uitbreidingsgebied (optioneel)

|Veldnr.| Lengte| Veld |Beschrijving|
---|---|---|---|
|10| 2 bytes |Extensiegrootte |Grootte in bytes van het extensiegebied, altijd 495|
|11| 41 bytes| Naam auteur |Naam van de auteur. Indien niet gebruikt, moeten bytes worden ingesteld op NULL (\0) of spaties|
|12| 324 bytes| Auteur commentaar| Een opmerking, georganiseerd als vier regels, elk bestaande uit 80 tekens plus een NULL|
|13| 12 bytes| Datum-/tijdstempel |Datum en tijd waarop de afbeelding is gemaakt|
|14| 41 bytes| Taak-ID||
|15| 6 bytes| Werktijd| Uren, minuten en seconden besteed aan het maken van het bestand (voor facturering, enz.)|
|16| 41 bytes| Software-ID |De toepassing die het bestand heeft gemaakt.|
|17| 3 bytes| Softwareversie||
|18| 4 bytes| Sleutelkleur||
|19| 4 bytes| Pixel-beeldverhouding||
|20| 4 bytes| Gammawaarde||
|21| 4 bytes| Kleurcorrectie offset |Aantal bytes vanaf het begin van het bestand tot de kleurcorrectietabel indien aanwezig|
|22| 4 bytes| Postzegel | Aantal bytes vanaf het begin van het bestand tot de afbeelding van de postzegel, indien aanwezig|
|23| 4 bytes| Scanlijnoffset| Aantal bytes vanaf het begin van het bestand tot de scanlijnentabel, indien aanwezig|
|24| 1 byte| Type attributen| Specificeert het alfakanaal|

### Bestandsvoettekst (optioneel)

De laatste 26 bytes van het bestand vertegenwoordigen de voettekst, wat, indien aanwezig, betekent dat het waarschijnlijk een TGA versie 2-bestand is.

|Veldnr.| Lengte| Veld| Beschrijving|
---|---|---|---|
|28| 4 bytes| Uitbreiding offset| Offset in bytes vanaf het begin van het bestand|
|29| 4 bytes| Offset ontwikkelaarsgebied| Offset in bytes vanaf het begin van het bestand|
|30| 16 bytes| Handtekening| Bevat "TRUEVISION-XFILE"|
|31| 1 byte| | Bevat "."|
|32| 1 byte| | Bevat NULL|


## Referenties

* [TGA 2.0 bestandsformaatspecificaties](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA door Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

