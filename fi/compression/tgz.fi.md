{
  "date": "2022-03-02",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGZ-tiedosto - Gzipped Tar-tiedosto",
  "description": "Opi TGZ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TGZ-tiedostoja.",
  "linktitle": "TGZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tg-fiz"
}
},
  "lastmod": "2022-03-02"
}

## Mikä on TGZ-tiedosto?

Tiedosto, jonka laajennus on .tgz, on TAR-arkistotiedosto, joka koostuu useista tiedostoista ja kansioista ja joka on pakattu Gnu Zip (gzip) -pakkausohjelmistolla. [TAR](/compression/tar/)-tiedosto yhdistää tavallisesti useita tiedostoja yhdeksi tiedostoksi varmuuskopiointia tai Internetin kautta jakelua varten. Se puretaan tiedostoa, kunnes se pakataan gzip-ohjelmistolla, minkä jälkeen siitä tulee TGZ-tiedosto. TGZ-tiedostot, koska ne ovat pakattuja tiedostoja, vievät vähemmän levytilaa ja ovat helposti siirrettävissä Internetin kautta sähköpostitse. Joitakin sovelluksia, jotka voivat avata TGZ-tiedostoja, ovat WinZip, Apple Archive Utility, 7-Zip ja WinRAR. TGZ-tiedostoja käytetään enimmäkseen UNIX- ja Linux-järjestelmissä.

## TGZ tiedostomuoto

TGZ-tiedostot tallennetaan pakattuina binääritiedostoina käyttämällä [GZ](/compression/gz/)-pakkausalgoritmia.

## .tgz-tiedoston purkaminen Linuxissa

Linux/Unix-käyttöjärjestelmässä seuraavaa komentoa voidaan käyttää TGZ-tiedostojen purkamiseen komentoriviltä.

```
tar zxvf tgzCompressedFile.tgz
```

Yllä oleva komento purkaa pakatun TGZ-tiedoston ja purkaa sen tiedostot TAR-arkistosta levylle.
## Viitteet ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)


