{
  "date" : "2020-08-20",
  "keywords" :[ "cff2-bestand", "cff2-bestandsformaat", "wat is een cff2-bestand", "bestand", "cff2-voorbeeld", "cff2-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Compact Font File Format versie 2",
  "description":"Meer informatie over CFF2-bestandsindelingen en API's om CFF2-bestanden te maken en te openen.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Wat is een CFF2-bestand?

Het CFF2-bestandsformaat is de versie 2.0 van het CFF-bestandsformaat en maakt een efficiënte opslag van glyph-contouren en metadata mogelijk, vergelijkbaar met het CFF-bestandsformaat. CFF2 verschilt van CFF doordat het bedoeld is om te worden gebruikt in de context van een OpenType-lettertype als een 'sfnt'-tabel met de tag CFF2. Het kan niet worden gebruikt als een op zichzelf staand programma en is afhankelijk van gegevens in andere OpenType-tabellen.

## CFF2-bestandsindeling

De [CFF2-specificaties voor bestandsindelingen](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2) bevat details over de interne gegevenslay-out, gegevenstypen, tabellen en andere interne informatie over de bestandsindeling. Het kan worden doorverwezen ter referentie van de ontwikkelaar. Enkele details hierover zijn als volgt.

### Gegevenslay-out

De binaire gegevens van het CFF2-bestandsformaat zijn logisch georganiseerd als een aantal afzonderlijke gegevensstructuren. De lay-out binnen de binaire gegevens is zoals weergegeven in de volgende tabel.

|Invoer |Opmerkingen|
---|---|
|Koptekst |Vaste locatie|
|Top DICT| Vaste locatie|
|Global Subr INDEX| Vaste locatie|
|Variatie |Opslaan|
|FDSelect |Alleen presenteren als er meer dan één Font DICT in de Font DICT INDEX is.|
|Lettertype DICT INDEX ||
|Array van lettertype DICT| Opgenomen in lettertype DICT INDEX.|
|Privé DICT| Eén per lettertype DICT.|

Alleen de eerste drie structuren zijn gebaseerd op vaste locaties. De overige worden bereikt via offsets en hun volgorde kan worden gewijzigd.

### Gegevenstypen

Het CFF2-bestandsformaat gebruikt de volgende gegevenstypen.

|Naam |Bereik |Beschrijving|
---|---|---|
|uint8 |0 tot 255 |8-bits niet-ondertekend nummer|
|uint16 |0 tot 65535| 16-bits niet-ondertekend nummer|
|uint32 |0 tot 4294967295| 32-bits niet-ondertekend nummer|
|Offset |varieert| 1, 2, 3 of 4 byte offsets (gespecificeerd door OffSize veld in een Index tabel)|
|UitGrootte |1 tot 4| 1-byte unsigned nummer specificeert de grootte van een Offset veld of velden|

Het slaat alle multi-byte numerieke gegevens en offsetvelden op in big-endian bytevolgorde. Het CFF2-formaat is vrij van opvulbytes omdat het geen uitlijningsbeperkingen respecteert.

### DICT-gegevens

CFF2-bestanden bevatten de font-woordenboekgegevens als sleutel-waardeparen in een compacte tokenized-indeling. Woordenboeksleutels worden gecodeerd als operatoren van 1 of 2 bytes en woordenboekwaarden worden gecodeerd als numerieke operanden van variabele grootte. Er zijn drie structuren die het DICT-gegevensformaat gebruiken: `Top DICT`, `Font DICT` en `Private DICT`. Er is een aantal integere operandtypen van verschillende grootte gedefinieerd en gecodeerd zoals weergegeven in de volgende tabel (eerste byte van operand is b0, tweede is b1, enzovoort).

|Grootte |b0 bereik |Waardebereik |Waardeberekening|
---|---|---|---|
|1 |32 tot 246| -107 tot +107 |b0 - 139|
|2 |247 tot 250| +108 tot +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 tot 254| -1131 tot -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 tot +32767| b1 << 8 | b2|
|5 |29| -(2^31) tot +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Koptekst

De binaire gegevens beginnen met een kop met het formaat dat wordt weergegeven in de onderstaande tabel.

|Type |Naam |Beschrijving|
---|---|---|
|uint8| majorVersion| Grote versie formatteren. Instellen op 2.|
|uint8| minorVersie| Kleinere versie opmaken. Zet op nul.|
|uint8| kopgrootte| Headergrootte (bytes).|
|uint16| topDictLengte| Lengte van Top DICT-structuur in bytes.|

## Referenties

* [CFF2-bestandsindeling](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2)

