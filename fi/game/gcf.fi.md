{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Opi GCF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata GCF-tiedostoja.",
  "title" : "GCF-tiedosto - Nadeo Game GCF-muoto",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-fi",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## Mikä on GCF-tiedosto?

.gcf-tiedosto on Steam-pelialustan käyttämä pelin välimuistitiedosto. Se sisältää pelitietoja, kuten tekstuurit, mallit ja muut pelin käyttämät tiedostot. Nämä tiedostot tallennetaan käyttäjän tietokoneelle, ja niitä käytetään vähentämään ladattavan tiedon määrää pelin päivityksen tai asennuksen aikana. .gcf-tiedostoja voidaan käyttää myös varmuuskopioiden luomiseen pelin asennuksesta tai pelin siirtämiseen tietokoneiden välillä.

GCF-tiedostoja voi lukea ja kirjoittaa avoimen lähdekoodin C++-ohjelmointikirjasto, **HLLib**.

## GCF-tiedostomuoto

GCF-tiedostot tallennetaan levylle binääritiedostoina. GCF käytettiin alun perin lyhenteenä Grid Cache File -tiedostolle (Steamin varhainen koodinimi oli Grid), mutta myöhemmin se otettiin Game Cache File -tiedostoksi. GCF-tiedosto on arkistotiedosto, joka tallentaa Steam-pelejä. Kaikki virallinen sisältö ladataan GCF-tiedostoina. GCF-tiedostoja voidaan myös jakaa pelien välillä.

HUOMAA: GCF on {{HYPERLINKKI}}:n edeltäjä.
## Viitteet

* [Valve Software](https://www.valvesoftware.com/en/)

* [GCF-tiedostomuoto](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib – avoimen lähdekoodin C++-ohjelmointikirjasto GCF-tiedostojen lukemiseen](https://developer.valvesoftware.com/wiki/HLLib)


