{
  "date": "2021-08-29",
  "keywords": [
"ade",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Microsoft Access"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi ADE-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ADE-tiedostoja.",
  "title": "ADE - Käytä projektin laajennustiedostoa",
  "linktitle": "ADE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ad-fie"
}
},
  "lastmod": "2021-08-29"
}

## Mikä on ADE-tiedosto?

Tiedosto, jonka pääte on .ade, on Microsoft Access Project -tiedosto, joka sisältää Microsoft Access ADP -projektitiedoston sisältämien tietojen kootun tulosteen. Access-projektitiedoston tiedot, muut kuin Visual Basic for Applications (VBA), ovat saatavilla koottuna ADE-tiedostoina. Tiedot tallennetaan näihin tiedostoihin pakatussa muodossa tiedoston koon pienentämiseksi ja Accessin suorituskyvyn parantamiseksi. Koska ADE on Access-projektitiedoston käännetty tulos, kaikki projektiin kuuluva VBA-lähdekoodi pysyy suojattuna, koska se ei salli sen olla osa tulostetta. ADE-tiedostot voidaan avata Microsoft Access 365:ssä.

## ADE-tiedostomuoto - lisätietoja

ADE ovat koottuja Access Database -tiedostoja, jotka tallennetaan levylle binääritiedostoina. Näiden tiedostojen sisäistä tiedostorakennetta ei tunneta.

The ADE files can create issues in opening based on the version of Microsoft Access that has been used to create these files. Access databases that are using the 64-bit version of Microsoft Access 2010 and that are compiled as MDE, [ACCDE](/database/accde/), or ADE files have to be recompiled in Microsoft Access 2021 Service Pack 1 (SP1) to work correctly with Access 2010 SP1. Tämä ongelma ilmenee, koska Access 2010 SP1 käyttää VBE7.dll-tiedoston uudempaa versiota (versio 7.00.1619).

## Viitteet

* [Ongelma Access ADE -tiedostoissa](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)

* [Mitä käyttöoikeustiedostomuotoja käytetään](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)


