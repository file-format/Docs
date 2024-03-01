{
  "date": "2021-05-03",
  "keywords": [
"SDF",
"sdf-tiedosto",
"mikä on sdf-tiedosto",
"kuinka avata sdf-tiedosto",
"laajennus",
"tiedosto",
"sdf-tiedostomuoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Tietokantatiedostot"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi SDF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SDF-tiedostoja.",
  "title": "SDF - SQL Server Compact -tietokantatiedosto",
  "linktitle": "SDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sd-fif"
}
},
  "lastmod": "2021-05-03"
}

## Mikä on SDF-tiedosto?
Tiedosto, jonka laajennus on .sdf, sisältää Microsoft SQL Server Compact (SQL CE) -tietokannan, joka tunnetaan myös kompaktina relaatiotietokantana. Microsoftin tuottama mobiililaitteiden ja pöytätietokoneiden sovelluksiin. Se tukee sekä 32- että 64-bittistä käyttöjärjestelmää, ja koko tietokannan sisältö sisältyy yhteen SDF-tiedostoon ja se voi viedä yli 4 Gt levytilaa. Turvallisuussyistä .sdf-tiedosto voidaan salata 128-bittisellä salauksella. SQL CE:n ajonaika määrittää rinnakkaisen usean käyttäjän pääsyn .sdf-tiedostoon. SDF-tiedosto voidaan kopioida **QuickOncen** avulla tai yksinkertaisesti kopioida kohteeseen järjestelmän käyttöönottoa varten.

## SDF-tiedostomuoto
SDF-tiedosto sisältää tietokannan, jota yleensä kutsutaan kompaktiksi relaatiotietokannaksi. SDF-tiedosto sisältää kaikki tietokantaan liittyvät tiedot, ja SQL Server Compact on kevyt ja ilmainen tietokantamoottori, jota käytetään .sdf-tiedostojen hallintaan. .sdf-tiedoston koko ei saa ylittää 4 Gt:n kokorajoitusta. SDF-tiedostot eivät tallenna tietoja tallennetuista toimenpiteistä, laukaisimista tai näkymistä. SQL CE -tietokantaa käyttävien sovellusten ei tarvitse määrittää polkua SDF-tiedostoon ADO.NET-yhteysmerkkijonossa, vaan se voidaan mainita muodossa |DataDirectory|\database_name.sdf, joka määrittää sovelluksen kokoonpanoluettelossa määritetyn tietohakemiston.
.sdf-nimeämiskäytäntö on valinnainen, ja tiedoston tallentamiseen voidaan käyttää mitä tahansa tunnistetta. Tietokantatiedoston salasanan määrittäminen on valinnainen vaihe. Tietokannan pakkaamista tai korjaamista varten tiedosto tulee tallentaa valitsemalla **tiivistetty/korjattu tietokanta**.

## Viitteet

 * [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
 * [SQL Server Compactin käyttäminen ASP.NET-verkkosovelluksiin](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


