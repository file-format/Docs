{
  "date": "2023-03-07",
  "keywords": [
"manifest-tiedosto",
"mikä on manifest-tiedosto",
"tiedosto",
"manifest-tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "MANIFEST-tiedostomuoto - Windows-sovellusluettelotiedosto",
  "description": "Opi MANIFEST-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata MANIFEST-tiedostoja.",
  "linktitle": "MANIFEST",
  "menu": {
    "docs": {
      "identifier": "system-manifest-fi",
      "parent": "system"
}
},
  "lastmod": "2023-03-07"
}

## Mikä on MANIFEST-tiedosto?

Luettelotiedosto on tiedosto, joka sisältää tietoja ohjelmistosovelluksesta tai -paketista. Tiedosto on yleensä nimetty .manifest-tiedostotunnisteella. Luettelotiedosto sisältää tietoja pakettiin sisältyvistä tiedostoista, niiden versionumeroista ja mahdollisista riippuvuuksista, joita paketilla on muihin ohjelmistokomponentteihin.

Manifest-tiedostoja käytetään yleisesti Windows-alustalla sen varmistamiseksi, että ohjelmistosovellukset on asennettu ja määritetty oikein. Niitä voidaan käyttää määrittämään asioita, kuten mitä versioita jaetuista kirjastoista tulee käyttää, mitkä asetustiedostot tulee sisällyttää ja mitä rekisteriavaimia tulee muokata asennuksen aikana.

Windowsin lisäksi luettelotiedostoja voidaan käyttää myös muissa yhteyksissä, kuten verkkosovelluksissa tai Android-sovelluksissa. Luettelotiedoston muoto ja sisältö riippuvat alustasta ja pakattavasta sovelluksesta.

## Lisää tietoa

Manifest-tiedostot ovat XML-muodossa. XML on laajalti käytetty merkintäkieli strukturoitujen asiakirjojen ja tietojen luomiseen, ja sitä käytetään usein ohjelmistokehityksessä konfiguraatioiden, asetusten ja muiden metatietojen kuvaamiseen.

Ohjelmistosovellusten yhteydessä manifesti XML-tiedosto sisältää yleensä tietoja sovelluksen riippuvuuksista, versiotiedoista ja muista kokoonpanoasetuksista. Tiedostoa käytetään varmistamaan, että sovellus on asennettu oikein ja että siinä on kaikki tarvittavat osat ja resurssit toimiakseen oikein.

Manifesti XML-tiedosto voidaan sisällyttää sovelluspakettiin tai erillisenä tiedostona, joka ladataan asennuksen aikana. Se on yleensä nimetty .manifest-tiedostotunnisteella, ja se noudattaa tiettyä muotoa, jonka määrittelee alusta tai kehys, johon sovellus on rakennettu.

Esimerkiksi Microsoft .NET Frameworkissa manifesti-XML-tiedostoa käytetään kuvaamaan sovelluksen riippuvuuksia ja versiotietoja, ja se sisältyy yleensä osana sovelluksen kokoonpanoa. Common Language Runtime (CLR) käyttää tiedostoa määrittääkseen ladattavien kokoonpanojen oikeat versiot ja varmistaakseen, että sovellus toimii oikein.

## Viitteet
* [Manifestitiedosto](https://en.wikipedia.org/wiki/Manifest_file)


