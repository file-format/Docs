{
  "date": "2021-06-21",
  "keywords": [
"UDL",
"laajennus",
"udl tiedosto",
"udl-tiedostomuoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"mikä on udl-tiedosto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi UDL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata UDL-tiedostoja.",
  "title": "UDL - Microsoft Universal Data Link File",
  "linktitle": "UDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ud-fil"
}
},
  "lastmod": "2021-06-21"
}

## Mikä on UDL-tiedosto?
Tiedostoa, jonka tunniste on .udl, kutsutaan Microsoft Universal Data Link -tiedostoksi. yhteysattribuuttien määrittäminen; Windows-sovellukset käyttävät yhteyden muodostamiseen tietokantaan. UDL-tiedosto sisältää OLE DB -tietolähteen yhteysmerkkijonon; käyttäjätunnuksella ja salasanalla sekä tärkeillä yhteysmerkkijono-ominaisuuksilla. Jotta vältetään ominaisuuksien määrittäminen suoraan käsin yhteysmerkkijonossa, voidaan vaihtoehtona käyttää Data Link Properties -valintaikkunaa yhteystietojen tallentamiseen .udl-tiedostoon.

## UDL tiedostomuoto
Pohjimmiltaan UDL (Universal Data Link) -tiedosto on yksinkertainen tekstitiedosto, joka koostuu tietokantayhteysmerkkijonosta, jolla on tiettyjä määritteitä tai ominaisuuksia. Kun UDL-tiedosto on luotu, sitä voidaan testata SQL Server Management Studion avulla varmistaaksesi yhteyden.

### Yhteysmerkkijonon ominaisuudet
Seuraavat ominaisuudet voidaan asettaa UDL:ään oikean yhteyden varmistamiseksi:

- **Palvelimen nimi**: sen palvelimen sijainti, jossa tietokanta, jota haluat käyttää, sijaitsee.
- **Todennusvaihtoehdot**
- **Windows-todennus**: Todennus SQL Serveriin käyttämällä tällä hetkellä kirjautuneen käyttäjän Windows-tilin tunnistetietoja.
- **SQL Server Authentication**: Todennus kirjautumistunnuksella ja salasanalla.
- **Active Directory - Integrated**: Integroitu todennus Azure Active Directory -identiteetillä; voidaan käyttää myös Windowsin todentamiseen SQL Serveriin.
- **Active Directory - Salasana**: Käyttäjätunnuksen ja salasanan todennus Azure Active Directory -identiteetillä.
- **Active Directory - universaali MFA-tuella**: Interaktiivinen todennus Azure Active Directory -identiteetillä.
- **Active Directory - Palvelupäällikkö**: Todennus Azure Active Directory -palvelun pääkäyttäjällä.
- **Palvelimen SPN**: Jos käytät luotettua yhteyttä, voit määrittää palvelimelle palvelun päänimen (SPN).
- **Käyttäjänimi**: Kirjoita todentamiseen käytettävä käyttäjätunnus, kun kirjaudut sisään tietolähteeseen.
- **Salasana**: Kirjoita todentamiseen käytettävä salasana, kun kirjaudut sisään tietolähteeseen.
- **Tyhjä salasana**: Kun tämä on valittuna, määritetty palveluntarjoaja voi käyttää tyhjää salasanaa yhteysmerkkijonossa.
- **Salli salasanan tallentaminen**: Sallii salasanan tallentamisen yhteysmerkkijonon kanssa.
- **Käytä vahvaa salausta**: yhteyden kautta välitettävät tiedot salataan.
- **Trust server certificate**: The server's certificate will be validated.
- **Tietokanta**: Tietokannan nimi, jota haluat käyttää.
- **Liitä tietokantatiedosto tietokannan nimeksi**: Määrittää liitettävän tietokannan ensisijaisen tiedoston nimen.

## Viitteet ##

* [Microsoft Data Access Components](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)

* [Universal Data Link (UDL) -määritys](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)


