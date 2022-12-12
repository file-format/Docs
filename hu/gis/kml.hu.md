{
  "date" : "2019-10-11",
  "keywords" :[ "kml fájl", "mi az a kml fájl", "fájl", "kml példa", "kml fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML – Keyhole Markup Language",
  "description":"További információ a KML-fájlformátumról és az API-król, amelyek KML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a KML-fájl?

KML, Keyhole Markup Language) XML-jelölésben tartalmaz térinformációkat. A KML formátumban mentett fájlok megnyithatók a Geographic Information System (GIS) alkalmazásaiban, feltéve, hogy támogatják azt. Sok alkalmazás megkezdte a KML-fájlformátum támogatását, miután nemzetközi szabványként elfogadták. A KML címke-alapú struktúrát használ beágyazott elemekkel és attribútumokkal. Minden címke megkülönbözteti a kis- és nagybetűket, és fontos betartani a címkék sorrendjét a [KML](https://developers.google.com/kml/documentation/kmlreference) referencia szerint.

## Rövid története ##

A KML-t eredetileg a Google Földdel való használatra fejlesztették ki, amely eredetileg Keyhole Earth Viewer néven volt ismert. A KLM-et 2008-ban fogadta el nemzetközi szabványként az Open Geospatial Consortium 2008-ban. Mivel a formátumot a Google Földhöz való használatra fejlesztették ki, az a megkülönböztetés, hogy elsőként tekint meg és szerkeszt KML-fájlokat. Az idő múlásával egyre több olyan projekt létezik, amely támogatja a KML-fájlformátumokat, beleértve számos API-t különböző nyelveken.

## KML fájlformátum specifikációi ##

A KML-referencia egy teljes útmutató a hivatkozásokhoz, hogy a teljes fájlformátum-specifikációhoz rendelkezzen. Egy szabványos KML-fájl a következőkből áll:

* Helyjelzők
* Leíró HTML helyjelzőkben
* Földi átfedések
* Utak
* Sokszögek

Ezeken kívül a KML-fájl továbbfejlesztett verziója a következőket is tartalmazhatja:

* Stílusok a geometriához
* Stílusok a kiemelt ikonokhoz
* Képernyőfedések
* Hálózati hivatkozások

Mindegyik KML-elemnek van hosszúságú információja, amely földrajzilag meghatározza a fájlban található információkat. Lehetnek azonban további paraméterek, például irány, magasság és dőlésszög.

### Helyjelzők ###

A Föld felszínén elfoglalt helyzet ábrázolására szolgál, és a<Point> elem. Az alábbiakban egy példa látható a helyjelzők KML-fájlban való megjelenítésére.

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

### Leíró HTML helyjelzőkben ###

További információk társíthatók egy helyjelzőhöz, amely tovább javítja a helyjelző megjelenítését. Az ilyen információk közé tartoznak a hivatkozások, a betűméretek, a stílusok és a színek. Ezenkívül szövegigazítást és táblázatokat is tartalmaz, amelyek a helyjelző részét képezik.

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

### Földi lefedések ###

Ezek a képnek a Föld felszínére való rétegződését jelentik. Az<icon> Az elment tartalmazza az átfedő képfájl hivatkozását.

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

### Utak ###

Az utakat a<LineString> elem, amely lat-long párok gyűjteménye. Ezek segítségével sokféle útvonalat lehet létrehozni a Google Földben.

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

## Térbeli hivatkozás a ## KML-fájlban

A földrajzi helyekkel kapcsolatos bármely térinformatikai fájlban található információk térbeli hivatkozási információk nélkül eltérő jelentéssel bírhatnak. Alapértelmezés szerint a KML-fájlok térbeli hivatkozását az 1984-es World Geodetic System, WGS84 határozza meg.

## Referenciák ##

* [KML-referencia](https://developers.google.com/kml/documentation/kmlreference)
* [Google Developer Tutorial for KML](https://developers.google.com/kml/documentation/kml_tut)
* [KML-fájlformátum](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

