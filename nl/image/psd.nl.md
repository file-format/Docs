{
  "date" : "2019-10-11",
  "keywords" :[ "psd-bestand", "psd-bestandsindeling", "wat is een psd-bestand", "bestand", "psd-voorbeeld", "psd-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Photoshop-beeldbestandsindeling",
  "description":"Meer informatie over PSD-bestandsindeling en API's die PSD-bestanden kunnen maken en openen.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een PSD-bestand?

PSD, Photoshop Document, vertegenwoordigt het oorspronkelijke bestandsformaat van Adobe Photoshop dat wordt gebruikt voor het ontwerpen en ontwikkelen van afbeeldingen. PSD-bestanden kunnen afbeeldingslagen, aanpassingslagen, laagmaskers, annotaties, bestandsinformatie, trefwoorden en andere Photoshop-specifieke elementen bevatten. Photoshop-bestanden hebben de standaardextensie .PSD en hebben een maximale hoogte en breedte van 30.000 pixels en een lengtelimiet van twee gigabyte.

## Specificaties PSD-bestandsindeling ##

Gegevens in een PSD-bestand worden opgeslagen in big endian-bytevolgorde. Dit houdt in dat de korte en lange gehele getallen worden verwisseld bij het lezen of schrijven op het Windows-platform. Het Photoshop-bestandsformaat is verdeeld in vijf grote delen. Het heeft veel lengtemarkeringen die kunnen worden gebruikt om van de ene sectie naar de volgende te gaan. De lengtemarkeringen zijn meestal opgevuld met bytes om af te ronden op het dichtstbijzijnde interval van 2 of 4 bytes. De vijf belangrijkste onderdelen zijn:

* Bestandskoptekst
* Kleurmodusgegevens
* Afbeeldingsbronnen
* Laag- en maskerinformatie
* Afbeeldingsgegevens

Voor conformiteit moeten gegevens naar al deze velden in de sectie worden geschreven, aangezien Photoshop kan proberen de hele sectie te lezen. Het houdt ook in dat er nullen naar overgeslagen velden worden geschreven tijdens het schrijven naar een bestand. Het lengteveld in de lengte-gescheiden secties moet worden gebruikt om te beslissen wanneer u moet stoppen met lezen. In de meeste gevallen geeft het lengteveld het volgende aantal bytes aan, niet de records. De volgende punten moeten worden onthouden tijdens het lezen van een bestand.

* De waarden in de kolom "Lengte" in alle tabellen zijn in bytes.
* Alle waarden gedefinieerd als Unicode-tekenreeks bestaan uit:
* Een veld met een lengte van 4 bytes, dat het aantal tekens in de tekenreeks vertegenwoordigt (geen bytes).
* De reeks Unicode-waarden, twee bytes per teken.

### Bestandskop ###

De bestandskop bevat de basiseigenschappen van de afbeelding.

|Lengte|Beschrijving
---|---|
|4|Handtekening: altijd gelijk aan '8BPS' . Probeer het bestand niet te lezen als de handtekening niet overeenkomt met deze waarde.
|2|Versie: altijd gelijk aan 1. Probeer het bestand niet te lezen als de versie niet overeenkomt met deze waarde. (~*~*PSB~*~* versie is 2.)
|6|Gereserveerd: moet nul zijn.
|2|Het aantal kanalen in de afbeelding, inclusief alfakanalen. Het ondersteunde bereik is 1 tot 56.
|4|De hoogte van de afbeelding in pixels. Het ondersteunde bereik is 1 tot 30.000.
|4|De breedte van de afbeelding in pixels. Het ondersteunde bereik is 1 tot 30.000.
|2|Diepte: het aantal bits per kanaal. Ondersteunde waarden zijn 1, 8, 16 en 32.
|2|De kleurmodus van het bestand. Ondersteunde waarden zijn: Bitmap # 0; Grijsschaal # 1; Geïndexeerd # 2; RGB # 3; CMYK # 4; Meerkanaals # 7; Duotoon # 8; Laboratorium # 9.

### Kleurmodus Gegevenssectie ###

De gegevenssectie van de kleurmodus is als volgt gestructureerd:


|Lengte|Beschrijving
---|---|
|4|De lengte van de volgende kleurgegevens
|variabele|De kleurgegevens

Kleurmodusgegevens zijn alleen beschikbaar voor geïndexeerde kleuren en duotoon zoals gedefinieerd door het modusveld in de sectie Bestandskoptekst. Voor alle andere modi wordt deze sectie weergegeven door 4-byte nulwaarden. Voor geïndexeerde kleurenafbeeldingen is de lengte 768 en bevatten de kleurgegevens de kleurentabel voor de afbeelding, in niet-interleaved volgorde. Voor Duotone-afbeeldingen bevatten kleurgegevens de duotoonspecificatie (waarvan het formaat niet is gedocumenteerd). Andere toepassingen die Photoshop-bestanden lezen, kunnen een duotoonafbeelding als een grijze afbeelding behandelen en de inhoud van de duotooninformatie behouden bij het lezen en schrijven van het bestand.

### Beeldbronnen Sectie ###

Het derde deel van het bestand bevat afbeeldingsbronnen. Het begint met een lengteveld, gevolgd door een reeks resourceblokken.


|Lengte|Beschrijving
---|---|
|4|Lengte van het gedeelte met afbeeldingsbronnen. De lengte kan nul zijn.
|Variabele|Beeldbronnen (blokken met afbeeldingsbronnen)

Afbeeldingsbronnen worden gebruikt om niet-pixelgegevens op te slaan die zijn gekoppeld aan afbeeldingen, zoals pengereedschappen. Ze worden resourceblokken genoemd omdat ze gegevens bevatten die in vroege versies van Photoshop in de Macintosh-bron waren opgeslagen. De basisstructuur van afbeeldingsresourceblokken is als volgt:


|Lengte|Beschrijving
---|---|
|4|Handtekening: '8BIM'
|2|Unieke id voor de bron. Afbeeldingsresource-ID's bevatten een lijst met resource-ID's die door Photoshop worden gebruikt.
|Variabele|Naam: Pascal-tekenreeks, opgevuld om de grootte gelijk te maken (een null-naam bestaat uit twee bytes van 0)
|4|Werkelijke grootte van brongegevens die volgt
|Variabele|De resourcegegevens, beschreven in de secties over de afzonderlijke resourcetypen. Het is gewatteerd om de maat gelijk te maken.

Beeldbronnen gebruiken verschillende standaard ID-nummers.

### Informatie over lagen en maskers ###

Het vierde gedeelte van een Photoshop-bestand bevat informatie over lagen en maskers, zoals het aantal lagen, kanalen in de lagen, overvloeibereiken, aanpassingslaagtoetsen, effectlagen en maskerparameters. Als er geen lagen of maskers zijn, wordt deze sectie weergegeven door een op nul gezet 4-byte-veld. Speciale aandacht moet worden besteed aan de lengte van secties tijdens het lezen van deze sectie vanwege de nulwaarden. De indeling van de sectie Laag en Masker is als volgt:


|Lengte|Beschrijving
---|---|
|4|Lengte van de laag- en maskerinformatiesectie. (PSB-lengte is 8 bytes.)
|Variabele|Informatie over lagen
|Variabele|Globale informatie over laagmasker
|Variabele|Serie van getagde blokken die verschillende soorten gegevens bevatten.

#### Laaginfo ####

De volgende tabel toont de organisatie op hoog niveau van de laaginformatie.


|Lengte|Beschrijving
---|---|
|4|Lengte van de sectie met informatie over lagen, naar boven afgerond op een veelvoud van 2. (PSB-lengte is 8 bytes.)
|2|Lagen tellen. Als het een negatief getal is, is de absolute waarde het aantal lagen en bevat het eerste alfakanaal de transparantiegegevens voor het samengevoegde resultaat.
|Variabele|Informatie over elke laag. Zie Laagrecords beschrijft de structuur van deze informatie voor elke laag.
|Variabele|Kanaal afbeeldingsgegevens. Bevat een of meer beeldgegevensrecords voor elke laag. De lagen staan in dezelfde volgorde als in de laaginformatie

### Afbeeldingsgegevens ###

De afbeeldingspixelgegevens bevinden zich in het gedeelte Afbeeldingsgegevens van het bestand. Rangschikking van gegevens in het gedeelte Afbeeldingsgegevens is in vlakke volgorde, dwz eerst alle rode gegevens, dan alle groene gegevens, enz. Elk vlak wordt opgeslagen in scanlijnvolgorde, zonder padbytes. Het gedeelte met beeldgegevens is gerangschikt in een formaat zoals weergegeven in de volgende tabel.

|Lengte|Beschrijving
---|---|
|2|Compressiemethode: *0 = onbewerkte afbeeldingsgegevens * 1 = RLE gecomprimeerde afbeeldingsgegevens beginnen met het aantal bytes voor alle scanlijnen (rijen * kanalen), waarbij elke telling wordt opgeslagen als een waarde van twee bytes. De RLE-gecomprimeerde gegevens volgen, waarbij elke scanlijn afzonderlijk wordt gecomprimeerd. De RLE-compressie is hetzelfde compressie-algoritme dat wordt gebruikt door de Macintosh ROM-routine PackBits en de TIFF-standaard. *2 = ZIP zonder voorspelling *3 = ZIP met voorspelling.
|Variabele|De afbeeldingsgegevens. Planaire volgorde = RRR GGG BBB, enz.

## Referenties ##

* [PSD-bestandsindelingspecificaties - door Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Adobe Photoshop-bestandsindeling](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

