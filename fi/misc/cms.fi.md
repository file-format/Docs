{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CMS-tiedostomuoto - Connection Manager -palvelun profiilitiedosto",
  "description":"Lisätietoja CMS-tiedostoista ja sovellusliittymistä, jotka voivat luoda ja avata CMS-tiedostoja.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms-fi",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Mikä on CMS-tiedosto?

CMS-tiedosto on datatiedosto, joka sisältää Microsoft Windows Connection Managerin käyttämät profiilitiedot. Sen avulla etäkäyttäjät voivat muodostaa yhteyden verkkoon näiden profiilitietojen avulla. CMS-tiedostoon tallennetut tiedot sisältävät tietoja käyttäjän käyttöjärjestelmästä ja käyttöoikeuksista, joita käytetään yhteyden muodostamiseen etäkäyttäjän ja verkon välille. CMS-järjestelmänvalvojat käyttävät Connection Manager Administrator Kit (CMAK) -pakettia CMS-tiedostojen luomiseen.

## CMS-tiedostomuoto – lisätietoja

CMS-tiedostoja ei yleensä löydy käyttäjien koneilta. Koska näitä käytetään erityisesti sallimaan etäkäyttäjät verkkoon, löydät ne tietokoneista, joita käytetään yhteyden muodostamiseen yrityksen verkkoon tai johonkin tiettyyn tarkoitukseen rakennettavaan toimistoon. Useimmissa tapauksissa sitä käytetään yhteyden muodostamiseen organisaation verkkoon, kuten Virtual Private Network (VPN), joka on omistettu vain yritykselle. Koska olet verkonvalvoja, määrität pääsyn tällaiseen verkkoon Connection Managerin avulla, jotta hän voi käyttää yrityksen verkkoa etäpaikasta.

### Mikä insdie CMS on?

CMS-profiilitiedosto luodaan Connection Managerilla ja pakataan muiden asetustiedostojen kanssa ennen kuin se toimitetaan etäkäyttäjälle. Nämä lisätiedostot voivat sisältää CMP- ja ja INF-tiedoston, jotka on pakattu rinnalle [EXE](/executable/exe/)-tiedostoon. Tämä täydellinen paketti toimitetaan etäkäyttäjälle verkkoon yhdistämistä varten.

## Viitteet

* [Windows Connection Managerin ymmärtäminen ja määrittäminen](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)


