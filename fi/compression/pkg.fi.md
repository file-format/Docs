{
  "date": "2021-04-08",
  "keywords": [
"pkg tiedosto",
"pkg tiedostomuoto",
"mikä on pkg-tiedosto",
"tiedosto",
"pkg esimerkki",
"pkg tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PKG - laajennettavissa oleva arkistotiedostomuoto",
  "description": "Opi PKG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PKG-tiedostoja.",
  "linktitle": "PKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pk-fig"
}
},
  "lastmod": "2021-04-13"
}

## Mikä on PKG-tiedosto?

Tiedosto, jonka laajennus on .pkg, on asennuspakettitiedosto, jota käytetään ohjelmiston asentamiseen macOS:ään. Macintosh-tietokoneiden lisäksi sitä käytetään myös iPhonessa. Sisäänrakennettua Applen asennusohjelmaa voidaan käyttää PKG-tiedoston sisällön asentamiseen. PKG-tiedosto on samanlainen kuin MSI-tiedosto, jota käytetään Windows-käyttöjärjestelmässä ohjelmiston asentamiseen. Asennuksen aikana nämä pakettitiedostot voivat kirjata viestejä, jotka antavat sinulle käsityksen siitä, mitä ylimääräisiä asioita tämä paketti asentaa.

## PKG tiedostomuoto

PKR ovat binääritiedostoja, jotka on pakattu tiedoston kokonaiskoon pienentämiseksi. OSX 10.5:stä lähtien Apple on ottanut käyttöön litteitä paketteja, joissa on yksi asennustiedosto. Nämä ovat erilaisia kuin aiemmat pakkausmuodot, jotka toimitettiin nippuina yksittäisten tiedostojen sijaan. Nämä niputetut paketit sisälsivät jäsennellyn hakemistohierarkian, joka tallensi tiedostot tavalla, joka helpottaa niiden hakemista jonkin hakemistotiedoston kautta. Litteä PKG-tiedostomuoto on itse asiassa {{HYPERLINKKI}}-arkisto, jossa on:

 * Otsikko – Määrittää koon, tarkistussumman ja versiotiedot
 * Sisällysluettelo - XML-dokumentti, joka on (ja täytyy) olla koodattu UTF-8-koodauksella ja joka on tallennettu tiedoston alkuun, mikä helpottaa arkiston skannaamista yksittäisen tiedoston purkamiseksi
 * Keko – TOC:n viittaama jäsentämätön tietokasa

## Viitteet

* [Flat Package File Format](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)

* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)


