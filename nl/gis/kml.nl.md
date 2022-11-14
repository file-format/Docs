{
  "date" : "2019-10-11",
  "keywords" :[ "kml-bestand", "wat is een kml-bestand", "bestand", "kml-voorbeeld", "kml-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Keyhole Markup Language",
  "description":"Meer informatie over KML-bestandsindeling en API's die KML-bestanden kunnen maken en openen.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een KML-bestand?

KML, Keyhole Markup Language) bevat geospatiale informatie in XML-notatie. Bestanden die als KML zijn opgeslagen, kunnen worden geopend in GIS-toepassingen (Geografisch Informatiesysteem), op voorwaarde dat ze dit ondersteunen. Veel toepassingen bieden ondersteuning voor het KML-bestandsformaat nadat het als internationale standaard is aangenomen. KML gebruikt een op tags gebaseerde structuur met geneste elementen en attributen. Alle tags zijn hoofdlettergevoelig en de volgorde van deze tags, volgens de [KML](https://developers.google.com/kml/documentation/kmlreference) Reference, is belangrijk om te volgen.

## Korte geschiedenis ##

KML is oorspronkelijk ontwikkeld voor gebruik met Google Earth, dat oorspronkelijk bekend stond als Keyhole Earth Viewer. KLM is in 2008 door het Open Geospatial Consortium als internationale standaard aangenomen in 2008. Aangezien het formaat is ontwikkeld voor gebruik met Google Earth, onderscheidt het zich als eerste om KML-bestanden te bekijken en te bewerken. Met het verstrijken van de tijd zijn er nu steeds meer projecten die ondersteuning bieden voor KML-bestandsindelingen, waaronder verschillende API's in verschillende talen.

## Specificaties KML-bestandsindeling ##

De KML-referentie is een complete gids voor verwijzingen om de volledige specificaties van het bestandsformaat te hebben. Een standaard KML-bestand bestaat uit:

* Plaatsmarkeringen
* Beschrijvende HTML in plaatsmarkeringen
* Grondoverlays
* Paden
* Veelhoeken

Daarnaast kan een geavanceerde versie van het KML-bestand het volgende bevatten:

* Stijlen voor geometrie
* Stijlen voor gemarkeerde pictogrammen
* Schermoverlays
* Netwerklinks

Elk van de KML-elementen heeft lat-long-informatie waarmee de informatie in het bestand wordt gelokaliseerd. Er kunnen echter ook aanvullende parameters zijn, zoals koers, hoogte en kanteling.

### Plaatsmarkeringen ###

Het wordt gebruikt om een positie op het aardoppervlak weer te geven en wordt geïdentificeerd door de<Point> element. Hieronder volgt een voorbeeld van hoe een plaatsmarkering wordt weergegeven in een KML-bestand.

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

### Beschrijvende HTML in plaatsmarkeringen ###

Aanvullende informatie kan worden gekoppeld aan een plaatsmarkering die de weergave van de plaatsmarkering verder verbetert. Dergelijke informatie omvat links, lettergroottes, stijlen en kleuren. Daarnaast bevat het ook tekstuitlijning en tabellen die deel uitmaken van de plaatsmarkering.

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

### Ground Overlays ###


Deze vertegenwoordigen de gelaagdheid van een afbeelding op het aardoppervlak. De<icon> elment bevat de link naar het overlay-afbeeldingsbestand.

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

### Paden ###

Paden worden weergegeven door<LineString> element dat een verzameling lat-long paren is. Hiermee kunnen in Google Earth veel verschillende soorten paden worden gemaakt.

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

## Ruimtelijke verwijzingen in KML-bestand ##

Informatie in elk Geospatial-bestand over Geo-Locaties kan verschillende betekenissen hebben zonder ruimtelijke referentie-informatie. Standaard worden de ruimtelijke referenties van het KML-bestand gedefinieerd door het World Geodetic System van 1984, WGS84.

## Referenties ##

* [KML-referentie](https://developers.google.com/kml/documentation/kmlreference)
* [Google Developer Tutorial voor KML](https://developers.google.com/kml/documentation/kml_tut)
* [KML-bestandsindeling](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

