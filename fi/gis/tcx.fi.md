{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TCX-tiedostomuoto - koulutuskeskuksen XML-tiedosto",
  "description":"Opi TCX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TCX-tiedostoja.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx-fi",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Mikä on TCX-tiedosto?

TCX (Training Center XML) -tiedosto on tiedonsiirtomuoto, jota käytetään tietojen jakamiseen kuntolaitteiden välillä. Se esiteltiin vuonna 2008 Garminin Training Center -tuotteen kanssa. Harjoitustiedot, kuten syke, juoksupoljinnopeus, poljinnopeus, kalorit ja kierrosaika, tallennetaan [XML](/web/xml/)-muodossa TCX-tiedostoon. Lisäksi TCX-tiedostossa on yhteenvetotiedot harjoitusradasta. TCX-tiedostot ovat samanlaisia kuin [FIT](/gis/fit/)-tiedostot, jotka on luotu puettavilla Garmin-urheilulaitteilla.

## TCX-tiedostomuoto - Lisätietoja

TCX-tiedostot tallennetaan levylle XML-tiedostoina, ja jokainen tietue tallennetaan aktiviteettina. Harjoitus sisältää kaikki harjoituksen tiedot, kuten ajan, kierrosajan, tunnisteen, sykkeen, intensiteetin, poljinnopeuden ja raidan tiedot, jotka sisältävät sijaintiparit sekä kyseisen lat-pitkän sijainnin aikaleiman, joka on samanlainen kuin [GPX](/gis/gpx/) tiedostot.

### TCX-tiedostomuodon versiot

Tästä muodosta on kaksi versiota, joissa on omat Garminin isännöimät XML-skeemat. Seuraavassa on muutamia niistä:

 * https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
 * https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
 * https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX Data Protocol

A swift version of TCX XML format is available on Github as [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Viitteet ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)

* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)


