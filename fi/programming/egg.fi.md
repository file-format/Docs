{
  "date": "2022-03-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EGG-tiedostomuoto - Python-jakelutiedosto",
  "description": "Opi EGG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata EGG-tiedostoja.",
  "linktitle": "EGG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-eg-fig"
}
},
  "lastmod": "2022-03-15"
}

## Mikä on EGG-tiedosto?

EGG-tiedosto, joka tunnetaan myös nimellä Python munat, on vanhempi Python-jakelumuoto. Se on [ZIP](/compression/zip/)-pakattu arkisto, jonka laajennus on .egg ja joka sisältää Python-sovelluksen lähdetiedostot sekä jakelun metatiedot. EGG-tiedostot ovat vaihtoehto Windows Executable [EXE](/executable/exe/) -tiedostolle, mutta ne ovat monialustaisia. Tämä Python-jakelujen vanhempi muoto on korvattu uudemmalla Wheel (WHL) -tiedostomuodolla vuoden 2010 alussa.

## EGG tiedostomuoto

EGG-tiedostot tallennetaan pakattuna ZIP-arkistoon. Se tarkoittaa, että jos korvaat .egg-tunnisteen .zip-tunnisteella, voit avata sen tavallisilla purkuapuohjelmilla, kuten Corel WinZIP, Microsoft Explorer tai RARLAB WinRAR.

EGG-tiedostoja voidaan luoda Pythonin **distutils**-paketilla. Toinen työkalu, jolla voidaan luoda ja avata EGG-tiedostoja, on **SetupTools**. EGG-tiedostot voidaan asentaa pakettina käyttämällä **easy_install**-toimintoa.

`HUOM - EGG-tiedostomuoto on vanhentunut uuden WHL-pyörän tiedostomuodon hyväksi.`

## Viite ##

* [Python EGGs](https://python101.pythonlibrary.org/chapter38_eggs.html)


