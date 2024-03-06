{
  "date": "2020-11-11",
  "keywords": [
"NSF",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par NSF failu formātu un API, kas var izveidot un atvērt NSF failus.",
  "title": "NSF faila formāts — Lotus Notes datu bāzes formāts",
  "linktitle": "NSF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ns-lvf"
}
},
  "lastmod": "2020-08-12"
}

## Kas ir NSF fails?

Fails ar paplašinājumu .nsf (Notes Storage Facility) ir datu bāzes faila formāts, ko izmanto [IBM Notes software](https://en.wikipedia.org/wiki/HCL_Domino), kas iepriekš bija pazīstams kā Lotus Notes. Tā nosaka shēmu dažāda veida objektu, piemēram, e-pastu, tikšanās, dokumentu, veidlapu un skatu glabāšanai. Visa šī informācija ir ietverta vienā NSF failā biznesa sadarbībai, kas ir līdzīgs PST/OST failam. Dažas lietojumprogrammas, kas var atvērt NSF failus, ir IBM Lotus Notes un IBM Domino.

## NSF faila formāta specifikācijas

NSF faili ir bināri, un to specifikācijas ir pieejamas Joahims Mets vietnē [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). Saskaņā ar šo informāciju NSF fails sastāv no:

 * Faila galvene
 * Datu bāzes galvene

Turklāt tas sastāv no:

 * Superbloks
 * Kausa deskriptora bloks
 * Bitkarte
 * Ierakstu pārvietošanas vektora spainis
 * Kopsavilkuma spaiņi
 * Nekopsavilkuma spaiņi


### NSF faila galvene

NSF faila galvenes izmērs ir 6 baiti. Tas sastāv no:

|Nobīde|Izmērs|Vērtība|Apraksts|
---|---|---|---|
0|2|0x1a 0x00|Paraksts|
2|4| |Datubāzes galvenes izmērs|

### Datu bāzes galvene

NSD datu bāzes galvenē ir šādas apstiprinātās vērtības.

 * Informācija par datu bāzi
   * Datu bāzes identifikators (DBID)
 * Informācija par replikāciju
 * Datu bāzes informācijas bufera karodziņi
   * Nosaukums
   * Kategorijas
   * Klase
   * Dizaina klase (veidnes nosaukums)
 * Īpaši piezīmju identifikatori
 * Polsterējums
 * Informācija par datu bāzi 2
 * Informācija par datu bāzi 3
 * Informācija par datu bāzi 4
 * Informācija par datu bāzi 5
 * Polsterējums
 * Datu bāzes instances identifikators (DBIID)
 * Replikācijas vēsture

## Atsauces

 * [NSF formāts — Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

