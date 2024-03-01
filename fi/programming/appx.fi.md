{
  "date": "2021-04-22",
  "keywords": [
"appx-tiedosto",
"laajennus",
"muoto",
"kuinka avata appx-tiedosto",
"appx-tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APPX - Mikä on APPX-tiedosto?",
  "description": "Lisätietoja APPX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata APPX-tiedostoja.",
  "linktitle": "APPX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-app-fix"
}
},
  "lastmod": "2021-12-16"
}

## Mikä on APPX-tiedosto?

APPX-tiedosto on jaettava pakettitiedostomuoto, jota käytetään sovelluksen jakeluun ja asentamiseen. Se esiteltiin Windows 8:n kanssa julkaistavaksi Microsoft Windows Storessa. Se sisältää kaikki Windows-sovelluksen asentamiseen tarvittavat tiedostot. Näitä ovat metatiedot, tiedostot ja tunnistetiedot. Nykyaikaisempi pakkaustiedostomuoto on MSIX, jota käytetään tällä hetkellä yleisemmin kuin APPX.

## APPX-tiedostomuoto - lisätietoja

APPX-tiedostot tallennetaan pakattuina tiedostoina [ZIP](/compression/zip/)-tiedostomuodossa. Tämä tekee koko paketista pienennetyn tiedostokoon arkistotiedoston, joka on helppo ladata Microsoft Storeen.

## Kuinka katsella tiedostoja APPX-tiedostossa?

Jotta voit tarkastella APPX-tiedoston sisältöä tai tiedostoja, sinun on noudatettava seuraavia vaiheita.

 1. Koska APPX-tiedostot tallennetaan pakattuina ZIP-tiedostoina, nimeä tiedosto uudelleen .zip-tunnisteeksi
 1. Käytä mitä tahansa purkutyökalua, kuten 7-Zip, WinZip tai WinRAR purkaaksesi APPX-tiedoston sisältämät tiedostot

## Kuinka luoda APPX-tiedosto?

APPX-tiedostoja voidaan luoda kahdella tavalla.

 1. MakeApp.exe-sovelluksen avulla - {{HYPERLINKKI}} luodaan sekä sovelluspaketteja (.msix tai .appx) että sovelluspakettien tiedostoja .msixbundle tai .appxbundle). Lisäksi se voi purkaa tiedostoja sovelluspaketista. MakeApp.exe on saatavana Windows 10 SDK:n kanssa ja sitä voidaan käyttää komentokehotteesta.
 1. Microsoft Visual Studion käyttäminen - Kehittäjät yleensä [create APPX files](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) käyttävät Microsoft Visual Studiota. Kun sovelluskehitys on valmis ja sovellus on valmis julkaistavaksi, APPX-pakettitiedosto voidaan luoda julkaisemalla se Visual Studiosta.

## Viitteet

 * [Luo MSIX-paketti tai -paketti MakeAppx.exe-sovelluksella](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
 * [Luo APPX-tiedostoja Microsoft Visual Studiolla](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

