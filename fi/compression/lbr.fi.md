{
  "date": "2021-04-08",
  "keywords": [
"mst-tiedosto",
"mst-tiedostomuoto",
"mikä on mst-tiedosto",
"tiedosto",
"mst esimerkki",
"mst tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LBR - LU kirjaston arkiston tiedostomuoto",
  "description": "Opi LBR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LBR-tiedostoja.",
  "linktitle": "LBR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lb-fir"
}
},
  "lastmod": "2021-04-19"
}

## Mikä on LBR-tiedosto?

Tiedosto, jonka pääte on .lbr, on LU-ohjelmalla luotu arkistotiedosto, jota käytettiin CP/M- ja DOS-käyttöjärjestelmissä 1980-luvulla. Sitä ei enää käytetä, ja se on korvattu nykyaikaisilla arkistointitiedostomuodoilla. Muoto ei pakkaa jäsentiedostoja ja toimii näiden konttiarkistoina. Arkistointiominaisuutta käytettiin enimmäkseen arkistoitujen tiedostojen siirtämiseen Internetin kautta. Koska LBR ei tarjonnut pakkausta, muita apuohjelmia, kuten SQ tai CRUNCH, käytettiin jäsentiedostojen pakkaamiseen esiarkistointia varten tai tuloksena olevan arkistotiedoston jälkiarkistointiin sen koon pienentämiseksi.

## LBR-tiedostomuoto

LBR file format was designed by Gary P. Novosielski and has no technical details available publicly. LBR files start with a 0x00 byte, followed by 11 spaces (0x20), then two 0x00 bytes, then two bytes that are not both 0x00. Koska konttitiedostomuoto on, se voidaan purkaa käyttämällä LU.COM- ja NULU.COM-tiedostoja.

## Viitteet

* [LBR - Wikipedia](https://en.wikipedia.org/wiki/LBR_(file_format))


