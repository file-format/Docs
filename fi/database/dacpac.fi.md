{
  "date": "2021-09-06",
  "keywords": [
"dacpac",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Data Tier -sovelluspaketti"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi DACPAC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DACPAC-tiedostoja.",
  "title": "DACPAC - Data Tier -sovelluspaketti",
  "linktitle": "DACPAC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dacpa-fic"
}
},
  "lastmod": "2021-09-06"
}

## Mikä on DACPAC-tiedosto?

Tiedosto, jonka laajennus on .dacpac (lyhenne sanoista Data Tier AppliCation Package), on Microsoft SQL Server -tietotasosovelluksella luotu tietokantatiedosto, joka sisältää tietokantamallin tietokantaobjektien esittämistä varten. Koska se sisältää tietokannan täydellisen mallin, sitä käytetään tietokannan palauttamiseen mallissa olevista tiedoista. DACPAC-tiedostot luovutetaan yleensä käyttöönottoryhmille asennettavaksi asiakkaan tiloihin tietokannan palauttamiseksi. Nämä voidaan avata
{{HYPERLINKKI1}}.

## DACPAC-tiedostomuoto – lisätietoja

DACPAC-tietopakettitiedostot ovat itse asiassa pakattuja ZIP-tiedostoja, jotka sisältävät useita [XML](/web/xml/)-tiedostoja, jotka sisältävät tietoa tietokantamallista, kuten taulukoita ja näkymiä, joita käytetään tietokannan palauttamiseen. Jos haluat tarkastella DACPAC-tiedostojen sisältöä, nimeä tiedostot .dacpacista uudelleen muotoon [.zip](/compression/zip/) ja pura zip-arkisto millä tahansa purkuapuohjelmalla.

Seuraavassa on muutamia tiedostoja, jotka löytyvät DACPAC-tiedostosta.

 * [Content_Types].xml
```
<?xml version=1.0 encoding=utf-8?>
<Types
xmlns=http://schemas.openxmlformats.org/package/2006/content-types>
<Default Extension=xml ContentType=text/xml />
</Types>
```
 * DacMetadata.xml

```
<?xml version=1.0 encoding=utf-8?>
<DacType xmlns=http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02>
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
 * Origin.xml

 * malli.xml

On huomattava, että DACPAC ei sisällä DATA- ja muita palvelintason objekteja. Tiedosto voi sisältää kaikki objektityypit, jotka voidaan säilyttää SSDT-projektissa.

## Viitteet

* [Datatason sovellukset – edut](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)

* [Datatason sovelluksen käyttöönotto – Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)

* [How to create DACPAC File?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)
