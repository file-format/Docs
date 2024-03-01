{
  "date": "2020-08-20",
  "keywords": [
"cff2 tiedosto",
"cff2 tiedostomuoto",
"mikä on cff2-tiedosto",
"tiedosto",
"cff2 esimerkki",
"cff2 tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF2 - Compact Font File Format versio 2",
  "description": "Opi CFF2-tiedostomuodosta ja sovellusliittymistä CFF2-tiedostojen luomiseen ja avaamiseen.",
  "linktitle": "CFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cff-fi2"
}
},
  "lastmod": "2020-10-21"
}

## Mikä on CFF2-tiedosto?

CFF2 file format is the version 2.0 of the CFF file format and allows efficient storage of glyph outlines and metadata similar to the CFF file format. CFF2 differs from CFF in that it is intended to be used in the context of an OpenType font as a 'sfnt' table with the tag CFF2. Sitä ei voi käyttää erillisenä ohjelmana, ja se riippuu muiden OpenType-taulukoiden tiedoista.

## CFF2 tiedostomuoto

[CFF2 file format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) sisältää tietoja sisäisestä tietojen asettelusta, tietotyypeistä, taulukoista ja muista tiedostomuodon sisäisistä tiedoista. Se voidaan viitata kehittäjän viitteeksi. Jotkut näistä tiedoista ovat seuraavat.

### Tietojen asettelu

CFF2-tiedostomuodon binääridata on loogisesti järjestetty useiksi erillisiksi tietorakenteiksi. Binääritietojen asettelu on seuraavan taulukon mukainen.

|Syöttö |Kommentit|
---|---|
|Otsikko |Kiinteä sijainti|
|Paras DICT| Kiinteä sijainti|
|Global Subr INDEKSI| Kiinteä sijainti|
|Variaatio |Kauppa|
|FDValitse |Näytä vain, jos Font DICT INDEX -hakemistossa on useampi kuin yksi Font DICT.|
|Fontti DICT INDEX ||
|Fontti DICT| Sisältyy Font DICT INDEX.|
|Yksityinen DICT| Yksi per Font DICT.|

Vain kolme ensimmäistä rakennetta perustuvat kiinteisiin paikkoihin. Jäljelle jäävät saavutetaan offsettien kautta, ja niiden järjestystä voidaan muuttaa.

### Tietotyypit

CFF2-tiedostomuoto käyttää seuraavia tietotyyppejä.

|Nimi |Alue |Kuvaus|
---|---|---|
|uint8 |0 - 255 |8-bittinen etumerkitön numero|
|uint16 |0 - 65535| 16-bittinen etumerkitön numero|
|uint32 |0 - 4294967295| 32-bittinen etumerkitön numero|
|Poikkeama |vaihtelee| 1, 2, 3 tai 4 tavun siirtymät (määritetty OffSize-kentässä hakemistotaulukossa)|
|OffSize |1-4| 1-tavuinen etumerkitön numero määrittää Offset-kentän tai kenttien koon|

Se tallentaa kaikki monitavuiset numeeriset tiedot ja offset-kentät big endian tavujärjestyksessä. CFF2-muoto ei sisällä täytetavuja, koska se ei noudata kohdistusrajoituksia.

### DICT-tiedot

CFF2-tiedostot sisältävät fonttisanakirjan tiedot avain-arvo-pareina kompaktissa tokenoidussa muodossa. Sanakirjan avaimet on koodattu 1- tai 2-tavuisina operaattoreina ja sanakirjan arvot muuttuvan kokoisina numeerisina operandeina. On olemassa kolme rakennetta, jotka käyttävät DICT-tietomuotoa: Top DICT, Font DICT ja Private DICT. Useita erikokoisia kokonaislukuoperandityyppejä on määritelty ja koodattu seuraavan taulukon mukaisesti (operandin ensimmäinen tavu on b0, toinen on b1 ja niin edelleen).

|Koko |b0-alue |Arvoalue |Arvon laskeminen|
---|---|---|---|
|1 |32 - 246| -107 - +107 |b0 - 139|
|2	|247 to 250|	+108 to +1131	|(b0 - 247) * 256 + b1 + 108|
|2	|251 to 254|	-1131 to -108|	-(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 - +32767| b1 << 8 | b2|
|5 |29| -(2^31) - +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Otsikko

Binääritiedot alkavat otsikolla, jonka muoto on alla olevassa taulukossa.

|Tyyppi |Nimi |Kuvaus|
---|---|---|
|uint8| pääversio| Muotoile pääversio. Aseta arvoon 2.|
|uint8| minorVersion| Muotoile sivuversio. Aseta nollaan.|
|uint8| headerSize| Otsikon koko (tavuina).|
|uint16| topDictLength| Top DICT -rakenteen pituus tavuina.|

## Viitteet

 * [CFF2-tiedostomuoto](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

