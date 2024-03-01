{
  "date": "2019-10-11",
  "keywords": [
"gml-tiedosto",
"mikä on gml-tiedosto",
"tiedosto",
"gml esimerkki",
"gml tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GML - Maantieteellisen merkintäkielen tiedostomuoto",
  "description": "Lisätietoja GML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata GML-tiedostoja.",
  "linktitle": "GML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gm-fil"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on GML-tiedosto?

GML on lyhenne sanoista Geography Markup Language, joka perustuu Open Geospatial Consortiumin (OGC) kehittämiin XML-spesifikaatioihin. Muotoa käytetään maantieteellisten tietojen tallentamiseen eri tiedostomuotojen välistä vaihtoa varten. Se toimii mallinnuskielenä maantieteellisille järjestelmille sekä avoimena vaihtomuotona maantieteellisille tapahtumille Internetissä.

## GML-tiedostomuoto ##

Kuten useimmissa XML-pohjaisissa kieliopeissa, kielioppi sisältää kaksi osaa – asiakirjaa kuvaava skeema ja todelliset tiedot sisältävä ilmentymädokumentti. GML-dokumentti kuvataan GML-skeemalla. Näin käyttäjät ja kehittäjät voivat kuvata yleisiä maantieteellisiä tietojoukkoja, jotka sisältävät pisteitä, viivoja ja polygoneja. Sovelluskaavioiden avulla käyttäjät voivat viitata teihin, moottoriteihin ja siltoihin pisteiden, viivojen ja polygonien sijaan.

On syytä huomata, että GML:ää ei pidä tulkita paikkatiedon esittämiseksi kartoissa. GML-sisällön esitystapa on erilainen kuin tarkoitus, jota varten GML luotiin. Lyhyesti sanottuna GML on samanlainen kuin XML, koska sitä käytetään vain sellaisen tilasisällön säilyttämiseen, jota voidaan käyttää kartoitussovelluksissa näyttötarkoituksiin.

### Sisällönmuodostus GML:ssä ###

GML represents spatial data using features which is a list of properties and geometries. A Property has a name, type and value description. Geometries are composed of basic geometry building blocks such as:

* pisteet

* rivit

*käyrät

* pinnat ja

* polygonit


GML:n tulevien versioiden on suunniteltu tukevan 3D-geometriaa sekä ominaisuuksien välisiä topologisia suhteita.

GML-koodaus mahdollistaa jo melko monimutkaiset ominaisuudet. Ominaisuus voi esimerkiksi koostua muista ominaisuuksista. Yksittäinen ominaisuus, kuten lentoasema, voi siten koostua muista ominaisuuksista, kuten taksireiteistä, kiitotieistä, ripustimista ja lentoterminaaleista. Maantieteellisen kohteen geometria voi myös koostua useista geometriaelementeistä. Geometrisesti monimutkainen piirre voi siten koostua yhdistelmästä geometriatyyppejä, mukaan lukien pisteitä, viivajonoja ja polygoneja.

### Esimerkkejä ###

GML 1.0 ja 2.0 koodaavat polygonit, pisteet ja viivajono-objektit seuraavasti:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Viitteet ##

* [GML-tiedot](https://www.ogc.org/standard/gml/)

* [GML - Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)


