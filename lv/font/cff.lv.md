{
  "date": "2020-08-20",
  "keywords": [
"cff failu",
"cff faila formātā",
"kas ir cff fails",
"failu",
"cff piemērs",
"cff faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF - kompakts fonta faila formāts",
  "description": "Uzziniet par CFF faila formātu un API, lai izveidotu un atvērtu CFF failus.",
  "linktitle": "CFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cf-lvf"
}
},
  "lastmod": "2020-10-21"
}

## Kas ir CFF fails?

Fails ar paplašinājumu .cff ir kompaktais fonta formāts, un to sauc arī par PostScript Type 1 jeb CIDFont. CFF darbojas kā konteiners vairāku fontu glabāšanai vienā vienībā, kas pazīstama kā FontSet. CFF fontu dizains ļauj iegult PostScript valodas kodu, kas nodrošina papildu elastību un formāta paplašināšanu lietošanai ar printeru vidēm. CFF fontu failus var atvērt un konvertēt, izmantojot API, piemēram, [Aspose.Font](https://products.aspose.com/font).

## CFF faila formāts

CFF faili ir bināri faili, kas satur strukturētu datu izkārtojumu, kuriem ir noteikti datu tipi, galvene, glifu organizācija un tabulu vārdnīcas. Plašāku informāciju par tiem var atrast [compact font format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff).

### Datu izkārtojums
CFF faila formāta datu izkārtojums ir šāds.

|Ieraksts|Komentāri|
---|---|
|Galvene|–|
|VārdsINDEX|–|
|Augšākais DICT INDEKSS|–|
|String INDEX|–|
|Global Subr INDEX|–|
|Kodējumi–Rakstzīmes|–|
|FDSelect|CIDFonts tikai|
|CharStrings INDEX|par fontu|
|Fontu DICT INDEX|par fontu, tikai CIDFonti|
|Privāts DICT|par fontu|
|Local Subr INDEX|par fontu vai privāto DICT CIDFontiem|
|Paziņojumi par autortiesībām un preču zīmēm|–|

### Datu veidi

CFF datu tipi ir parādīti nākamajā tabulā.

|Nosaukums|Diapazons|Apraksts|
---|---|---|
|Card8|0 –255|1 baita neparakstīts numurs|
|Kartīte16|0 – 65535|2 baitu neparakstīts numurs|
|Nobīde|svārstās|1, 2, 3 vai 4 baitu nobīde (norāda laukā OffSize)|
|OffSize|1–4|1 baita neparakstīts skaitlis norāda Nobīdes lauka vai lauku lielumu|
|SID|0 – 64999|2 baitu virknes identifikators|

### Virsraksts

Binārie dati sākas ar galveni, kura formāts ir parādīts nākamajā tabulā.

|Tips|Nosaukums|Apraksts|
---|---|---|
|Card8|major|Formatējiet galveno versiju (sākot ar 1)|
|Card8|minor|Formatējiet mazo versiju (sākot ar 0)|
|Kartīte8|hdrIzmērs| Galvenes lielums (baitos)|
|OffSize|offSize|Absolūtā nobīde (0) izmērs|

## Atsauces

 * [Compact Font Format Table](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
 * [CFF faila formāts](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
 * [CFF2 diagrammu kopa](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

