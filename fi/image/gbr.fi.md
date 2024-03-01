{
  "date": "2019-10-11",
  "keywords": [
"gbr tiedosto",
"gbr tiedostomuoto",
"mikä on gbr-tiedosto",
"tiedosto",
"gbr esimerkki",
"gbr tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GBR-tiedostomuoto - Gerber-tiedostomuoto PCB:lle",
  "description": "Opi GBR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata GBR-tiedostoja.",
  "linktitle": "GBR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gb-fir"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on GBR-tiedosto?

Tiedosto, jonka laajennus on .gbr, on Gerber-kuvatiedostomuoto painetun piirilevyn (PCB) suunnittelutiedon siirtoon. Sen on kehittänyt Ucamco. Piirilevyjen suunnittelutiedot ovat valmistusteollisuuden tarvitsemien pääkomponenttien käsittelyssä. GRB-tiedosto sisältää PCB-tietoja, kuten kuparikerroksia, juotosmaskin, selitteen sekä pora- ja reittitiedot. Sitä voidaan käyttää tietojen, kuten piirilevyjen valmistusominaisuuksien, kuten paksuuden tai viimeistelyn, siirtämiseen standardoidussa muodossa. Kaikki piirilevyjen suunnittelujärjestelmät tuottavat Gerber-tiedostoja, joita piirilevyjen valmistusjärjestelmät voivat käsitellä. GBR-tiedostoista on nyt tullut de facto standardi painetun piirilevyn (PCB) suunnittelun tiedonsiirrolle. Ucamco on toimittanut [free online viewer](https://gerber-viewer.ucamco.com/) GBR-tiedostomuotojen avaamiseen ja katseluun.

## GBR-tiedostomuoto

GBR on ihmisen luettavissa oleva UTF-8-muoto, joka koostuu vain 27 komennosta. Tämän lyhyen komentoluettelon ja sen tiiviyden ansiosta GBR:n virheenkorjaus on helppoa. Gerber on pohjimmiltaan avoin vektorimuoto 2D-binäärikuville. Metatiedot siirretään kuvien mukana Attribuuttien kautta. Yksittäinen GRB-tiedosto määrittää yhden kuvan eikä vaadi minkään liitteenä olevien tiedostojen tai ulkoisten parametrien tulkitsemista. Yksi kuva tarvitsee vain yhden tiedoston. Se käyttää 7-bittisiä ASCII-merkkejä kaikissa spesifikaatioissa määritellyissä tulostettavissa olevissa komennoissa ja nimissä. Tämä kattaa täysin kuvan luomisen.

### Esimerkki GBR-tiedostosta

Seuraavassa on esimerkki Gerber-tiedostosta, joka luo halkaisijaltaan 1,5 mm:n ympyrän, jonka keskipiste on origossa. Jokaisella rivillä on yksi komento.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Viitteet

 * [Gerber-muoto](https://www.ucamco.com/en/gerber)

