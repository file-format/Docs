{
  "date": "2023-05-02",
  "keywords": [
"obi tiedosto",
"mikä on obi-tiedosto",
"mikä on obi-tiedoston muoto",
"tiedosto",
"obi tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "OBI-tiedostomuoto - Outlook RSS -tilaustiedosto",
  "description": "Opi OBI-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata OBI-tiedostoja.",
  "linktitle": "OBI",
  "menu": {
    "docs": {
      "identifier": "settings-obi-fi",
      "parent": "settings"
}
},
  "lastmod": "2023-05-02"
}

## Mikä on OBI-tiedosto?

OBI-tiedosto on Outlook RSS -tilaustiedosto, jonka avulla käyttäjät voivat tilata RSS-syötteen Microsoft Outlookissa. RSS on lyhenne sanoista Really Simple Syndication, joka on verkkosyötemuoto, jota käytetään usein päivitettävän sisällön, kuten blogitekstien, uutisotsikoiden tai podcastien, julkaisemiseen.

RSS-syötteen tilaamiseksi Outlookissa käyttäjät voivat napsauttaa RSS-syötteen linkkiä verkkosivustolla tai kopioida RSS-syötteen URL-osoitteen ja liittää sen Outlookin Lisää uusi RSS-syöte -valintaikkunaan. Outlook tarkistaa sitten säännöllisesti RSS-syötteen uuden sisällön varalta ja näyttää sen käyttäjän RSS-syötekansiossa.

Outlook RSS -tilaustiedostojen tiedostotunniste on .rss. Nämä tiedostot sisältävät RSS-syötteen URL-osoitteen, ja niitä voidaan käyttää RSS-syötetilausten jakamiseen muiden kanssa tai RSS-syötetilausten varmuuskopiointiin ja palauttamiseen.

## OBI-tiedostomuoto - lisätietoja

OBI-tiedostot tunnetaan nimellä OPML (Outline Processor Markup Language) -tiedosto, ja ne sisältävät luettelon RSS-syötteen URL-osoitteista, jotka on tilattu Microsoft Outlookissa.

Kun käyttäjä vie RSS-syötteensä OBI-tiedostoon, se sisältää luettelon kaikista tilaamistaan RSS-syötteistä, mukaan lukien kunkin syötteen otsikon, syötteen URL-osoitteen ja muut asiaankuuluvat tiedot. Näin käyttäjät voivat helposti siirtää RSS-syötetilauksensa toiseen RSS-lukijaan tai varmuuskopioida tilauksensa säilytystä varten.

OBI-tiedostoja voidaan käyttää myös RSS-syötetilausten tuomiseen Microsoft Outlookiin tai muuhun RSS-lukijaan. Tuodakseen OBI-tiedoston Outlookiin käyttäjät voivat napsauttaa Tiedosto > Avaa ja vie > Tuo/Vie > Tuo toisesta ohjelmasta tai tiedostosta > Seuraava > Tuo RSS-syötteitä OPML-tiedostosta ja Selaa sitten OBI-tiedoston sijaintiin tietokoneella.

## Mikä on OBI-tiedoston muoto?

Outlook RSS -tilaustiedosto, joka tunnetaan myös nimellä OBI-tiedosto, määrittää tiedoston rakenteen ja sisällön XML:n (eXtensible Markup Language) avulla.

OBI-tiedostot koostuvat sarjoista sisäkkäisistä elementeistä, joilla kullakin on oma attribuutti- ja arvosarjansa. OBI-tiedoston pääelementti on outline-elementti, joka sisältää tietoja RSS-syötteestä, mukaan lukien syötteen otsikko, syötteen URL-osoite ja muut asiaankuuluvat tiedot.

Jokainen ääriviiva-elementti voi sisältää myös alatason elementtejä, jotka edustavat RSS-syöteluettelon alikansioita tai alaluokkia. OBI-tiedoston rakenne mahdollistaa RSS-syötetilausten helpon organisoinnin ja hallinnan, ja sen avulla voidaan siirtää tilauksia eri RSS-lukijoiden välillä tai varmuuskopioida ja palauttaa tilauksia.

## Viitteet
* [Mitä RSS-syötteet ovat?](https://support.microsoft.com/en-us/office/what-are-rss-feeds-e8aaebc3-a0a7-40cd-9e10-88f9c1e74b97)


