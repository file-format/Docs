{
  "date": "2022-06-24",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SY_-tiedostomuoto - pakattu SYS-tiedosto",
  "description": "Opi SY_-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SY_-tiedostoja.",
  "linktitle": "SY_",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-sy-fi_"
}
},
  "lastmod": "2022-06-24"
}

## Mikä on SY_-tiedosto?

SY_-tiedosto on pakattu .sys-tiedosto, jota ohjelmiston asentajat käyttävät pienentämään asennusohjelman sisällä olevien asennustiedostojen kokoa. Tämä pienentää asentajan kokonaiskokoa. SY_-tiedostoja voidaan laajentaa käyttämällä Microsoft Expand -komentorivityökalua, joka laajentaa yhden tai useamman pakatun tiedoston.

## SY_ tiedostomuoto - lisätietoja

SY_-tiedostot tallennetaan levylle pakattuina binääritiedostoina. Niiden sisäinen tiedostomuoto ei kuitenkaan ole saatavilla julkisesti. Microsoft Expand -komentoriviapuohjelma voi laajentaa SY_-tiedostoja jollakin seuraavista komentoriveistä.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Laajennettaessa SY_-tiedostot muunnetaan [SYS](/system/sys/)-tiedostoksi.

SY_-tiedostot ovat samanlaisia kuin EX_- ja DL_-tiedostot.

## Viitteet

 * [StuffIt - Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
 * [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

