{
  "date": "2022-05-08",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GDB-tiedostomuoto - ESRI-tiedoston geotietokantatiedosto",
  "description": "Opi GDB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata GDB-tiedostoja.",
  "linktitle": "GDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-gd-fib"
}
},
  "lastmod": "2022-05-08"
}

## Mikä on GDB-tiedosto?

ESRI-tiedoston geotietokanta (FileGDB) on kokoelma levyllä olevassa kansiossa olevia tiedostoja, jotka sisältävät aiheeseen liittyviä geospatiaalisia tietoja, kuten ominaisuustietojoukkoja, ominaisuusluokkia ja niihin liittyviä taulukoita. Se edellyttää tiettyjen muiden tiedostojen säilyttämistä .gdb-tiedoston rinnalla samassa hakemistossa, jotta se toimisi. Kyselyjä voidaan suorittaa .gdb-tiedostossa sekä paikkatietojen että ei-tilatietojen hallitsemiseksi.

## GDB-tiedostomuoto - lisätietoja

Tiedoston geotietokannat koostuvat seitsemästä järjestelmätaulukosta sekä käyttäjätiedoista. Käyttäjätiedot voidaan tallentaa seuraavan tyyppisiin tietojoukkoihin:

* Ominaisuusluokka

* Ominaisuustietojoukko

* Mosaiikkitietojoukko

* Raster luettelo

* Rasteritietojoukko

* Kaavamainen tietojoukko

* Taulukko (ei-spatiaalinen)

* Työkalulaatikot


Ominaisuustietojoukot voivat sisältää ominaisuusluokkia sekä seuraavan tyyppisiä tietojoukkoja:

* Liitteet

* Ominaisuuksiin linkitetty huomautus

* Geometriset verkot

* Verkkotietojoukot

* Pakettikankaat

* Suhdekurssit

* Maastot

* Topologiat


Tietojen oletusarvoinen enimmäiskoko tiedostogeotietokantoissa on 1 TB. Suurin tietojoukkojen (yleensä rasteri) enimmäiskoko voidaan nostaa 256 Tt:aan. Tätä ohjaa määritysavainsana. Katso lisätietoja kohdasta Tiedoston geotietokantojen määritysavainsanat.

Tiedoston geotietokannat voivat sisältää myös alatyyppejä ja verkkotunnuksia ja osallistua kassa-/sisäänkirjautumisreplikaatioihin ja yksisuuntaisiin replikoihin.

Tiedoston geotietokantaa voivat käyttää samanaikaisesti useat käyttäjät. Jos käyttäjät muokkaavat, heidän on muokattava erilaisia tietojoukkoja.

## GDB-tiedostomuodon tekniset tiedot ##

GDB-tiedosto on ESRI:n oma muoto ja sen tekniset tiedot eivät ole saatavilla julkisesti. Tästä syystä tiedoston GDB tiedostomuodon tietoja ei voitu dokumentoida muualle kuin joihinkin lähteisiin, jotka ovat tehneet sen [partially](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) käänteistekniikalla.

## Viitteet ##

* [FGDB:n tiedot](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)


