{
  "date": "2020-11-11",
  "keywords": [
"MDF",
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
  "description": "Opi MDF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MDF-tiedostoja.",
  "title": "MDF-tiedostomuoto - SQL Server -päätietokantatiedosto",
  "linktitle": "MDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-fif"
}
},
  "lastmod": "2020-08-12"
}

## Mikä on MDF-tiedosto?

Mdf-päätteinen tiedosto on perustietokantatiedosto, jota [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) käyttää käyttäjätietojen tallentamiseen. Se on ensiarvoisen tärkeää, koska kaikki tiedot on tallennettu tähän tiedostoon. MDF-tiedosto tallentaa käyttäjien tiedot relaatiotietokantoihin lomakkeen sarakkeissa, riveissä, kentissä, hakemistoissa, näkymissä ja taulukoissa. SQL Server mahdollistaa automaattisen kasvun ja automaattisen kutistuksen asetusten määrittämisen, jotta niillä on myönteinen vaikutus tietokannan suorituskykyyn. MDF-tiedostoja voidaan ladata ja liittää tietokantaan Microsoft SQL Serverin avulla. MDF-tiedostoilla on Application/octett-stream mime-tyyppi.

## MDF-tiedostomuoto

SQL Serverin tietojen tallennuksen perusyksikkö on sivu. Tietokannan muistisivu on jaettu loogisiin sivuihin, joiden numerointi on 0 - n. Yksi sivu alkaa 96-tavuisella otsikolla, joka koostuu sivun tunnuksesta, sivun rakenteen tyypistä, sivulla olevien tietueiden määrästä sekä osoittimista edelliselle ja seuraavalle sivulle.

### Tiedostorakenne

MDF-tiedostolla on seuraava tietorakenne.

 * Sivu 0: Otsikko
 * Sivu 1: Ensimmäinen PFS
 * Sivu 2: Ensimmäinen GAM
 * Sivu 3: Ensimmäinen SGAM
 * Sivu 4: Käyttämätön
 * Sivu 5: Käyttämätön
 * Sivu 6: Ensimmäinen DCM
 * Sivu 7: Ensimmäinen BCM

#### Tiedoston otsikko

Kaikkien tiedostojen sivunumero 0 sisältää otsikon, joka tallentaa tiedoston metatiedot.

#### Sivun vapaa tila (PFS)
PFS tunnistaa varauksen tilan ja määrittää vapaan tilan määrän.

 * Bitti 1: Osoittaa, onko sivu varattu vai ei.
 * Bitti 2: Osoittaa, onko sivu sekakokoinen.
 * Bitti 3: Ilmaisee, että tämä sivu on IAM-sivu.
 * Bitti 4: Osoittaa, että tämä sivu sisältää haamutietueita
 * Bitit 5–7: Yhdistetty kolmen bitin arvo, joka ilmaisee sivun täyteyden seuraavasti:
   * 0: Sivu on tyhjä
   * 1: Sivu on 1–50 % täynnä
   * 2: Sivu on täynnä 51–80 %
   * 3: Sivu on 81–95 % täynnä
   * 4: Sivu on 96–100 % täynnä

## Viitteet

 * [Tietokantatiedostot ja tiedostoryhmät](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Tietokannan irrottaminen ja liittäminen - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- versio 15)
 * [SQL Serverin datatiedoston anatomian analysointi](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

