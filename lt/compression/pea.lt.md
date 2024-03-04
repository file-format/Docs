{
  "date": "2021-04-21",
  "keywords": [
"žirnių failas",
"žirnių failo formatas",
"kas yra žirnių failas",
"failą",
"žirnių pavyzdys",
"pea failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEA – PeaZip archyvo failo formatas",
  "description": "Sužinokite apie PEA failo formatą ir API, kurios gali kurti ir atidaryti PEA failus.",
  "linktitle": "PEA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pe-lta"
}
},
  "lastmod": "2021-04-21"
}

## Kas yra PEA failas?

Failas su plėtiniu .pea, akronimu Pack, Encrypt ir Authenticate, yra [zip](/compression/zip/) archyvas, sukurtas naudojant [PeaZip](https://peazip.github.io/) archyvavimo programinę įrangą. Jame yra suspaudimas ir kelių garsų išvestis bei lankstus saugos modelis naudojant autentifikuotą šifravimą ir kriptografiją. Tai užtikrina ir privatumą, ir duomenų autentifikavimą. PeaZip programa yra prieinama kaip atvirojo kodo variklis, kurį galima sudaryti skirtingoms OS pagal reikalavimus.

## PEA failo formatas

[PEA file format specifications](https://peazip.github.io/pea_help.pdf) yra viešai prieinami kūrėjams. PEA archyvai yra dvejetainiai failai su lanksčiu saugos modeliu ir pertekliniais vientisumo patikrais nuo kontrolinių sumų iki kriptografiškai stiprių maišų. Tai apibrėžia tris skirtingus valdymo lygius:

 * Srautai – faktinis išvesties duomenų srautas, sudarytas iš kelių įvesties failų ir gali būti įrašytas į kelis išvesties tomus
 * Objektai – įvesties failai ir aplankai, siunčiami į .pea archyvą
 * Apimtys – išvesties archyvo failas, kurį galima išplėsti iki vartotojo nustatyto dydžio

Kiekvienas iš jų yra neprivalomas ir gali būti įtrauktas pagal vartotojo reikalavimus. PEA failo formatas gali saugoti vieną srautą su neribotais objektais. Kiekvienas srautas yra iki 2^64 baitų dydžio.

PEA failai siūlo neprivalomą vientisumo patikrinimą ir autentifikuotą šifravimą naudojant AES EAX arba HMAC režimu, arba Twofish ir Serpent EAX režimu.

### PEA archyvo antraštė

Archyvo antraštė yra 10 baitų ir jos struktūra yra tokia.

|Baitai|Aprašymas|
---|---|
|1 | Magiškasis baitų laukas failo formato išaiškinimui: $EA|
|1 | Versijos numeris|
|1 | Pataisymo numeris|
|1 | Garsumo valdymo schema|
|1 | OS, kurioje buvo sukurtas srautas, deklaravimas|
|1 | OS datos ir laiko kodavimo deklaravimas|
|1 | Deklaruojamas objektų pavadinimas simbolių kodavimas|
|1 | CPU tipo (užkoduotas 7 bitais) ir endianness (msb) deklaravimas |
|1 | Rezervuotas naudojimui ateityje|

## Nuorodos

* [PEA failo formato specifikacijos] (https://peazip.github.io/pea_help.pdf)

* [PEA failo formatas](https://peazip.github.io/pea-file-format.html#.pea_specifications)


