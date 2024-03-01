{
  "date": "2020-08-20",
  "keywords": [
"cff-tiedosto",
"cff-tiedostomuoto",
"mikä on cff-tiedosto",
"tiedosto",
"cff esimerkki",
"cff tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF - Kompakti fonttitiedostomuoto",
  "description": "Opi CFF-tiedostomuodosta ja sovellusliittymistä CFF-tiedostojen luomiseen ja avaamiseen.",
  "linktitle": "CFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cf-fif"
}
},
  "lastmod": "2020-10-21"
}

## Mikä on CFF-tiedosto?

Tiedosto, jonka laajennus on .cff, on kompakti fonttimuoto, ja se tunnetaan myös nimellä PostScript Type 1 tai CIDFont. CFF toimii säilönä useiden fonttien tallentamiseen yhteen yksikköön, joka tunnetaan nimellä FontSet. CFF-fonttien suunnittelu mahdollistaa PostScript-kielikoodin upottamisen, mikä mahdollistaa muodon lisää joustavuutta ja laajennettavuutta käytettäväksi tulostinympäristöissä. CFF-fonttitiedostoja voidaan avata ja muuntaa API:illa, kuten [Aspose.Font](https://products.aspose.com/font).

## CFF-tiedostomuoto

CFF-tiedostot ovat binääritiedostoja, jotka sisältävät strukturoidun tietoasettelun, joissa on määritellyt tietotyypit, otsikko, kuvioorganisaatio ja taulukkosanakirjat. Lisätietoja näistä löytyy osoitteesta [compact font format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff).

### Tietojen asettelu
CFF-tiedostomuodon tietojen asettelu on seuraavanlainen.

|Syöttö|Kommentit|
---|---|
|Otsikko|–|
|NimiINDEX|–|
|Suosituin DICT-HAKEMISTO|–|
|merkkijono INDEKSI|–|
|Global Subr INDEKSI|–|
|Koodaukset–Merkit|–|
|FDSelect|Vain CIDFonts|
|CharStrings INDEX|per-fontti|
|Fontti DICT INDEX|fonttikohtaisesti, vain CIDFonts|
|Yksityinen DICT|fonttikohtaisesti|
|Paikallinen alahakemisto INDEKSI|fontti- tai yksityinen DICT CIDFontsille|
|Tekijänoikeus- ja tavaramerkkiilmoitukset|–|

### Tietotyypit

CFF-tietotyypit ovat seuraavan taulukon mukaiset.

|Nimi|Alue|Kuvaus|
---|---|---|
|Kortti8|0 –255|1-tavuinen allekirjoittamaton numero|
|Kortti16|0 – 65535|2-tavuinen allekirjoittamaton numero|
|Offset|vaihtelee|1, 2, 3 tai 4 tavun offset (määritetty OffSize-kentässä)|
|OffSize|1–4|1-tavuinen etumerkitön luku määrittää Offset-kentän tai kenttien koon|
|SID|0 – 64999|2-tavuinen merkkijonotunniste|

### Otsikko

Binääridata alkaa otsikolla, jonka muoto on seuraavassa taulukossa.

|Tyyppi|Nimi|Kuvaus|
---|---|---|
|Card8|major|Alusta pääversio (alkaen numerosta 1)|
|Card8|minor|Alusta sivuversio (alkaen 0:sta)|
|Kortti8|hdrSize| Otsikon koko (tavuina)|
|OffSize|offSize|Absoluuttinen offset (0) koko|

## Viitteet

 * [Compact Font Format Table](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
 * [CFF-tiedostomuoto](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
 * [CFF2-kaavio](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

