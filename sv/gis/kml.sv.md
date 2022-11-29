{
  "date" : "2019-10-11",
  "keywords" :[ "kml-fil", "vad är en kml-fil", "fil", "kml-exempel", "kml-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Keyhole Markup Language",
  "description":"Läs mer om KML-filformat och API:er som kan skapa och öppna KML-filer.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en KML fil?

KML, Keyhole Markup Language) innehåller geospatial information i XML-notation. Filer sparade som KML kan öppnas i Geographic Information System (GIS) applikationer förutsatt att de stöder det. Många applikationer har börjat ge stöd för KML-filformat efter att det antagits som internationell standard. KML använder en taggbaserad struktur med kapslade element och attribut. Alla taggar är skiftlägeskänsliga och ordningen på dessa taggar, enligt [KML](https://developers.google.com/kml/documentation/kmlreference) referens, är viktig att följa.

## Kortfattad bakgrund ##

KML utvecklades ursprungligen för användning med Google Earth som ursprungligen var känd som Keyhole Earth Viewer. KLM antogs som internationell standard 2008 av Open Geospatial Consortium 2008. Eftersom formatet utvecklades för användning med Google Earth har det utmärkelsen att vara den första att visa och redigera KML-filer. Med tidens gång finns det nu fler och fler projekt som ger stöd för KML-filformat inklusive flera API:er på olika språk.

## KML-filformatspecifikationer ##

KML-referensen är en komplett guide för att hänvisa för att få fullständiga filformatspecifikationer. En standard KML-fil består av:

* Platsmärken
* Beskrivande HTML i platsmärken
* Marköverlägg
* Vägar
* Polygoner

Utöver dessa kan en avancerad version av KML-filen ha:

* Stilar för geometri
* Stilar för markerade ikoner
* Skärmöverlägg
* Nätverkslänkar

Vart och ett av KML-elementen har lat-long information som geolokaliserar informationen som finns i filen. Det kan dock finnas ytterligare parametrar som kurs, höjd och lutning.

### Platsmärken ###

Den används för att representera en position på jordens yta och identifieras av<Point> element. Följande är ett exempel på hur ett platsmärke representeras i KML-fil.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself,
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### Beskrivande HTML i platsmärken ###

Ytterligare information kan kopplas till ett platsmärke som ytterligare förbättrar representationen av platsmärket. Sådan information inkluderar länkar, teckenstorlekar, stilar och färger. Dessutom innehåller den också textjustering och tabeller som ska vara en del av platsmärket.

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

### Marköverlägg ###

Dessa representerar skiktningen av en bild på jordens yta. De<icon> elment innehåller länken till överläggsbildfilen.

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

### Banor ###

Banor representeras av<LineString> element som är en samling av lat-långa par. Med hjälp av dessa kan många olika typer av vägar skapas i Google Earth.

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

## Rumslig referens i KML-fil ##

Information som finns i en geospatial fil om Geo-Locations kan ha olika betydelser utan rumslig referensinformation. Som standard definieras den rumsliga referensen av KML-filen av World Geodetic System från 1984, WGS84.

## Referenser ##

* [KML-referens](https://developers.google.com/kml/documentation/kmlreference)
* [Google Developer Tutorial for KML](https://developers.google.com/kml/documentation/kml_tut)
* [KML-filformat](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

