{
  "date": "2019-12-12",
  "keywords": [
"KF8",
"laajennus",
"tiedosto",
"muoto",
"e-kirja",
"Kindle File Format",
"AZW3 tiedostorakenne"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi AZW3-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata AZW3-tiedostoja.",
  "title": "Mikä on AZW3-tiedosto?",
  "linktitle": "AZW3",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-azw-fi3"
}
},
  "lastmod": "2021-06-04"
}

## Mikä on AZW3-tiedosto?

AZW3, joka tunnetaan myös nimellä Kindle Format 8 (**KF8**), on Amazon Kindle -laitteille kehitetyn [AZW](/ebook/azw/) e-kirjan digitaalisen tiedostomuodon muokattu versio. Muoto on parannus vanhoihin AZW-tiedostoihin, ja sitä käytetään Kindle Fire -laitteissa vain taaksepäin yhteensopivilla esivanhempien tiedostomuodoilla eli [MOBI](/ebook/mobi/) ja AZW. Amazon esitteli KFX-muodon (KF-versio 10) KF8:n jälkeen, jota käytetään uusimmissa Kindle-laitteissa. AZW3-tiedostoilla on Internet-mediatyyppi application/vnd.amazon.mobi8-ebook. AZW3-tiedostot voidaan muuntaa useisiin muihin tiedostomuotoihin, kuten [PDF](/pdf/), [EPUB](/ebook/epub/), [AZW](/ebook/azw/), [DOCX](/word-processing/docx/) ja [RTF](/word-processing/rtf/).

## AZ3/KF8 tiedostomuoto ##

KF8-tiedostot ovat luonteeltaan binaarisia ja säilyttävät MOBI-tiedostomuodon rakenteen PDB-tiedostona. Kuten aiemmin mainittiin, KF8-tiedosto voi koostua sekä MOBI:sta että uudemmasta EPUB:n KF8-versiosta myöhemmin. Muodon sisäiset tiedot on purettu {{HYPERLINKKI}}:lla, joka on Python-skripti, joka jäsentää lopullisen käännetyn tietokannan ja poimii siitä MOBI- tai AZW-lähdetiedostoja. AZW3 (KF8) -tiedostot kohdistuvat EPUB3-versioon, jossa on myös taaksepäin yhteensopivuus EPUB:n kanssa. KF8 kokoaa EPUB-tiedostot ja luo binäärirakenteen, joka perustuu PDB-tiedostomuotoon.

## Viitteet ##

* [KF8 - Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)

* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)


