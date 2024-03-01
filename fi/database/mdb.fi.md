{
  "date": "2020-11-11",
  "keywords": [
"MDB",
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
  "description": "Opi MDB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MDB-tiedostoja.",
  "title": "MDB-tiedostomuoto - Microsoft Access -tietokantatiedosto",
  "linktitle": "MDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-fib"
}
},
  "lastmod": "2020-11-11"
}

## Mikä on MDB-tiedosto?

A file with .mdb extension is a Microsoft Access database file which is a Relational Database Management System (RDBMS). It stores data in database tables that are linked to each other via primary and foreign keys. The MDB file contains complete structure of the database tables, queries, stored procedures. MDB is the default file format for Microsoft Access 2003. Microsoft Accessin sivuversiot käyttävät [ACCDB](/database/accdb/)-tiedostomuotoa, joka on tähän mennessä uusin tiedostomuoto. MDB-tiedostoja voidaan avata sovelluksilla, kuten Microsoft Access, MDB Viewer, MDBOpener, ja ne voidaan muuntaa ACCDB-, [CSV](/spreadsheet/csv/)-, Excel-muotoihin jne.

## MDB tiedostomuoto

There are public specifications available for MDB format and it remains Microsoft's proprietary file format. Microsoft, however, provides connectivity access to the MDB file using Open Database Connectivity (ODBC) standard and Visual Basic for Applications (VBA). The unofficial MDB guide provides brief informal description of the MDB format based on the reverse engineering and can be consulted for knowing about the specifications.

### Sivut

Epävirallisen MDB-oppaan mukaan MDB-tiedosto koostuu kiinteän kokoisista sivuista (2048 tavua Jeb DB3:lle ja 4096 tavua Jet DB 4:lle). Ensimmäinen tavu ilmaisee sivun tyypin. Seuraavat ovat tärkeimmät sivutyypit:

`Ensimmäinen sivu:` Se sisältää tietokannan otsikkotiedot, jotka sisältävät myös sen Jet DB -version tunnisteen, jonka kanssa tiedosto on yhteensopiva. Lisäksi se sisältää myös tiedostojen suojaustiedot ja kartan sivun käytöstä.

Taulukon määrityssivu: Taulukon määrityssivu määrittää sarakkeet, tietotyypit, hakemiston ja muut tiedot. Se käyttää tarvittaessa lisäsivuja ja sisältää sivukartan, joka sisältää tämän taulukon rivitiedot.

`Datasivut:` Tietosivut ovat varsinaisia tietosäiliöitä, joihin tiedot tallennetaan riveittäin. Se käyttää sivusivuja pitkien data-arvojen tallentamiseen.

Yksi Microsoft Access -tietokanta voi sisältää useita tiedostoja, jotka ylittävät tiedosto- ja taulukkokokorajoitukset. Tämä helpottaa lomakkeiden ja koodin sijoittamista käyttöliittymän MDB-tiedostoon käyttäjän työpöydälle ja tietojen sijoittamista muihin MDB-taustatiedostoihin verkkoon yhdistetyillä palvelimilla.

## Viitteet ##

* [Käyttöoikeustiedot](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [Epävirallinen MDB-opas](http://jabakobob.net/mdb/)


