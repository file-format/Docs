{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Bestandsindeling", "Openen", "Lezen", "Maken", "CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over DWF-bestandsindelingen en API's die DWF-bestanden kunnen maken en openen.",
  "title" :"DWF-bestandsindeling",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een DWF-bestand?

Design Web Format (DWF) vertegenwoordigt 2D/3D-tekeningen in gecomprimeerd formaat voor het bekijken, bekijken of afdrukken van ontwerpbestanden. Het bevat afbeeldingen en tekst als onderdeel van ontwerpgegevens en verkleint de grootte van het bestand vanwege het gecomprimeerde formaat. De beperkte bestandsgrootte maakt de distributie en communicatie van rijke ontwerpgegevens efficiënt. DWF vereist niet dat de ontvanger op de hoogte is van het gebruik van CAD-software waarmee de originele tekening is gemaakt. De inhoud van het DWF-bestandsformaat kan eenvoudig zijn en slechts een enkel blad bevatten of complex genoeg om lettertypen, kleuren en afbeeldingen te hebben.

## Korte geschiedenis ##

Autodesk introduceerde het DWF-bestandsformaat in 1995 als onderdeel van de Netscape Navigation plug-in, WHIP. Het formaat is in de loop van de tijd geëvolueerd van het alleen 2D-formaat naar 3D-inhoud. Veel toepassingen van derden maken ook gebruik van dit formaat.

## DWF-bestandsindeling ##

DWF is een open, veilige indeling die speciaal is ontworpen voor het delen van rijke technische ontwerpgegevens. Het is onafhankelijk van de originele applicatiesoftware, hardware en besturingssysteem die zijn gebruikt om die ontwerpgegevens te creëren. Hierdoor kunnen teamleden die geen CAD-applicaties gebruiken, deelnemen aan de digitale processen door gebouw-, GIS- of productontwerpen te bekijken. Een DWF-bestandsarchief bestaat uit verschillende XML- en binaire bestanden die samen zijn verpakt in een gecomprimeerd archief dat is gemaakt met [ZIP](/nl/compression/zip/)-compressie. U kunt een DWF-bestandsextensie hernoemen naar ZIP en de inhoud van het bestand bekijken. Het DWF-pakket kan vele soorten ontwerpgegevens bevatten, zoals 2D-afbeeldingen, 3D-afbeeldingen, pakket- en sectiemetagegevens en andere bronbestanden.

**DWF-metadatabestanden** – XML-bestanden die informatie bevatten met betrekking tot metadata en structuur (auteur, titel, aanmaaktijd, sectie-afhankelijkheden, sectievolgorde, beschrijvingen van bronbestanden, rollen, mimetypes, enz.) en die betrekking hebben op de sectie (pagina informatie, ontwerpmetadata, enz.). De structurele metadata wordt gebruikt om logische objecten te creëren (verzamelingen van bestanden die een onderdeel of pagina vertegenwoordigen, enz.).

**Bronbestanden** – media- of andere inhoudsbestanden waarnaar wordt verwezen vanuit de metadata van het pakket/de sectie en zijn meestal presentaties van ontwerpgegevens in verschillende formaten (ZGL, W2D, [JPG](/nl/image/jpeg/), [PNG](/nl/image/png/), AVI, XML, [TXT](/nl/tekstverwerking/txt/), [DOC](/nl/tekstverwerking/doc/), enz.)

### Details bestandsformaat ###

DWF-bestanden zijn georganiseerd in drie hoofdsecties, zoals hieronder weergegeven.

* Koptekst voor bestandsidentificatie
* Bestandsgegevensblok
* Aanhangwagen voor bestandsbeëindiging

#### Bestandsidentificatiekoptekst ####

De header van de bestandsidentificatie maakt identificatie van DWF-bestanden door toepassingen mogelijk. Het geeft ook aan welke versie van de DWF-specificaties is gebruikt voor het coderen van het bestand. Het is een header van 12 bytes die als volgt is gerangschikt:


|Byte|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Teken|(|D|W|F|(spatie)|V|0|0|.|3|0|)

Hier is een samenvatting van deze tabel:

* De eerste zes bytes van de header vertegenwoordigen altijd ASCII-tekens "(DWF V"
* De volgende 5 bytes bevatten informatie over het versienummer, bijv. "00.30" met de hoofd- en secundaire versiewaarde van het formaat

Toepassingen die een DWF-bestand maken, moeten het laagst mogelijke versienummer specificeren dat een leestoepassing moet ondersteunen om de gegevens correct te gebruiken.

#### Bestandsgegevensblok ####

Het bestandsgegevensblok begint bij de 13e byte van een DWF-bestand en is een reeks opcode- en operandparen, zoals in de volgende tabel.

|Veld 1|Veld 2|Veld 3|Veld 4|Veld 5|Veld 5
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operand

Een DWF-bestand kan opcode-operandparen bevatten als leesbare ASCII en als binaire code of een combinatie van beide. Alle DWF-bewerkingen hebben een leesbare ASCII-opcode/operand-vorm en de meeste bewerkingen hebben ook een gecodeerde binaire opcode/operand-vorm. Opcodes zijn in één byte, waardoor meer dan 200 bewerkingen mogelijk zijn. Extended ASCII en extended binary zijn uitzonderlijke gevallen. De waarden van Opcodes kunnen variëren van 0-255 met enkele uitzonderingen. Behalve de twee speciale typen opcodes, uitgebreid ASCII en uitgebreid binair, moet een bestandslezer weten hoe de operandlengte moet worden berekend.

##### Verboden opcodes #####

De ASCII-representaties voor het volgende kunnen niet als opcodes worden gebruikt:

De volgende ASCII-representaties kunnen niet als opcodes worden gebruikt:

* Ruimte (0x20)
* Tabblad (0x09)
* Koppelteken (0x2D)
* ASCII-cijfers 0-9 (0x30 - 0x39)
* Koetsretour (0x0D)
* Lijnvoeding (0x0A)
* Enkel aanhalingsteken (0x27)
* Dubbel aanhalingsteken (0x22)
* Periode (0x2E)
* Haakjes (0x28 en 0x29)
* accolades (0x7B en 0x7D)
* Vierkante haken (0x5B en 0x5D)
* Achterwaartse slash (0x5C)

#### Aanhangwagen voor bestandsbeëindiging ####

De trailer voor het beëindigen van bestanden voor DWF is gewoon een speciale opcode die het einde van het bestand aangeeft. Sommige toepassingen kunnen niet-DWF-gegevens opslaan na de beëindiging-opcode. De trailer is zoals hieronder weergegeven:


|Byte|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Teken|(|E|n|d|0|f|D|W|F|)

## Referenties ##

* [DWF - Door Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [WHIP-gegevensindeling](http://paulbourke.net/dataformats/whip/)
* [http://blogs.msdn.com/opc/archive/2009/05/18/adventures-in-packaging-episode-1.aspx](http://blogs.msdn.com/opc/archive/2009 /05/18/avonturen-in-verpakking-episode-1.aspx)

