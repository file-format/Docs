{
  "date": "2019-10-11",
  "keywords": [
"kml fil",
"hvad er en kml-fil",
"fil",
"kml eksempel",
"kml filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KML - Keyhole Markup Language",
  "description": "Lær om KML-filformat og API'er, der kan oprette og åbne KML-filer.",
  "linktitle": "KML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-dal"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en KML fil?

KML, Keyhole Markup Language) indeholder geospatial information i XML-notation. Filer gemt som KML kan åbnes i Geographic Information System (GIS) applikationer, forudsat at de understøtter det. Mange applikationer er begyndt at understøtte KML-filformatet, efter at det er blevet vedtaget som international standard. KML bruger en tag-baseret struktur med indlejrede elementer og attributter. Alle tags skelner mellem store og små bogstaver, og rækkefølgen af disse tags i henhold til [KML](https://developers.google.com/kml/documentation/kmlreference)-referencen er vigtig at følge.

## Kort historie ##

KML was originally developed for use with Google Earth which was originally known as Keyhole Earth Viewer. KLM was adopted as international standard in 2008 by the Open Geospatial Consortium in 2008. Da formatet blev udviklet til brug med Google Earth, har det den udmærkelse, at det er det første til at se og redigere KML-filer. Med tiden er der nu flere og flere projekter, der understøtter KML-filformater, herunder flere API'er på forskellige sprog.

## KML-filformatspecifikationer ##

KML-referencen er en komplet vejledning til henvisning for at få de fulde filformatspecifikationer. En standard KML-fil består af:

* Stedsmarkører

* Beskrivende HTML i stedsmarkører

* Jordoverlejringer

* Stier

* Polygoner


Ud over disse kan en avanceret version af KML-fil have:

* Stilarter til geometri

* Stilarter til fremhævede ikoner

* Skærmoverlejringer

* Netværkslinks


Hvert af KML-elementerne har lat-long information, der geolokaliserer oplysningerne i filen. Der kan dog også være yderligere parametre som kurs, højde og hældning.

### Stedsmærker ###

Det bruges til at repræsentere en position på Jordens overflade og identificeres af<Point> element. Følgende er et eksempel på, hvordan en stedsmarkør er repræsenteret i KML-fil.

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

### Beskrivende HTML i stedsmarkører ###

Yderligere oplysninger kan knyttes til en stedsmarkør, der yderligere forbedrer repræsentationen af stedsmarkøren. Sådanne oplysninger omfatter links, skriftstørrelser, typografier og farver. Derudover inkluderer det også tekstjustering og tabeller, der skal være en del af stedsmarkøren.

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

### Jordoverlejringer ###

Disse repræsenterer lagdelingen af et billede på jordens overflade. Det<icon> elment indeholder linket til overlejringsbilledfilen.

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

### Stier ###

Stier er repræsenteret ved<LineString> element, der er en samling af lat-lange par. Ved hjælp af disse kan der oprettes mange forskellige typer stier i Google Earth.

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

## Rumlig reference i KML-fil ##

Oplysninger indeholdt i enhver geospatial fil om Geo-Locations kan have forskellige betydninger uden rumlig referenceinformation. Som standard er den rumlige reference til KML-filen defineret af World Geodetic System of 1984, WGS84.

## Referencer ##

* [KML-reference](https://developers.google.com/kml/documentation/kmlreference)

* [Google Developer Tutorial for KML](https://developers.google.com/kml/documentation/kml_tut)

* [KML-filformat](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)


