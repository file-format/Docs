{
  "date": "2022-04-01",
  "keywords": [
"nkit tiedosto",
"nkit tiedostomuoto",
"mikä on nkit-tiedosto",
"tiedosto",
"nkit esimerkki",
"nkit tiedostopääte",
"laajennus",
"muoto",
"nkit-alatunniste",
"nkit-tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi NKIT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata NKIT-tiedostoja.",
  "title": "NKIT - Levykuvatiedostomuoto",
  "linktitle": "NKIT",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nki-fit"
}
},
  "lastmod": "2022-04-01"
}

## Mikä on NKIT-tiedosto?

NKIT-tiedosto on levykuva NintendoWii- ja GameCube-peleistä poimitusta tiedosta. NKIT on Nintendo Toolkit -formaatille. Tuloksena oleva pakkaustiedosto [ISO](/compression/iso/) käyttää näiden pelien päätietoja ajettavaksi emulaattoriohjelmilla, kuten Dolphin, Swiss ja Nintendont. NKit tulee raaka- (iso) ja pakatuissa (gcz) tiedostomuodoissa, jotka molemmat on suunniteltu pitämään näkyvyyden toistettavuus ja koko.

## NKIT tiedostomuoto

NKit-tiedostomuoto on häviötön muoto, ja sitä käytetään Nintendo Wii- ja GameCube-kuvien pienentämiseen ja palauttamiseen. Muodot ovat saatavilla ISO- ja GCZ-tiedostomuodoissa jokaiselle GameCube- ja Wii-pelille.

|Järjestelmä |Muoto |Laitteistotuettu |Dolphin-tuettu |Palautettava 1:1 |Huomautuksia|
---|---|---|---|---|---|
|GameCube| nkit.iso| Kyllä |Kyllä| Kyllä |Sama kuin tiivistetty GameCube iso|
|GameCube| nkit.gcz| Ei| Kyllä| Kyllä |GCZ on Dolphinin oma lohkohakuinen pakkausmuoto|
|Wii| nkit.iso| Ei Kyllä| Kyllä| RVT-H-muoto, jota voi toistaa vain Dolphinissa|
|Wii| nkit.gcz| Ei Kyllä| Kyllä| GCZ:n RVT-H toistettava vain Dolphinissa|

### NKIT-otsikko

NKIT-tiedostomuodon otsikko on seuraava.

|Siirtymä |Pituus |Nimi|
---|---|---|
|0x200 |0x4 |NKit-otsikko 'NKIT'|
|0x204 |0x4 |NKit-versio ' v01'|
|0x208 |0x4 |Lähdekuva alkuperäinen CRC32|
|0x20C |0x4 |NKit CRC - tekee NKit-tiedostosta CRC32 yhtä suuren kuin lähde-CRC kohdassa 0x208 (0x4 GCZ:ssa)|
|0x210 |0x4 |Lähdekuvan pituus|
|0x214 |0x4 |Pakotettu roskapostitunnus (kun levytunnus eroaa – harvinainen – vain GameCube)|
|0x218 |0x4 |Wii Päivitä osio CRC32, jos se poistetaan muunnettaessa|

## Viitteet ##

* [NKIT-tiedostomuoto - tekijä gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)


