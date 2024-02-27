{
  "date": "2020-08-20",
  "keywords": [
"cff fil",
"cff filformat",
"hvad er en cff-fil",
"fil",
"cff eksempel",
"cff filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF - Kompakt skrifttypefilformat",
  "description": "Lær om CFF-filformat og API'er til at oprette og åbne CFF-filer.",
  "linktitle": "CFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cf-daf"
}
},
  "lastmod": "2020-10-21"
}

## Hvad er en CFF fil?

En fil med filtypenavnet .cff er et kompakt skrifttypeformat og er også kendt som en PostScript Type 1 eller CIDFont. CFF fungerer som en beholder til at gemme flere skrifttyper sammen i en enkelt enhed kendt som et FontSet. Designet af CFF-skrifttyper tillader indlejring af PostScript-sprogkode, der tillader yderligere fleksibilitet og udvidelsesmuligheder af formatet til brug med printermiljøer. CFF-skrifttypefiler kan åbnes og konverteres ved hjælp af API'er såsom [Aspose.Font](https://products.aspose.com/font).

## CFF filformat

CFF-filer er binære filer, der indeholder et struktureret datalayout, har definerede datatyper, en header, glyph-organisation og tabelordbøger. Flere detaljer om disse kan findes i [compact font format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff).

### Datalayout
Datalayoutet for CFF-filformatet er som vist nedenfor.

|Indgang|Kommentarer|
---|---|
|Overskrift|–|
|NavnINDEX|–|
|Top DICT INDEX|–|
|String INDEX|–|
|Global Subr INDEX|–|
|Kodninger–tegnsæt|–|
|FDSelect|Kun CIDfonts|
|CharStrings INDEX|per-font|
|Skrifttype DICT INDEX|pr. skrifttype, kun CIDFonter|
|Privat DICT|pr. skrifttype|
|Local Subr INDEX|per-font eller per-private DICT for CIDFonts|
|Ophavsret og varemærkemeddelelser|–|

### Datatyper

CFF-datatyper er som vist i følgende tabel.

|Navn|Område|Beskrivelse|
---|---|---|
|Kort8|0 –255|1-byte usigneret nummer|
|Kort16|0 – 65535|2-byte usigneret nummer|
|Offset|varierer|1, 2, 3 eller 4 byte offset (specificeret af OffSize-feltet)|
|OffSize|1–4|1-byte usigneret tal angiver størrelsen af et eller flere forskydningsfelter|
|SID|0 – 64999|2-byte strengidentifikator|

### Header

De binære data begynder med en header med formatet vist i følgende tabel.

|Type|Navn|Beskrivelse|
---|---|---|
|Card8|major|Formater større version (startende ved 1)|
|Card8|minor|Formater mindre version (startende ved 0)|
|Kort8|hdrStørrelse| Overskriftsstørrelse (bytes)|
|OffSize|offSize|Absolut offset (0) størrelse|

## Referencer

 * [Kompakt skrifttypeformattabel](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
 * [CFF-filformat](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
 * [CFF2 Chartset](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

