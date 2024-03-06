{
  "date": "2020-08-20",
  "keywords": [
"cff2 failu",
"cff2 faila formātā",
"kas ir cff2 fails",
"failu",
"cff2 piemērs",
"cff2 faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF2 — kompaktā fonta faila formāta versija 2",
  "description": "Uzziniet par CFF2 faila formātu un API, lai izveidotu un atvērtu CFF2 failus.",
  "linktitle": "CFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cff-lv2"
}
},
  "lastmod": "2020-10-21"
}

## Kas ir CFF2 fails?

CFF2 file format is the version 2.0 of the CFF file format and allows efficient storage of glyph outlines and metadata similar to the CFF file format. CFF2 differs from CFF in that it is intended to be used in the context of an OpenType font as a 'sfnt' table with the tag CFF2. To nevar izmantot kā atsevišķu programmu, un tā ir atkarīga no datiem citās OpenType tabulās.

## CFF2 faila formāts

[CFF2 file format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) satur informāciju par iekšējo datu izkārtojumu, datu veidiem, tabulām un citu iekšējo informāciju par faila formātu. To var izmantot izstrādātāja uzziņai. Tālāk ir sniegta informācija par tiem.

### Datu izkārtojums

CFF2 faila formāta binārie dati ir loģiski sakārtoti kā vairākas atsevišķas datu struktūras. Bināro datu izkārtojums ir tāds, kā parādīts nākamajā tabulā.

|Ieraksts |Komentāri|
---|---|
|Galvene |Fiksēta vieta|
|Top DICT| Fiksēta vieta|
|Global Subr INDEX| Fiksēta vieta|
|Variācija |Veikals|
|FDSelect |Parādīt tikai tad, ja fontu DICT INDEX ir vairāk nekā viens fonts DICT.|
|Fontu DICT INDEX ||
|Fontu masīvs DICT| Iekļauts fontu DICT INDEX.|
|Privātais DICT| Viens katram fontam DICT.|

Tikai pirmās trīs struktūras ir balstītas uz fiksētām atrašanās vietām. Atlikušie tiek sasniegti ar nobīdēm, un to secību var mainīt.

### Datu veidi

CFF2 faila formātā tiek izmantoti šādi datu veidi.

|Nosaukums |Diapazons |Apraksts|
---|---|---|
|uint8 |0 līdz 255 |8 bitu neparakstīts numurs|
|uint16 |0 līdz 65535| 16 bitu neparakstīts numurs|
|uint32 |0 līdz 4294967295| 32 bitu neparakstīts numurs|
|Nobīde |atšķiras| 1, 2, 3 vai 4 baitu nobīdes (norāda indeksa tabulas laukā OffSize)|
|OffSize |1 līdz 4| 1 baita neparakstīts numurs norāda nobīdes lauka vai lauku lielumu|

Tas saglabā visus vairāku baitu skaitliskos datus un nobīdes laukus lielo baitu secībā. CFF2 formātā nav iekļauti polsterējuma baiti, jo tas neievēro nekādus izlīdzināšanas ierobežojumus.

### DICT dati

CFF2 faili satur fontu vārdnīcas datus kā atslēgu un vērtību pārus kompaktā marķierizētā formātā. Vārdnīcas atslēgas tiek kodētas kā 1 vai 2 baitu operatori, un vārdnīcas vērtības tiek kodētas kā mainīga izmēra ciparu operandi. Ir trīs struktūras, kurās tiek izmantots DICT datu formāts: Top DICT, Font DICT un Privāts DICT. Ir definēti vairāki dažāda lieluma veselu skaitļu operandu veidi un tiek kodēti, kā parādīts nākamajā tabulā (operanda pirmais baits ir b0, otrais ir b1 un tā tālāk).

|Izmērs |b0 diapazons |Vērtību diapazons |Vērtības aprēķins|
---|---|---|---|
|1 |32 līdz 246| -107 līdz +107 |b0 - 139|
|2	|247 to 250|	+108 to +1131	|(b0 - 247) * 256 + b1 + 108|
|2	|251 to 254|	-1131 to -108|	-(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 līdz +32767| b1 << 8 | b2|
|5 |29| -(2^31) līdz +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Virsraksts

Binārie dati sākas ar galveni, kura formāts ir parādīts tabulā zemāk.

|Tips |Vārds |Apraksts|
---|---|---|
|uint8| majorVersion| Formatējiet galveno versiju. Iestatīt uz 2.|
|uint8| minorVersion| Formatējiet mazo versiju. Iestatīt uz nulli.|
|uint8| headerSize| Galvenes lielums (baitos).|
|uint16| topDictLength| Top DICT struktūras garums baitos.|

## Atsauces

 * [CFF2 faila formāts](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

