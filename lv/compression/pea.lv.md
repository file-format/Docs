{
  "date": "2021-04-21",
  "keywords": [
"zirņu fails",
"zirņu faila formāts",
"kas ir zirņu fails",
"failu",
"zirņu piemērs",
"zirņu faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEA - PeaZip arhīva faila formāts",
  "description": "Uzziniet par PEA faila formātu un API, kas var izveidot un atvērt PEA failus.",
  "linktitle": "PEA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pe-lva"
}
},
  "lastmod": "2021-04-21"
}

## Kas ir PEA fails?

Fails ar paplašinājumu .pea, saīsinājums vārdiem Pack, Encrypt un Authenticate, ir [zip](/compression/zip/) arhīvs, kas izveidots ar [PeaZip](https://peazip.github.io/) arhivēšanas lietojumprogrammu. Tam ir saspiešana un vairāku skaļumu izvade, un tas piedāvā elastīgu drošības modeli, izmantojot autentificētu šifrēšanu un kriptogrāfiju. Tas nodrošina gan datu privātumu, gan autentifikāciju. PeaZip utilīta ir pieejama kā atvērtā koda dzinējs, ko var apkopot dažādām operētājsistēmām atbilstoši prasībām.

## PEA faila formāts

[PEA file format specifications](https://peazip.github.io/pea_help.pdf) ir publiski pieejami izstrādātāju uzziņai. PEA arhīvi ir bināri faili ar elastīgu drošības modeli un liekām integritātes pārbaudēm, sākot no kontrolsummām līdz kriptogrāfiski spēcīgām jaukām. Tas nosaka trīs dažādus saziņas līmeņus, ko kontrolēt:

 * Straumes — faktiskā izejas datu straume, ko veido vairāki ievades faili un ko var ierakstīt vairākos izvades sējumos
 * Objekti - ievades faili un mapes, kas nosūtītas uz .pea arhīvu
 * Sējumi - izvades arhīva fails, kuru var paplašināt līdz lietotāja noteiktam izmēram

Katrs no tiem nav obligāts un var tikt iekļauts atbilstoši lietotāja prasībām. PEA faila formāts var saglabāt vienu straumi, kurā ir neierobežoti objekti. Katra straume ir līdz 2^64 baitiem liela.

PEA faili piedāvā izvēles integritātes pārbaudi un autentificētu šifrēšanu, izmantojot AES EAX vai HMAC režīmā vai Twofish un Serpent EAX režīmā.

### PEA arhīva galvene

Arhīva galvene ir 10 baiti, un tās struktūra ir šāda.

|Baiti|Apraksts|
---|---|
|1 | Burvju baitu lauks faila formāta noskaidrošanai: $EA|
|1 | Versijas numurs|
|1 | Pārskatīšanas numurs|
|1 | Skaļuma regulēšanas shēma|
|1 | OS deklarēšana, kurā tika izveidota straume|
|1 | OS datuma un laika kodējuma deklarēšana|
|1 | Deklarējot objektu nosaukumu rakstzīmju kodējums|
|1 | CPU tipa (kodēts 7 bitos) un endianness (msb) deklarēšana |
|1 | Rezervēts turpmākai lietošanai|

## Atsauces

* [PEA faila formāta specifikācijas](https://peazip.github.io/pea_help.pdf)

* [PEA faila formāts](https://peazip.github.io/pea-file-format.html#.pea_specifications)


