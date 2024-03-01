{
  "date": "2021-08-13",
  "keywords": [
"sdi tiedosto",
"sdi-tiedostomuoto",
"mikä on sdi-tiedosto",
"tiedosto",
"sdi esimerkki",
"sdi tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi SDI-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SDI-tiedostoja.",
  "title": "SDI - Windows System Deployment Image File",
  "linktitle": "SDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-sd-fii"
}
},
  "lastmod": "2021-08-13"
}

## Mikä on SDI-tiedosto?
Tiedosto, jonka laajennus on .sdi, sisältää latausblobin, käynnistysblobin ja osablobin; käytetään yleisesti Windows Embedded Studiossa RAM-levyjen tai käynnistyslevyjen luomiseen Windowsin lataamista ja asentamista varten. SDI on lyhenne sanoista System Deployment Image. Windows Embedded Studio on ohjelma, jota käytetään levykuvien luomiseen Windowsille. Itse asiassa tämä ohjelma sisältää SDI-tiedostonhallintaohjelman ja komentorivityökalun nimeltä **sdimgr.exe**, molempia voidaan käyttää SDI-kuvien lisäämiseen, luomiseen ja muokkaamiseen.

## SDI-tiedostomuoto
SDI-tiedostomuotoa käytetään laajalti mahdollistamaan virtuaalilevyn käyttö järjestelmän käynnistämiseen. Jotkut Microsoft Windows -versiot mahdollistavat **RAM-käynnistyksen**, mikä on tärkeää ladata SDI-tiedosto muistiin ja sitten käynnistää siitä. SDI-tiedostomuoto mahdollistaa myös verkkokäynnistyksen PXE:n (Preboot Execution Environment) avulla. Sitä käytetään myös kiintolevyn kuvantamiseen.
### SDI-tiedostoosiot
Itse SDI-tiedosto voidaan jakaa seuraaviin osiin:
- **Boot BLOB**: Tämä sisältää varsinaisen käynnistysohjelman, STARTROM.COM. Tämä on analoginen kiintolevyn käynnistyssektorin kanssa.
- **Lataa BLOB**: Tämä sisältää yleensä NTLDR:n ja sen käynnistää käynnistysBLOB.
- **Part BLOB**: Tämä sisältää todellisen käynnistyksen suoritusajan; sisältää myös boot.ini- ja ntdetect.com-tiedostot, joiden pitäisi sijaita ajonaikaisen juurihakemistossa.
- **Disk BLOB**: Tämä on litteä HDD-kuva, joka alkaa MBR:llä. Sitä käytetään kiintolevyn kuvantamiseen käynnistyksen sijaan. Myös vain Disk BLOB -levyjä voidaan asentaa Microsoftin apuohjelmilla.


## Viitteet 

* [Järjestelmän käyttöönottokuva – Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)



