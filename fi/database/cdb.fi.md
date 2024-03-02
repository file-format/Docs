{
  "date": "2021-06-16",
  "keywords": [
"CDB",
"laajennus",
"cdb-tiedosto",
"cdb-tiedostomuoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"mikä on cdb-tiedosto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi CDB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CDB-tiedostoja.",
  "title": "CDB - jatkuva tietokantatiedosto",
  "linktitle": "CDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-cd-fib"
}
},
  "lastmod": "2021-06-16"
}

## Mikä on CDB-tiedosto?
CDB-tiedostoja käytetään kriittisissä sovelluksissa, kuten sähköpostissa. CDB on lyhenne sanoista jatkuva tietokanta, nopea, luotettava ja yksinkertainen paketti vakiotietokantojen luomiseen tai lukemiseen. Tietokannan korvaaminen on turvallista järjestelmän kaatumisilta. Käyttäjien ei tarvitse pysähtyä uudelleenkirjoituksen aikana. CDB toimii assosiatiivisena taulukkona (levyllä), yhdistää avaimet arvoihin ja mahdollistaa useiden arvojen tallentamisen yhteen avaimeen.

## CDB tiedostomuoto

CDB-tiedostomuoto tallentaa numerot, siirtymät, pituudet ja hash-arvot little endian -muodossa etumerkittöminä 32-bittisinä kokonaislukuina. Avainten ja tietojen uskotaan olevan läpinäkymättömiä tavujonoja, joita ei ole käsitelty. Tietokannan alussa kiinteän kokoinen otsikko edustaa 256 hash-taulukkoa listaamalla niiden sijainnin tiedostossa ja pituuden paikoissa. Yleensä tiedot tallennetaan tietueiden sarjana, jokainen tietue tallentaa avaimen pituuden, datan pituuden, avaimen ja tiedot. Lajittelu- tai kohdistussääntöjä ei ole. Tietueita seuraa joukko 256 eripituista hash-taulukkoa. Koska nolla on kelvollinen pituus, tietokantaan voi fyysisesti olla tallennettuna vähemmän kuin 256 hash-taulukkoa, mutta mitään ei pidetä 256 taulukona. Hash-taulukot koostuvat sarjasta aikaväliä, joista jokainen sisältää hajautusarvon ja tietuepoikkeaman. Tyhjien paikkojen siirtymä on nolla.

### CDB-tiedostomuodon rakenne

CDB-tietokanta koostuu kokonaisesta tietojoukosta yhdessä tietokonetiedostossa. Se sisältää kolme osaa:
- Kiinteän kokoinen otsikko
- Dataa
- Sarja hash-taulukoita.

Hakuja on saatavilla vain tarkalle avaimelle. Haut toimivat seuraavan algoritmin mukaan:

- Hash avain.
- Määritä, mihin hash-taulukkoon ja -paikkaan tämä tietue tulisi sijoittaa.
- Testaa ilmoitettua paikkaa hash-taulukossa.

Jos haetaan avaimia, joissa on useampi kuin yksi arvo, lisäarvoja voidaan löytää yksinkertaisesti jatkamalla hakua seuraavasta paikasta.

#### Ominaisuudet

CDB-tietokantarakenne tarjoaa useita ominaisuuksia:

##### Nopeat haut
Onnistunut haku valtavasta tietokannasta kestää tavallisesti vain kaksi levykäyttöä ja epäonnistunut haku vain yhden.
##### Matalat yleiskustannukset
Tietokanta käyttää 2048 tavua, 24 tavua per tietue ja tilaa avaimille ja tiedoille.
##### Ei satunnaisia rajoja
CDB voi hallita mitä tahansa tietokantaa jopa 4 gigatavuun asti. Koska muita rajoituksia ei ole, tietueiden ei tarvitse edes mahtua muistiin. Tietokannat on tallennettu koneriippumattomaan muotoon.
##### Nopea atomitietokannan vaihto
Komento **cdbmake** voi kirjoittaa koko tietokannan uudelleen kahteen suuruusluokkaan, nopeammin kuin muut hajautuspaketit.
##### Nopeat tietokantavedokset
**cdbdump** voi tulostaa tietokannan sisällön cdbmake-yhteensopivassa muodossa.


## Viitteet ##

* [cdb (software) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [CDB-määritys](http://cr.yp.to/cdb.html)
