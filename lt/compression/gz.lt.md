{
  "date": "2019-10-11",
  "keywords": [
"gz failą",
"gz failo formatas",
"kas yra gz failas",
"failą",
"gz pavyzdys",
"gz failo plėtinį",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GZ failo formatas – GNU ZIP archyvo failas",
  "description": "Sužinokite, kas yra GZ failas ir API, kurios gali kurti ir atidaryti GZ failus.",
  "linktitle": "GZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-g-ltz"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra GZ failas?

GZ failas yra suspaustas archyvas, sukurtas naudojant standartinį [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) glaudinimo algoritmą. Jame gali būti keli suspausti failai, katalogai ir failų šakneliai. Šis formatas iš pradžių buvo sukurtas siekiant pakeisti glaudinimo formatus UNIX sistemose. ir vis dar yra vienas iš labiausiai paplitusių archyvų tipų Linux sistemose. Tokios programos kaip [WinZip](https://www.winzip.com/en/) gali atidaryti GZ failus ir peržiūrėti jų turinį Windows ir MacOS.

## GZ failo formatas – daugiau informacijos

Gzip naudoja [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) algoritmą archyvui suspausti ir skiriasi nuo [ZIP](/compression/zip/) archyvo formato tuo, kad taiko glaudinimo algoritmą visam archyvui, o ne atskiriems failams. Internet Engineering Task Force (IETF) paskelbtoje GZIP failo formato specifikacijų versijoje 4.3 yra išsami informacija apie failo formatą. Failo formatas susideda iš:

* Failo antraštė

* Pasirenkamos antraštės

* Suspausti duomenys

* Failo poraštė


## GZ failo antraštė Nr.

GZ failo antraštę sudaro 10 baitų, kaip nurodyta toliau:

|Poslinkis|Dydis|Vertė|Aprašymas
---|---|---|---|
|0|2|0x1f 0x8b|Magiškas skaičius, identifikuojantis failo tipą
|2|1| |Compression Method * 0–7 (rezervuota) * 8 (išmesti)
|3|1| |Failų vėliavėlės
|4|4| |32 bitų laiko žyma
|8|1| |Suspaudimo vėliavėlės
|9|1| |Operacinės sistemos ID

### Failų vėliavėlės ###

|Vertė|Identifier|Aprašymas
---|---|---|
|0x01|FTEXT|Jei nustatyta, nesuglaudinti duomenys turi būti traktuojami kaip tekstas, o ne dvejetainiai duomenys. Ši žyma rodo kelių platformų tekstinių failų eilutės pabaigos konvertavimą, bet to neįgyvendina.
|0x02|FHCRC|Faile yra antraštės kontrolinė suma (CRC-16)
|0x04|FEXTRA|Faile yra papildomų laukų
|0x08|FNAME|Faile yra originali failo pavadinimo eilutė
|0x10|FCOMMENT|Faile yra komentaras
|0x20| |Rezervuota
|0x40| |Rezervuota
|0x80| |Rezervuota

### Operacinė sistema ###

|Vertė|Aprašymas
---|---|
|0|FAT failų sistema (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (arba OpenVMS)
|3|Unix
|4|VM/TVS
|5|Atari TOS
|6|HPFS failų sistema (OS/2, NT)
|7|Macintosh
|8|Z sistema
|9|CP/M
|10|TOPS-20
|11|NTFS failų sistema (NT)
|12|QDOS
|13|Gilės RISCOS
|255|nežinoma

## GZ pasirenkamos antraštės ##

Neprivalomos papildomos antraštės yra tos, kurios pažymėtos failo vėliavėlėmis ir apima tokią informaciją kaip pradinis failo pavadinimas, papildomi laukai, komentarai ir antraštės kontrolinė suma.

## Suspausti duomenys ##

Šiame skyriuje yra suspausti duomenys naudojant DEFLATE glaudinimo algoritmą.

## GZ failo poraštė Nr.

Failo poraštė yra 8 baitų dydžio, joje yra ši informacija.

|Offsetas|Dydis|Aprašymas
---|---|---|
|0|4|Kontrolinė suma (CRC-32)
|4|4|Nesuglaudinto duomenų dydžio reikšmė baitais

## Nuorodos Nr.

* [gzip – Vikipedija](https://en.wikipedia.org/wiki/Gzip)

* [RFC1952: GZIP failo formato specifikacija](https://datatracker.ietf.org/doc/html/rfc1952), pateikė IETF.


