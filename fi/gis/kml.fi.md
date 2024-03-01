{
  "date": "2019-10-11",
  "keywords": [
"kml tiedosto",
"mikä on kml-tiedosto",
"tiedosto",
"kml esimerkki",
"kml tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KML - Keyhole Markup Language",
  "description": "Lisätietoja KML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata KML-tiedostoja.",
  "linktitle": "KML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-fil"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on KML-tiedosto?

KML, Keyhole Markup Language) sisältää paikkatietoa XML-muodossa. KML-muodossa tallennetut tiedostot voidaan avata Geographic Information System (GIS) -sovelluksissa, jos ne tukevat sitä. Monet sovellukset ovat alkaneet tarjota tukea KML-tiedostomuodolle sen jälkeen, kun se on hyväksytty kansainväliseksi standardiksi. KML käyttää tunnistepohjaista rakennetta, jossa on sisäkkäisiä elementtejä ja attribuutteja. Kaikki tunnisteet erottelevat kirjainkoolla, ja näiden tunnisteiden järjestystä [KML](https://developers.google.com/kml/documentation/kmlreference)-viitteen mukaisesti on tärkeää noudattaa.

## Lyhyt historia ##

KML was originally developed for use with Google Earth which was originally known as Keyhole Earth Viewer. KLM was adopted as international standard in 2008 by the Open Geospatial Consortium in 2008. Koska muoto on kehitetty käytettäväksi Google Earthin kanssa, se eroaa siitä, että se on ensimmäinen, joka katselee ja muokkaa KML-tiedostoja. Ajan myötä on tullut yhä useampia projekteja, jotka tarjoavat tukea KML-tiedostomuodoille, mukaan lukien useita API:ita eri kielillä.

## KML-tiedostomuodon tekniset tiedot ##

KML-viite on täydellinen opas viittaukseen, jotta saat täydelliset tiedostomuodon määritykset. Tavallinen KML-tiedosto koostuu:

* Paikkamerkit

* Kuvaava HTML paikkamerkitsimeissä

* Maapeittokuvat

* Polut

* Monikulmiot


Näiden lisäksi KML-tiedoston edistyneessä versiossa voi olla:

* Geometrian tyylejä

* Korostettujen kuvakkeiden tyylejä

* Näytön peittokuvat

* Verkkolinkit


Jokaisella KML-elementillä on lat-pituiset tiedot, jotka paikantavat tiedostossa olevat tiedot. Lisäparametreja voi kuitenkin olla, kuten suunta, korkeus ja kallistus.

### Paikkamerkit ###

Sitä käytetään edustamaan sijaintia maan pinnalla, ja se tunnistetaan<Point> elementti. Seuraavassa on esimerkki siitä, kuinka paikkamerkitsin esitetään KML-tiedostossa.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### Kuvaava HTML paikkamerkitsimeissä ###

Paikkamerkitsimeen voidaan liittää lisätietoja, mikä parantaa paikkamerkitsimen esitystapaa entisestään. Tällaisia tietoja ovat linkit, kirjasinkoot, tyylit ja värit. Lisäksi se sisältää myös tekstin tasauksen ja taulukot osaksi paikkamerkitsintä.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### Maapeittokuvat ###

Nämä edustavat kuvan kerrostumista maan pinnalle. The<icon> elment sisältää linkin peittokuvatiedostoon.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### Polut ###

Polkuja edustaa<LineString> elementti, joka on kokoelma lat-pitkiä pareja. Näitä käyttämällä voidaan luoda monia erilaisia polkuja Google Earthissa.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## Tilaviittaukset KML-tiedostossa ##

Missä tahansa paikkatietotiedostossa Geo-sijainteja koskevilla tiedoilla voi olla erilaisia merkityksiä ilman paikkaviittaustietoja. Oletusarvoisesti KML-tiedoston spatiaalinen viittaus on määritetty World Geodetic System of 1984 -järjestelmässä WGS84.

## Viitteet ##

* [KML-viite](https://developers.google.com/kml/documentation/kmlreference)

* [Google Developer Tutorial for KML](https://developers.google.com/kml/documentation/kml_tut)

* [KML-tiedostomuoto](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)


