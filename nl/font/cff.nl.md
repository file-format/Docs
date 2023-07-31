{
  "date" : "2020-08-20",
  "keywords" :[ "cff-bestand", "cff-bestandsformaat", "wat is een cff-bestand", "bestand", "cff-voorbeeld", "cff-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Compact lettertypebestandsformaat",
  "description":"Meer informatie over CFF-bestandsindeling en API's om CFF-bestanden te maken en te openen.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Wat is een CFF-bestand?

Een bestand met de extensie .cff is een Compact Font Format en wordt ook wel PostScript Type 1 of CIDfont genoemd. CFF fungeert als een container om meerdere lettertypen samen op te slaan in een enkele eenheid die bekend staat als een FontSet. Het ontwerp van CFF-lettertypen maakt het mogelijk om PostScript-taalcode in te sluiten die extra flexibiliteit en uitbreidbaarheid van het formaat mogelijk maakt voor gebruik met printeromgevingen. CFF-lettertypebestanden kunnen worden geopend en geconverteerd met behulp van API's zoals [Aspose.Font](https://products.aspose.com/font).

## CFF-bestandsindeling

CFF-bestanden zijn binaire bestanden met een gestructureerde gegevenslay-out, gedefinieerde gegevenstypen, een koptekst, glyph-organisatie en tabelwoordenboeken. Meer details hierover zijn te vinden in de [specificaties voor compacte lettertypeformaten](https://learn.microsoft.com/en-us/typography/opentype/spec/cff).

### Gegevenslay-out
De gegevenslay-out van het CFF-bestandsformaat is zoals hieronder weergegeven.

|Invoer|Opmerkingen|
---|---|
|Koptekst|–|
|NaamINDEX|–|
|Top DICT-INDEX|–|
|String INDEX|–|
|Global Subr INDEX|–|
|Codes–Tekensets|–|
|FDSelect|CIDfonts only|
|CharStrings INDEX|per-lettertype|
|Lettertype DICT INDEX|per-lettertype, alleen CIDFonts|
|Privé DICT|per-lettertype|
|Lokale Subr INDEX|per-lettertype of per-privé DICT voor CIDfonts|
|Copyright- en handelsmerkkennisgevingen|–|

### Gegevenstypen

CFF-gegevenstypen zijn zoals weergegeven in de volgende tabel.

|Naam|Bereik|Beschrijving|
---|---|---|
|Card8|0 –255|1-byte niet-ondertekend nummer|
|Card16|0 – 65535|2-byte niet-ondertekend nummer|
|Offset|varieert|1, 2, 3 of 4 byte offset (gespecificeerd door OffSize veld)|
|OffSize|1–4|1-byte niet-ondertekend getal specificeert de grootte van een Offset-veld of velden|
|SID|0 – 64999|2-byte tekenreeks-ID|

### Koptekst

De binaire gegevens beginnen met een kop met het formaat dat in de volgende tabel wordt weergegeven.

|Type|Naam|Beschrijving|
---|---|---|
|Card8|majeur|Formaat hoofdversie (vanaf 1)|
|Card8|minor|Formaat secundaire versie (vanaf 0)|
|Kaart8|hdrSize| Headergrootte (bytes)|
|OffSize|offSize|Absolute offset (0) maat|

## Referenties

* [Compacte lettertype-indelingstabel](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
* [CFF-bestandsindeling](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2-kaartenset](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

