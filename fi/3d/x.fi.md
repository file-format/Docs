{
  "date": "2020-01-11",
  "keywords": [
"x tiedosto",
"x tiedostomuoto",
"mikä on x-tiedosto",
"tiedosto",
"x esimerkki",
"x tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "X - DirectX 2.0 -tiedostomuoto",
  "description": "Opi DirectX X -tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda DirectX X -tiedostoja.",
  "linktitle": "X",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d--fix"
}
},
  "lastmod": "2020-01-11"
}

## Mikä on X-tiedosto?

A file with .x extension refers to [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics legacy file format that was introduced with Microsoft DirectX 2.0. Sitä käytettiin pelien 3D-grafiikkaan renderöimiseen, ja se määrittää verkkojen, tekstuurien, animaatioiden ja käyttäjän määrittämien objektien rakenteet. Se on poistettu käytöstä vuodesta 2014 lähtien, koska Autodesk FBX -tiedostomuoto toimii paremmin nykyaikaisempana tiedostomuotona. X on mallipohjainen, eikä siinä ole mitään käyttötietoa.

Voit avata DirectX X -tiedostoja Microsoft DirectX:n ja yleisten tekstieditorien avulla.

## X tiedostomuoto

{{HYPERLINKKI}} sisältää viitetiedot API-elementeistä, joita käytetään DirectX .x -tiedostojen kanssa toimimiseen. Muoto tarjoaa matalan tason tietoprimitiivit, joita muut sovellukset käyttävät korkeamman tason primitiivien määrittämiseen tietomallien avulla. DirectX 6.0 esitteli käyttöliittymät ja menetelmät, jotka mahdollistavat .x-tiedostoista lukemisen ja niihin kirjoittamisen. DirectX 3.0 esitteli tämän tiedostomuodon binaariversion.

DirectX 9:n määrittelemä {{HYPERLINKKI}} sisältää viitetietoja .x-tiedostoista binäärimuodossa sekä tekstikoodauksissa.

### Binäärikoodaus

{{HYPERLINKKI}} määrittelee DirectX X -muodon tekstimuodon tokenoituna esityksenä. Nämä merkit voivat olla itsenäisiä antamaan kieliopillisen rakenteen tai ne voivat olla tietueita sisältäviä tokeneita, jotka toimittavat tarvittavat tiedot.

#### Otsikko

Binääriotsikko voidaan lukea ja kirjoittaa käyttämällä seuraavia määritelmiä.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Tekstin koodaus

DirectX .x -tiedostot eivät riipu tavasta, jolla tiedostoa käytetään, eivätkä ne liity mihinkään sovellukseen. Tämä mallipohjainen lähestymistapa mahdollistaa .x-tiedostomuodon käytön kaikissa asiakassovelluksissa.


#### Otsikko

Vaihtuvapituinen otsikko on pakollinen ja sen on oltava tietovirran alussa. Otsikko sisältää seuraavat tiedot.

|Tyyppi |Alatyyppi |Koko |Sisältö |Sisällön merkitys|
---|---|---|---|---|
|Maaginen numero (pakollinen)| | 4 tavua |xof |
|Versionumero (pakollinen) |Päänumero |2 tavua |03 |Pääversio 3|
| |Pieni numero |2 tavua |02 |Pieni versio 2|
|Muototyyppi (pakollinen)| |4 tavua |txt |Tekstitiedosto|
| | | |bin | Binääritiedosto|
| | | |tzip| MSZip pakattu tekstitiedosto|
| | | |bzip| MSZip pakattu binaaritiedosto|
|Kellukekoko (pakollinen)| |4 tavua| 0064| 64-bittinen float|
| | | |0032 |32-bittiset kelluvat|


## Viitteet

 * [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
 * [DirectX 9 -tiedostomuodon viite](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

