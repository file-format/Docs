{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDLC - Raportin määritelmäkielen asiakaspuoli",
  "keywords": [
"rdlc",
"raportin määrittelykieli",
"mkv muodossa",
"XSD",
"raportin määrittelykielen asiakaspuolella"
],
  "description": "Lisätietoja RDLC-tiedostomuodosta, joka on SQL Server Reporting Services -raporttimäärittelyn XML-esitys.",
  "linktitle": "RDLC",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rdl-fic"
}
},
  "lastmod": "2021-03-02"
}

## Mikä on RDLC-tiedosto? ##

RDLC on lyhenne sanoista Report Definition Language Client. Itse asiassa se on Microsoftin raportointitekniikalla luodun raporttitiedoston laajennus. Näiden tiedostojen luomiseen käytetään Report Designerin SQL Server 2005 -versiota. Asiakaspuolen **ReportViewer**-säädin voi suorittaa RDLC-raportit suoraan.

## RDL VS RDLC -tiedostot
|.rdl-tiedostot |.rdlc-tiedostot|
---|---|
|RDL-tiedostot luodaan Report Designerin SQL Server 2005 -versiolla|RDLC-tiedostot luodaan Report Designerin Visual Studio 2005 -versiolla|
|Sitä käytetään SQL Server Reporting Servicesissä|Se on käytössä Visual Studiossa|
|Se on etäraportti|Se on paikallinen raportti|
|Tarvitset Reporting Services -ilmentymän sen suorittamiseen|Ei tarvitse Reporting Services -esiintymää|

## Client Report Definition (.rdlc) -tiedostojen luominen
ReportViewer-ohjausobjektia käytetään asiakasraporttimääritystiedostojen (.rdlc) suorittamiseen käyttämällä ohjausobjektin sisäänrakennettua käsittelytoimintoa. Paikallisessa käsittelytilassa suoritettavat asiakasraportit voidaan luoda helposti sovellusprojektissasi. Seuraavat menetelmät raportin luomiseen:

- Luo uusi asiakasraporttimäärittely (.rdlc) käyttämällä **Ohjattua raportointitoimintoa**.

- Luo uusi asiakasraporttimääritystiedosto (.rdlc) Visual Studion avulla.

- Luo raporttimääritelmä ohjelmallisesti.


Voit esikatsella raporttia vain suorittamalla sen **ReportViewer**-ohjauksessa. Huomaa, että voit avata ja muokata raporttimääritelmää milloin tahansa ja sitten rakentaa tai ottaa käyttöön sovelluksen tarkistaaksesi tulokset.

## Viitteet ##

- {{HYPERLINKKI}})

