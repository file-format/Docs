{
  "date": "2020-08-20",
  "keywords": [
"fon tiedosto",
"fon tiedostomuoto",
"mikä on fon-tiedosto",
"tiedosto",
"hyvä esimerkki",
"fon tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FON - Fonttikirjastotiedosto",
  "description": "Opi FON-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata FON-tiedostoja.",
  "linktitle": "FON",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fo-fin"
}
},
  "lastmod": "2020-10-30"
}

## Mikä on FON-tiedosto?

Tiedosto, jonka laajennus on .fon, on Microsoft Windows 3.x -fonttikirjasto, joka on itse asiassa suoritettava tiedosto, mutta joka on nimetty uudelleen .foniksi. Se on kokoelma [.fnt](/font/fnt/)-tiedostoja itsessään, ja sovellukset viittaavat siihen käyttäessään järjestelmäfonttia. Siksi se toimii resurssitiedostona. Se voidaan avata Windows-käyttöjärjestelmässä Microsoft Windows Font View -sovelluksella.

## FON tiedostomuoto

FON-tiedosto sisältää fonttiresursseja ja siinä on Resource (.res) -tiedostomuoto. .res-tiedostomuoto määrittää tiedoston otsikon sekä tietoosion tiedot. .fnt on myös resurssitiedosto, joka sisältyy resurssitiedostoon. FON-tiedostoilla on binääritiedostomuoto ja sovellus/oktettivirran MIME-tyyppi.

Fonttiresursseja, toisin kuin muun tyyppisiä resursseja, ei lisätä sovelluksen resursseihin. Sen sijaan ne lisätään EXE-tiedostoihin ja nimetään uudelleen .fon-tiedostoiksi, mikä johtaa kirjastotiedostoihin sovellusten sijaan. Useat yksittäiset kirjasimet muodostavat kirjasinryhmän osia, joissa jokainen ryhmä noudattaa resurssiryhmärakennetta. Fonttiresurssit käyttävät näitä resurssiryhmärakenteita. Ryhmän otsikossa on kaikki tiedot, joita tarvitaan tietyn kirjasimen käyttämiseen ryhmästä. Fonttikomponenttiresurssilla on seuraava muoto.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/font/fnt/) file)
```
Yhdellä .rc-resurssitiedostolla voi olla useita resurssimäärityksiä. Fonttiryhmät voivat olla missä tahansa resurssitiedostossa, eikä niiden tarvitse olla vierekkäisiä. RES-tiedostoja luovien ohjelmien on lisättävä FONTDIR manuaalisesti. Seuraavassa on ryhmän otsikon rakenne.

```
[Normaali resurssin otsikko (tyyppi = 7)]

WORD NumberOfFonts; // Kokonaismäärä .RES-tiedostossa
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
WORD dfType;
WORD dfPoints;
WORD dfVertRes;
WORD dfHorizRes;
WORD dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfItalic;
BYTE dfUnderline;
BYTE dfStrikeOut;
WORD dfPaino;
BYTE dfCharSet;
WORD dfPixWidth;
WORD dfPixHeight;
BYTE dfPitchAndFamily;
WORD dfAvgWidth;
WORD dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORD dfWidthBytes;
DWORD dfDevice;
DWORD dfFace;
DWORD dfReserved;
char szDeviceName[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

