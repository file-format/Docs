{
  "date": "2020-11-11",
  "keywords": [
"NDF",
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
  "description": "Opi MDF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata NDF-tiedostoja.",
  "title": "NDF-tiedostomuoto - SQL Server -päätietokantatiedosto",
  "linktitle": "NDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nd-fif"
}
},
  "lastmod": "2020-08-12"
}

## Mikä on NDF-tiedosto?

Tiedosto, jonka pääte on .ndf, on toissijainen tietokantatiedosto, jota [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) käyttää käyttäjätietojen tallentamiseen. NDF on toissijainen tallennustiedosto, koska SQL-palvelin tallentaa käyttäjän määrittämät tiedot ensisijaiseen tallennustiedostoon, joka tunnetaan nimellä [MDF](/database/mdf/). NDF-datatiedosto on valinnainen, ja se on käyttäjän määrittämä tietojen tallennuksen hallintaan, jos ensisijainen MDF-tiedosto käyttää kaiken varatun tilan. Se on yleensä tallennettu erilliselle levylle ja voi levitä useille tallennuslaitteille. MDF-tiedostojen läsnäolo on välttämätöntä NDF-tiedostojen avaamiseksi.

## NDF-tiedostomuoto

NDF-tiedostomuoto ei eroa {{HYPERLINKKI}}:sta, ja se käyttää sivuja tietojen tallennuksen perusyksikkönä. jokainen sivu alkaa 96 tavun otsikolla, joka sisältää:

 * Sivun tunnus
 * Rakenteen tyyppi
 * Tietueiden määrä sivuilla
 * Osoittimet edelliselle ja seuraavalle sivulle

### NDF-tiedostorakenne

MDF-tiedostolla on seuraava tietorakenne.

 * Sivu 0: Otsikko
 * Sivu 1: Ensimmäinen PFS
 * Sivu 2: Ensimmäinen GAM
 * Sivu 3: Ensimmäinen SGAM
 * Sivu 4: Käyttämätön
 * Sivu 5: Käyttämätön
 * Sivu 6: Ensimmäinen DCM
 * Sivu 7: Ensimmäinen BCM

#### NDF-tiedoston otsikko

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

## Tietotiedostosivu

SQL Server -datatiedoston sivut alkavat nollasta (0) ja kasvavat peräkkäin. Jokainen tiedosto tunnistetaan yksilöllisestä tiedostotunnusnumerosta. Tiedostotunnus- ja sivunumeropari tunnistaa yksiselitteisesti sivun tietokannassa. Esimerkki sivunumeroista tietokannassa on seuraavan kuvan mukainen.

{{< figure src="../ndf.png" alt="NDF-tietokantatiedostomuoto" >}}

Tämä esimerkki näyttää sivunumerot tietokannassa, jossa on 4 Mt:n ensisijainen tiedosto ja 1 Mt:n toissijainen tiedosto.

## Viitteet

 * [Tietokantatiedostot ja tiedostoryhmät](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
 * [Tietokannan irrottaminen ja liittäminen - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- versio 15)
 * [SQL Serverin datatiedoston anatomian analysointi](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

