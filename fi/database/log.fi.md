{
  "date": "2021-06-14",
  "keywords": [
"HIRSI",
"laajennus",
"loki tiedosto",
"lokitiedostomuoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"mikä on lokitiedosto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi LOG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LOG-tiedostoja.",
  "title": "LOG - lokitiedostomuoto",
  "linktitle": "LOG",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-lo-fig"
}
},
  "lastmod": "2021-06-14"
}

## Mikä on LOG-tiedosto?
Tiedosto, jonka pääte on .log, sisältää luettelon pelkkää tekstiä aikaleimalla. Yleensä ohjelmistot tai käyttöjärjestelmät kirjaavat tietyt toiminnan tiedot, jotta kehittäjät tai käyttäjät voivat seurata, mitä tietyllä ajanjaksolla tapahtui. Käyttäjät voivat muokata näitä tiedostoja erittäin helposti millä tahansa tekstieditorilla. Yleensä käyttöjärjestelmät kirjaavat virheraportit tai kirjautumistoiminnot, mutta myös muut ohjelmistot tai web-palvelimet luovat lokitiedostoja kävijöiden seuraamiseksi ja kaistanleveyden käytön seuraamiseksi.

## LOG-tiedostomuoto
LOG-tiedostomuoto tallentaa joko käyttöjärjestelmän tyypilliset tapahtumat, viestintäohjelmiston eri käyttäjien väliset viestit tai minkä tahansa muun ohjelmiston ajon. Yksinkertaisesti voidaan sanoa, että tietyt viestit tietyillä aikaleimoilla kirjataan LOG-tiedostoon. Jotkut yleisesti käytetyt kirjaamiseen käytetyt termit ovat:
### Tapahtumalokit
Se tallentaa järjestelmän suorituksessa tapahtuvat tapahtumat, jotta voidaan seurata ja ymmärtää järjestelmän toimintaa ja diagnosoida ongelmia. Ne ovat tärkeitä monimutkaisten järjestelmien toimintojen tunnistamisessa, tyypillisesti sovelluksissa, joissa on vain vähän käyttäjän vuorovaikutusta.
### Tapahtumalokit
Lähes kaikki tietokantajärjestelmät ylläpitävät tapahtumalokia, jota ei yleensä ole tarkoitettu myöhempää analysointia varten, eivätkä ne ole ihmisen luettavissa. Nämä lokit pitävät kirjaa vain olemassa olevien tietojen muutoksista, jotta tietokanta voi toipua kaatumisista tai muista tietovirheistä ja pitää tiedot johdonmukaisessa tilassa. Siksi tietokantajärjestelmissä on yleensä sekä yleiset tapahtumalokit että tapahtumalokit.
### Viestilokit
Internet Relay Chatin (IRC), pikaviestiohjelmien, keskustelutoiminnoilla varustettujen vertaistiedostojen jakamisohjelmien ja moninpelien (erityisesti MMORPG:iden) tallentamaa tekstiviestintää kutsutaan viestilokeiksi. Nämä lokit tallennetaan yleensä vain tekstitiedostoina, mutta pikaviesti- ja VoIP-asiakkaat (esim. Skype) saattavat tallentaa ne HTML-tiedostoihin lukemisen helpottamiseksi tai salauksen mahdollistamiseksi.
### Palvelimen lokit
Palvelinloki on itse asiassa lokitiedosto, joka sisältää luettelon toiminnoista, jotka palvelin itse suorittaa ja luo tai ylläpitää automaattisesti. Yleensä nämä tiedostot eivät ole yleisten Internetin käyttäjien saatavilla, vaan vain webmasterilla tai muulla Internet-palvelun ylläpitäjällä.



## Viitteet ##

* [Lokitiedosto - Wikipedia](https://en.wikipedia.org/wiki/Log_file)


