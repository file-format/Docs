{
  "date": "2020-08-20",
  "keywords": [
"otf tiedosto",
"otf tiedostomuoto",
"mikä on otf-tiedosto",
"tiedosto",
"otf esimerkki",
"otf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTF - TrueType-fonttitiedostomuoto",
  "description": "Opi OTF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OTF-tiedostoja.",
  "linktitle": "OTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-ot-fif"
}
},
  "lastmod": "2020-09-21"
}

## Mikä on OTF-tiedosto?

Tiedosto, jonka pääte on .otf, viittaa OpenType-kirjasinmuotoon. OTF-fonttimuoto on skaalattavampi ja laajentaa digitaalisen typografian [TTF](/font/ttf/)-muotojen olemassa olevia ominaisuuksia. Microsoftin ja Adoben kehittämä OTF yhdistää PostScript- ja TrueType-kirjasinmuotojen ominaisuudet. Tämä tekee OTF-formaatista enemmistön kirjoitusjärjestelmiin sopivan, ja siksi sitä käytetään yhtenäisesti suurilla tietokonealustoilla. OpenType-kirjasinmuotoa tukevat Mac OS X ja Windows 2000 ja uudemmat.

## Lyhyt historia

The requirement of OpenType fonts originated as a requirement for a more expressive font format that could handle fine typography. In addition, it was aimed to meet the requirements of complex behaviour of many of the world's writing systems. Microsoft attempted to license Apple's advanced typography technology, known as GX Typography, in the early 1990's. This didn't go well and as a result, Microsoft started enhancing its owns TrueType font technology in 1994. Muutokset sisälsivät myös sopivamman kirjasinmuodon, joka täyttää myös Adoben Type 1 (PostScript) -kirjasinmuotojen ominaisuudet.

Adobe liittyi Microsoftin kanssa vuonna 1996 sen pyrkimyksiin korvata sekä Applen TrueType että omat Type 1 -kirjasinformaatit. Tämä johti molempien taustalla olevien kirjasinmuotojen yhdistämiseen rajoitusten voittamiseksi ja uusien laajennusten lisäämiseksi. Tämä uusi tekniikka esiteltiin samana vuonna nimellä **OpenType**.

## OTF-tiedostomuodon tekniset tiedot

OTF specifications are available publicly by Microsoft and can be referred to from developer's perspective. Like TTF, it uses the same 'sfnt' container structure and is compatible with the TrueType specifications. Data inside an OpenType font file is used for different purposes such as calculating the text layout, defining glyphs as TrueType or Compact Font Format (CFF) outlines, providing monochromatic or color bitmaps or SVG documents as alternate glyph descriptions, and meta-data information.

### OTF-tietotyypit
OTF-tiedostot käyttävät seuraavia tietotyyppejä, jotka kaikki ovat Big Endianissa.

|Tietotyyppi| Kuvaus|
---|---|
|uint8| 8-bittinen etumerkitön kokonaisluku.|
|int8| 8-bittinen etumerkillinen kokonaisluku.|
|uint16| 16-bittinen etumerkitön kokonaisluku.|
|int16| 16-bittinen etumerkillinen kokonaisluku.|
|uint24| 24-bittinen etumerkitön kokonaisluku.|
|uint32| 32-bittinen etumerkitön kokonaisluku.|
|int32| 32-bittinen etumerkillinen kokonaisluku.|
|Kiinteä| 32-bittinen etumerkillä varustettu kiinteän pisteen numero (16.16)|
|FWORD| int16, joka kuvaa määrää kirjasinsuunnitteluyksiköissä.|
|UFWORD| uint16, joka kuvaa määrää kirjasinsuunnitteluyksiköissä.|
|F2DOT14| 16-bittinen etumerkillinen kiinteä luku, jonka murto-osa on 14 bittiä (2.14).|
|LONGDATETIME| Päivämäärä ja aika esitetään sekunteina kello 12:00 keskiyöstä, 1. tammikuuta 1904, UTC. Arvo esitetään etumerkillisenä 64-bittisenä kokonaislukuna.|
|Tagi| Neljän uint8:n joukko (pituus = 32 bittiä), jota käytetään tunnistamaan taulukko, suunnitteluvariaatioakseli, komentosarja, kielijärjestelmä, ominaisuus tai perusviiva|
|Offset16| Lyhyt offset taulukkoon, sama kuin uint16, NULL offset = 0x0000|
|Offset32| Pitkä offset taulukkoon, sama kuin uint32, NULL offset = 0x00000000|
|Versio16Piste16| Pakattu 32-bittinen arvo sekä pää- että sivuversionumerot. (Katso taulukon versionumerot.)|

### OTF-taulukkohakemisto

OTF-tiedosto alkaa taulukkohakemistosta. Tämä hakemisto on ylätason kokoelma fonttitiedoston taulukoita. Tiedoston fonttien määrästä riippuen taulukkohakemisto voi sijaita eri paikassa tiedostossa. Jos esimerkiksi kirjasintiedostossa on vain yksi fontti, taulukkohakemisto alkaa tiedoston tavusta 0. Jos OpenType-fontteja on useita,
taulukkohakemiston alku on osoitettu TTCHeaderissä.

|Tyyppi |Nimi |Kuvaus|
---|---|---|
|uint32 |sfntVersion| 0x00010000 tai 0x4F54544F ('OTTO')|
|uint16| numTables |Taulukoiden lukumäärä.|
|uint16|	searchRange	|Maximum power of 2 less than or equal to numTables, times 16 ((2\**floor(log2(numTables))) * 16, jossa ** on eksponentiooperaattori).|
|uint16 |entrySelector Log2, jonka maksimiteho on 2 pienempi tai yhtä suuri kuin numTables (log2(searchRange/16), joka on yhtä suuri kuin floor(log2(numTables))).|
|uint16	|rangeShift	|numTables times 16, minus searchRange ((numTables * 16) - hakualue).|
|tableRecord| tableRecords[numTables] |Taulukon tietuetaulukko — yksi jokaista fontin ylätason taulukkoa kohden|


### Taulukkotietue

Jokaiselle fontin ylimmän tason taulukolle on taulukkotietue, joka koostuu seuraavista kentistä.

|Tyyppi| Nimi| Kuvaus|
---|---|---|
|Tagi| tableTag| Taulukon tunniste.|
|uint32| tarkistussumma| Tämän taulukon tarkistussumma.|
|Offset32| offset| Poikkeama fonttitiedoston alusta.|
|uint32| pituus Tämän taulukon pituus.|

Jokainen OpenType-fonttitiedoston taulukko on esitetty nimillä, jotka tunnetaan nimellä taulukkotunnisteet. On välttämätöntä, että kaikki taulukon tietueet lajitellaan nousevaan järjestykseen tunnisteen mukaan.

## Viitteet
 * [Microsoftin OpenType-fonttimääritykset](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType Overview](https://learn.microsoft.com/en-us/typography/truetype/)

