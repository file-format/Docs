{
  "date": "2022-07-14",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "INC-tiedostotunniste - mikä on INC-tiedosto?",
  "description": "Lisätietoja INC:stä Sisällytä tiedostomuoto ja API:t, jotka voivat luoda ja avata INC-tiedostoja.",
  "linktitle": "INC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-in-fic"
}
},
  "lastmod": "2022-07-14"
}

## Mikä on INC-tiedosto?

INC-tiedosto on sisällyttävä tiedosto, jota ohjelmiston lähdekoodi käyttää otsikkotietoihin viittaamiseen. Se on samanlainen kuin {{HYPERLINKKI}} ja sisältää määrityksiä, toimintoja, otsikoita tai makroja, joita lähdekooditiedostot, kuten C++, voivat käyttää uudelleen. INC-tiedostoja käyttävät useat ohjelmointikielet, kuten C, [C++](/programming/cpp/), Pascal, [PHP](/programming/php/) ja [Java](/programming/java/). INC-tiedostojen avaamiseen voidaan käyttää tekstieditoreja, kuten Microsoft Notepad, Notepad++ ja TextEdit.

## INC-tiedostomuoto - lisätietoja

INC-tiedosto tallennetaan pelkkänä tekstitiedostona, joka sisältää kaikki ilmoitukset ilmoitussyntaksin mukaisesti. Yksi INC-tiedosto voi viitata myös muihin INC-tiedostoihin. Kun INC-tiedosto on luotu, siitä tulee osa projektia, ja siihen voidaan viitata lähdetiedostoista, kuten C++. Useat lähdetiedostot voivat viitata siihen päällekkäisyyden välttämiseksi.

## INC-tiedoston sisältö

INC-tiedostot voivat sisältää seuraavat tiedot.

**`Muuttujat`** – Object Oriented Programming (OOP) -ohjelmoinnin tapauksessa luokan otsikkotiedosto sisältää määritelmät kaikista luokkatason muuttujista, jotka ovat käytettävissä toteutuksen lähdekooditiedostoissa.

**`Methode Declaration`** - Kaikki menetelmäilmoitukset sisältyvät .h-otsikkotiedostoihin, jotta niitä voidaan käyttää useissa toteutustiedostoissa.

**`Non-inline Function Definitions`** - Otsikkotiedostot voivat sisältää myös ei-inline-menetelmien määritelmiä.

## INC-tiedoston käytön haittapuoli PHP:ssä

PHP ovat palvelinpuolen komentosarjoja, jotka toimivat palvelimella ja palauttavat tulokset kutsuville verkkosivuille. Jos PHP-tiedosto viittaa INC-tiedostoon ja palvelinta ei ole määritetty jäsentämään .inc-tiedostoja (mikä on hyvin yleistä), käyttäjä voi tarkastella .inc-tiedoston php-lähdekoodia käymällä URL-hakemistossa. Joten sinun on oltava varovainen käytettäessä INC-tiedostoja PHP:n sisällyttämistiedostoina.

## Viitteet

* [INC:n käyttäminen PHP:ssä](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)


