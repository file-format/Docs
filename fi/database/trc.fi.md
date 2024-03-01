{
  "date": "2021-08-24",
  "keywords": [
"trc tiedosto",
"trc-tiedostomuoto",
"mikä on trc-tiedosto",
"tiedosto",
"trc esimerkki",
"trc tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi TRC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TRC-tiedostoja.",
  "title": "TRC - SQL Server Trace File",
  "linktitle": "TRC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-tr-fic"
}
},
  "lastmod": "2021-08-24"
}

## Mikä on TRC-tiedosto?
Tiedosto, jonka laajennus on .trc, sisältää Miscrosoft SQL -palvelintietokannan toiminnan jäljitystulokset. Nämä tiedostot on luotu ohjelmistolla SQL Server Profiler; yleensä pakattu Microsoft SQL Server -ohjelmiston kanssa. Tietokannan ylläpitäjät voivat analysoida tietokannan lausekkeiden sarjaa ja tarkastella jäljityslokia, jos epäillään jonkinlaisia virheitä tai varoituksia. Nämä tiedostot sijaitsevat yleensä tyypillisessä MSSQL:n LOG-kansiossa Program Files -hakemistossa Windows-käyttöjärjestelmässä.

## TRC-tiedostomuoto
SQL Server Profiler käyttää TRC-tiedostomuotoa luodakseen automaattisesti uuden jäljen MS SQL -palvelimen äskettäin suorittamista käskyistä. SQL Server Profiler käyttää oletusmallia kaikille uusille jäljille. Ohjelmisto sisältää kuitenkin useita ennalta määritettyjä malleja tietyntyyppisten tapahtumien seurantaan. Myös SQL Server Profileria voidaan käyttää luomaan malleja, jotka määrittelevät jäljiin sisällytettävät tapahtumaluokat ja tietosarakkeet.

### Ennalta määritetyt mallit
Tässä on luettelo joistakin SQL Server Profileriin sisältyvistä esimääritetyistä malleista:
- **SP_Counts**: Kaappaa tallennettujen toimintojen suorituskäyttäytymisen ajan kuluessa.
- **Standard**: Yleinen aloituspiste jäljen luomiseen.
- **TSQL**: Kaappaa kaikki asiakkaiden SQL Serverille lähettämät Transact-SQL-käskyt ja niiden antamisajan.
- **TSQL_Duration**: Kaappaa kaikki asiakkaiden SQL Serverille lähettämät Transact-SQL-käskyt, niiden suoritusajan ja ryhmittelee ne keston mukaan.
- **TSQL_Grouped**: Käytä tietyn asiakkaan tai käyttäjän kyselyjen tutkimiseen.
- **TSQL_Locks**: Käytä umpikujien vianmääritykseen, lukitsemiseen aikakatkaisuun ja eskalaatiotapahtumien lukitsemiseen.
- **TSQL_Replay**: Käytä iteratiiviseen viritykseen, kuten vertailutestaukseen.
- **TSQL_SPs**: Käytä tallennettujen proseduurien komponenttivaiheiden analysointiin.
- **Tunning**: Käytä jäljitystulosteen tuottamiseen, jota Database Engine Tuning Advisor voi käyttää työkuormana tietokantojen virittämiseen.
### Korreloi jälki Windowsin suorituskykylokin tietojen kanssa
SQL Server Profileria voidaan käyttää avaamaan Microsoft Windowsin suorituskykyloki, valitsemaan laskurit, jotka korreloivat jäljityksen kanssa, ja näyttämään valitut suorituskykylaskurit jäljen rinnalla MS SQL Server Profiler -käyttöliittymässä. Jos haluat ilmoittaa suorituslokitiedot, jotka korreloivat valitun jäljitystapahtuman kanssa, pystysuora punainen palkki SQL Server Profilerin System Monitor -tietoikkunaruudussa.


## Viitteet ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)


