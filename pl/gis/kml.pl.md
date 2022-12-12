{
  "date" : "2019-10-11",
  "keywords" :["plik kml", "co to jest plik kml", "plik", "przykład kml", "rozszerzenie pliku kml", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - język znaczników dziurki od klucza",
  "description":"Poznaj format pliku KML i interfejsy API, które mogą tworzyć i otwierać pliki KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik KML?

KML, Keyhole Markup Language) zawiera informacje geoprzestrzenne w notacji XML. Pliki zapisane w formacie KML można otwierać w aplikacjach systemu informacji geograficznej (GIS), o ile go obsługują. Wiele aplikacji zaczęło zapewniać obsługę formatu plików KML po tym, jak został on przyjęty jako międzynarodowy standard. KML wykorzystuje strukturę opartą na znacznikach z zagnieżdżonymi elementami i atrybutami. We wszystkich tagach rozróżniana jest wielkość liter, a kolejność tych tagów zgodnie z dokumentacją [KML](https://developers.google.com/kml/documentation/kmlreference) jest ważna do przestrzegania.

## Krótka historia ##

KML został pierwotnie opracowany do użytku z Google Earth, który był pierwotnie znany jako Keyhole Earth Viewer. KLM został przyjęty jako międzynarodowy standard w 2008 roku przez Open Geospatial Consortium w 2008 roku. Ponieważ format został opracowany do użytku z Google Earth, wyróżnia się tym, że jako pierwszy wyświetla i edytuje pliki KML. Z biegiem czasu pojawia się coraz więcej projektów, które zapewniają obsługę formatów plików KML, w tym kilka interfejsów API w różnych językach.

## Specyfikacje formatu pliku KML ##

Odniesienie KML to kompletny przewodnik dotyczący odsyłaczy w celu uzyskania pełnych specyfikacji formatu pliku. Standardowy plik KML składa się z:

* Oznaczenia miejsc
* Opisowe znaczniki miejsc HTMLin
* Nakładki naziemne
* Ścieżki
* Wielokąty

Oprócz tego zaawansowana wersja pliku KML może mieć:

* Style dla geometrii
* Style podświetlonych ikon
* Nakładki ekranowe
* Linki sieciowe

Każdy element KML zawiera informacje o długości geograficznej, które umożliwiają geolokalizację informacji zawartych w pliku. Mogą jednak istnieć dodatkowe parametry, takie jak kurs, wysokość i nachylenie.

### Oznaczenia miejsca ###

Jest używany do reprezentowania pozycji na powierzchni Ziemi i jest identyfikowany przez<Point> element. Poniżej przedstawiono przykład reprezentacji oznaczenia miejsca w pliku KML.

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

### Opisowy kod HTML w oznaczeniach miejsc ###

Z oznaczeniem miejsca można powiązać dodatkowe informacje, które dodatkowo poprawiają reprezentację oznaczenia miejsca. Takie informacje obejmują łącza, rozmiary czcionek, style i kolory. Ponadto obejmuje również wyrównanie tekstu i tabele, które mają być częścią oznaczenia miejsca.

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

### Nakładki podłoża ###

Reprezentują one nakładanie się obrazu na powierzchnię Ziemi. The<icon> elment zawiera łącze do pliku obrazu nakładki.

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

### Ścieżki ###

Ścieżki są reprezentowane przez<LineString> element, który jest zbiorem par lat-długości. Korzystając z nich, w programie Google Earth można utworzyć wiele różnych typów ścieżek.

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

## Odniesienia przestrzenne w pliku KML ##

Informacje zawarte w dowolnym pliku geoprzestrzennym na temat lokalizacji geograficznych mogą mieć różne znaczenia bez informacji o odniesieniach przestrzennych. Domyślnie odniesienia przestrzenne pliku KML są zdefiniowane przez Światowy System Geodezyjny z 1984 r., WGS84.

## Bibliografia ##

* [Odniesienie KML](https://developers.google.com/kml/documentation/kmlreference)
* [Samouczek dla programistów Google dla KML](https://developers.google.com/kml/documentation/kml_tut)
* [Format pliku KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

