{
  "date": "2020-08-20",
  "keywords": [
"fnt tiedosto",
"fnt-tiedostomuoto",
"mikä on fnt-tiedosto",
"tiedosto",
"fnt esimerkki",
"fnt tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FNT - Windowsin kirjasintiedosto",
  "description": "Opi FNT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata FNT-tiedostoja.",
  "linktitle": "FNT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fn-fit"
}
},
  "lastmod": "2020-10-30"
}

## Mikä on FNT-tiedosto?

Tiedosto, jonka pääte on .fnt, on fonttitiedosto, joka tallentaa yleiset kirjasintiedot Windows-käyttöjärjestelmissä. FNT-tiedostot on useimmiten korvattu TrueType (.TTF)- ja OpenType (.OTF) -tiedostomuodoilla, ja se on toistaiseksi vanhentunut fonttitiedostomuoto. Nämä tiedostot voivat tallentaa yhden arvioijan tai vektorifontin. Kaikki laiteohjaimet tukevat Windows 2.x -fontteja. Kaikki laiteohjaimet eivät kuitenkaan ole käytettävissä
tukee Windows 3.0 -versiota.

## FNT-tiedostomuoto

FNT-tiedostot pystyvät tallentamaan yhden rasteri- tai vektorifontin. GDI käyttää vektorimuotoja useammin kuin rasteri, jossa kunkin charterin glyfi määritellään pienellä bittikartalla. Ilmeinen syy .fnt:n korvaamiseen .ttf:llä ja .otf:llä on sen rasterimuoto.

### Fonttitiedoston otsikko
Sekä rasteri- että vektorifonttitiedostojen alku on yhteinen, ja sitä seuraa eri tiedot jokaisesta tiedostotyypistä. Fonttitiedoston otsikko sisältää Windows 3.0:lle kuusi uutta kenttää, jotka on asetettu nollaan yhteensopivuuden varmistamiseksi tulevien Windows-versioiden kanssa.

 * dLiput
 * dfAspace
 * dfBspace
 * dfCspace
 * dfColorPointer
 * dfReserved1

Lisätietoja Windows 3.0:n ja 2.0:n otsikoista on osoitteessa {{HYPERLINKKI}}.

## Viitteet
 * [Fonttitiedostomuoto](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
 * [Fontin asentaminen tai poistaminen Windowsissa](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8- 7613-c76f-88d043b334b8)

