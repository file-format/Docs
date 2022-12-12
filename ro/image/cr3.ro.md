{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier CR3 - Fișier imagine Canon Raw 3",
  "description":"Aflați despre formatul de fișier CR3 și despre API-urile care pot crea și deschide fișiere CR3.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Ce este un fișier CR3?

Un fișier CR3 este un format de fișier imagine Canon RAW care este creat de camerele digitale Canon selectate. A fost introdus de Canon pentru a înlocui formatul de fișier CR2 și este folosit de unele dintre dispozitivele digitale Canon. Fișierele CR3 stochează datele originale de imagine, fără pierderi, neprocesate, capturate de cameră. Utilizarea acestor imagini brute oferă imagini de înaltă calitate și oferă mult spațiu pentru editare fotografilor. Pe lângă datele principale ale imaginii, fișierele CR3 stochează și informații despre metadate despre imagine.

## Format de fișier CR3

Fișierele CR3 sunt stocate pe disc ca fișier binar în formatul de fișier media de bază ISO (ISO/IEC 14496-12) și includ, de asemenea, [etichete Canon] personalizate (https://exiftool.org/TagNames/Canon.html#uuid). Include, de asemenea, [codecul Canon „crx”](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) care este un amestec de JPEG-LS (Rice-Golomb + RLE codificare) și JPEG-2000 (LeGall 5/3 DWT + cuantificare).

## Etichete personalizate CR3

Fișierele CR3 conțin etichete personalizate pentru diferite scopuri. Unele dintre aceste etichete sunt după cum urmează.

|ID etichetă| Nume etichetă| Inscriptibil |Valori / Note|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP Tags|
|'CMT1' |IFD0| - |--> Etichete EXIF|
|'CMT2' |ExifIFD| - |--> Etichete EXIF|
|'CMT3' |MakerNoteCanon| - |--> Etichete Canon|
|'CMT4' |GPSInfo| - |--> Etichete GPS|
|'CNCV' |CompressorVersion| nu| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP Tags|
|'CNTH' |CanonCNTH| - |--> Canon CNTH Tags|
|'THMB' |Imagine în miniatură| nu| |

## Referințe

* [Format fișier CR2](http://lclevy.free.fr/cr2/)
* [Etichete Canon](https://exiftool.org/TagNames/Canon.html#uuid)

