{
  "date": "2019-10-11",
  "keywords": [
"rar-tiedosto",
"rar-tiedostomuoto",
"mikä on rar-tiedosto",
"tiedosto",
"harvinainen esimerkki",
"rar tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RAR",
  "description": "Mikä on RAR-tiedostopääte ja API:t, jotka voivat luoda ja avata RAR-tiedostoja.",
  "linktitle": "RAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ra-fir"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on RAR-tiedosto?

Tiedostot, joiden tiedostopääte on .rar, ovat arkistotiedostoja, jotka on luotu tietojen tallentamista varten pakatussa tai normaalissa muodossa. RAR, joka tarkoittaa Roshal ARchive -tiedostomuotoa, on patentoitu tiedostomuoto, jonka loi Eugene Roshal vuonna 1995, joka oli venäläinen ohjelmistoinsinööri. Muotoa käytetään tiedostojen arkistointiin eri menetelmillä, mukaan lukien erilaiset pakkaustekniikat. Windowsille, Linuxille ja MacOS:lle on saatavana useita sovellusohjelmistoja RAR-tiedostojen purkamiseen. RARLAbin WinRAR-ohjelmisto on shareware-tiedostojen arkistointiapuohjelma (ilmainen 40 päivää) Microsoft Windows -alustalle; Sama kirjoittaja Eugene Roshal siirsi ohjelmiston Linuxiin (vain purkajana).

## RAR-tiedostomuodon versiohistoria

* v1.3 (alkuperäinen, ei "Rar!"-allekirjoitusta)

* v1.5

* v2.0 - julkaistu WinRAR 2.0:n ja Rar:n kanssa MS-DOS 2.0:lle

* v2.9 - julkaistu WinRAR-versiossa 3.00

* v5.0 - tukee WinRAR 5.0 ja uudemmat


## RAR-muodon tärkeimmät ominaisuudet

RAR on ollut alalla melko pitkään ja on ollut yksi suosituimmista arkistointitiedostomuodoista. RAR-muodon tärkeimmät ominaisuudet ovat:

**`Korkea pakkaussuhde:`** Ylivoimainen verrattuna [ZIP](/compression/zip/):iin, verrattavissa 7z- ja zipx-muotoon.

**`Suunniteltu vahva tiedostosalaus:`** Salatut RAR4-arkistot käyttävät AES-128-pohjaista salausta, kun taas salatut RAR5-arkistot AES-256-salausta parannetulla avainaikataululla

**`Edistyneet virheenkorjaus- ja tietojen palautusominaisuudet:`** valinnaiset palautustietueet arkiston luonnin aikana

**`Tiedoston koko:`** Vähintään 20 tavua ja enintään 2^63 tavua (8 eksatavua arkiston kokonaiskoosta)

**`Moniosaiset RAR-arkistot:`** Mahdollisuus jakaa suuret arkistot useiksi pienemmiksi tiedostoiksi siirron helpottamiseksi verkon yli. Tässä tapauksessa tiedostotunnisteita kasvatetaan 1:llä edustamaan jaettuja taltioita

## RAR-tiedostomuoto

Täydelliset RAR-muodon spesifikaatiot eivät ole saatavilla julkisesti, ja siksi formaatin yksityiskohtia ei voida muotoilla ytimekkäästi.

### Yleinen arkiston asettelu

Versiossa 5.0 käyttöönotetun RAR-tiedostomuodon yleinen asettelu on seuraava:

|Tiedostomuoto
---|
|Itsepurkautuva moduuli (valinnainen)
|RAR 5.0 Allekirjoitus
|Arkiston salausotsikko (valinnainen)
|Pääarkiston otsikko
|Arkistoi kommenttipalvelun otsikko (valinnainen)
Tiedoston otsikko 1
|Edellisen tiedoston palveluotsikot (NTFS ACL, streamit jne.) (valinnainen)
|...
|Tiedoston otsikko N
|Edellisen tiedoston palveluotsikot (NTFS ACL, streamit jne.) (valinnainen)
|Palautustietue (valinnainen)
|Arkiston loppuotsikko

Tietoja kustakin yllä mainitusta RAR-tiedoston osiosta löytyy asiakirjasta [RAR 5.0 File Format specifications](https://www.rarlab.com/technote.htm#arcstruct).

#### Itsepurkautuvat RAR-arkistot

Jos RAR-tiedosto itsessään purkautuu itsestään, itsepurkautuvat tiedot sisältyvät arkiston allekirjoitusta edeltävän tiedoston alkuun. Sen kokoa ja sisältöä ei ole määritelty.

#### RAR 5.0 -allekirjoitus

RAR-allekirjoitus on 8-tavuinen otsikko, joka koostuu seuraavista maagisista numeroista:

0x 52 61 72 21 1A 07 00

missä

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Viitteet

* [RAR 5.0 -arkistomuoto](https://www.rarlab.com/technote.htm)

* [RAR – Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))


