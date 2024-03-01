{
  "date": "2021-07-18",
  "keywords": [
"LOC",
"tiedosto",
"laajennus",
"tiedosto muoto",
"GPS-sijainti",
"Reittipiste"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOC - GPS-paikannustiedostomuoto",
  "description": "Opi LOC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata LOC-tiedostoja.",
  "linktitle": "LOC",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-lo-fic"
}
},
  "lastmod": "2021-07-18"
}

## Mikä on LOC-tiedosto?

Tiedosto, jonka pääte on .loc, on GPS-sijaintitiedosto, joka sisältää geospatiaalisia sijainteja reittipisteinä. Reittipiste on leveys- ja pituusaste-arvojen pari, joka viittaa paikkaan, jota GIS-sovellukset käyttävät. GPS-kartoitusohjelmat, kuten DeLorme Topo, käyttävät LOC-tiedostoja näiden LOC-tiedostojen sisältämien tietojen lukemiseen ja näyttämiseen loppukäyttäjien valittavissa tasoina. Lisäksi niitä käytetään GPS-tietojen vaihtamiseen sovellusten välillä. LOC-tiedostoja voidaan avata käyttämällä sovelluksia, kuten [TopoGrafix EasyGPS](https://www.easygps.com/), joka näyttää tällaisten tiedostojen sisällön tasoina ja datana, joka on piirretty kartalle vastaavassa maantieteellisessä sijainnissa.

## LOC-tiedostomuoto - lisätietoja

LOC-tiedostot ovat samankaltaisia [GPX](/gis/gpx/)-tiedostojen kanssa, mutta ne tallennetaan eri muodossa. Nämä tallennetaan [XML](/web/xml/)-tiedostoina, joissa reittipisteiden sisältö ja niihin liittyvät tiedot sisältyvät jäsenneltyihin tunnisteisiin. Koska XML on yleistetty kieli tietojen vaihtoon eri sovellusten välillä, tämä helpottaa LOC-tietojen vaihtoa muiden sovellusten kanssa.

## LOC-tiedostomuoto - esimerkki

Seuraavassa on yhden reittipisteen otsikko ja teksti LOC-tiedostosta. Kuten voidaan nähdä, otsikkotiedot sisältävät datan sijaintilähteen. Reittipiste sisältää tietoja, kuten ID ja siihen liittyvät sisältötiedot. Lopuksi reittipiste on kokoelma leveys- ja pituusastearvoja sekä tähän reittipisteeseen liittyvää tekstiä.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Viitteet

* [TopGraphic EasyGPS](https://www.easygps.com/)


