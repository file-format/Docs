{
  "date": "2020-11-11",
  "keywords": [
"DDL",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Tietokantatiedostot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi DDL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DDL-tiedostoja.",
  "title": "DDL-tiedostomuoto - Data Definition Language -tiedosto",
  "linktitle": "DDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dd-fil"
}
},
  "lastmod": "2020-11-11"
}

## Mikä on DDL-tiedosto?

Tiedosto, jonka tunniste on .ddl, on Data Definition Language -tiedosto, jota käytetään tietokannan skeeman määrittämiseen. Se sisältää käskyjä/komentoja tietokantarakenteiden, kuten taulukoiden, sarakkeiden, tietueiden ja muiden kenttien, kanssa työskentelemiseen. DDL-tiedoston komennot on kirjoitettu kielellä [SQL](/database/sql/), ja ne voivat suorittaa toimintoja, kuten luoda taulukon tietokantaan, pudottaa ja päivittää. Tietokantaskeeman omistaa sen luotu ja kaikki CRUD-toiminnot voidaan suorittaa sille. Suosittuja sovelluksia, jotka voivat luoda ja avata DDL-tiedostoja, ovat Windows Text Editor, Jetbrains Intellij Idea ja EclipseLink.

## DDL-komennot

Yksittäinen DDL-tiedosto voi sisältää useita komentoja, jotka oikean syntaksin vuoksi suorittavat peräkkäin ja tekevät muutoksia skeemaan, kuten luovat merkistöjä ja taulukoita, pudottavat taulukoita, nimeävät uudelleen ja muuttavat taulukoita. Seuraavia DDL-komentoja käytetään yleisesti tietokantaskeeman kanssa työskennellessä.

`CREATE` - Käytetään luomaan tietokanta tai sen objektit (kuten taulukko, indeksi, funktio, näkymät, tallennusmenettely ja triggerit).

DROP' – Käytetään objektien poistamiseen tietokannasta.

`ALTER` - Käytetään muuttamaan tietokannan rakennetta.

TRUNCATE – Käytetään poistamaan kaikki tietueet taulukosta, mukaan lukien kaikki tietueille varatut tilat poistetaan.

`COMMENT` – Lisää kommentteja tietosanakirjaan.

`RENAME` – Nimeää uudelleen olemassa olevan objektin tietokannassa.

## DDL esimerkki

Seuraava esimerkki näyttää CREATE-komennon DDL-käskyn, joka luo taulukon ja määrittelee sen kentät.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Viitteet ##

* [Wikipedian DDL](https://en.wikipedia.org/wiki/Data_definition_language)


