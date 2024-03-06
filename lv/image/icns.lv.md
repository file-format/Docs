{
  "date": "2021-06-29",
  "keywords": [
"ICNS",
"pagarinājumu",
"failu",
"formātā",
"attēlu",
"Apple ikonas attēls",
"macOS",
"Apple",
"Ikona"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICNS — Apple ikonas attēls",
  "description": "Uzziniet par ICNS failu formātu un API, kas var izveidot un atvērt ICNS failus.",
  "linktitle": "ICNS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-icn-lvs"
}
},
  "lastmod": "2021-06-29"
}

## Kas ir ICNS fails? ##

Ikonu formātu, ko izmanto macOS programmas, sauc par ICNS failu. Tas pieļauj 1 bitu un 8 bitu alfa joslas un saglabā vienu vai vairākus attēlus, kas parasti ir izgatavoti no [PNG](/image/png/) dokumentiem. Programmas ikona macOS pārlūkprogrammā un saskarnē tiek parādīta, izmantojot ICNS failus.

Atkarībā no atrašanās vietas vienai stila ikonai var būt vairāki iestatījumi. ICNS formātā ir veiktas daudzas izmaiņas, un tas ir attīstījies tiktāl, ka tagad to var izmantot kā dažādu saderīgu formātu pamatu. Šeit ir daži citi svarīgi punkti, kas jums jāzina:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource un Mac OS icons Resource ir daži no citiem nosaukumiem. 

* Ikonu informācijai tiek izmantots avots resursu filiālē.

* Lielākajā daļā gadījumu failā ir daudz attēlu. Atbalstītie attēla izmēri ir 1612 kvadrātveida pikseļi un 1024, 512, 256, 128, 48, 32 un 16 pikseļi kvadrātā.



## ICNS faila formāts ##

ICNS datu formāts ir kapsula vienam vai vairākiem attēliem, kas atbalsta 1 bitu joslas un daudzus attēla stāvokļus.
Operētājsistēma var mainīt ikonu attēlu izmērus, lai tie atbilstu vajadzīgajam displeja izmēram. Lielāki ikonu attēli parasti tiek saglabāti kā [JPEG](/image/jpeg/) 2000 vai [PNG](/image/png/) faili. Ir iespējams gan saspiestu, gan nesaspiestu ICNS failu veids.

Galvenes un bināro ikonu dati veido ICNS faila struktūru. Galvenē ir 8 baiti datu, no kuriem četri ir burtiski, bet četri — faila garums. Katra ikonas attēla veids un izmērs tiek saglabāts ikonu datu sadaļā, kam seko binārie attēla dati. Attēla izmērs nosaka binārās sadaļas izmēru.

## Tehniskā specifikācija Nr.

### Virsraksts ###

|Nobīde|Izmērs|Mērķis
---|---|---|
|0|4|Maģiskais burts, ir jābūt icns” (0x69, 0x63, 0x6e, 0x73)
|4|4|Faila garums baitos, vispirms msb


### Ikonu dati ###

|Nobīde|Izmērs|Mērķis
---|---|---|
|0|4|Ikonas veids
|4|4|Datu garums, baitos (ieskaitot veidu un garumu), vispirms msb
|8|Mainīgs|Ikonu dati

### Saspiešana ###

Pikseļu dati ir zināmā mērā saspiesti. 32 bitu (is32, il32, ih32, it32) un ARGB (ic04, ic05) pikseļi bieži tiek saspiesti (katram kanālam) līdzīgi kā PackBits.

|Lead Value|Astes baiti|Rezultāts (nesaspiests)
---|---|---|
|0 - 127|1 - 128|1 - 128 baiti
|128 - 255|1 baits|3 - 130 kopijas

## Atsauce Nr.

* [ICNS — Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)


