{
  "date" : "2019-10-11",
  "keywords" :[ "fișier kml", "ce este un fișier kml", "fișier", "exemplu kml", "extensie fișier kml", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML – Limbajul de marcare Keyhole",
  "description":"Aflați despre formatul de fișier KML și despre API-urile care pot crea și deschide fișiere KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier KML?

KML, Keyhole Markup Language) conține informații geospațiale în notație XML. Fișierele salvate ca KML pot fi deschise în aplicațiile Sistemului de Informații Geografice (GIS) cu condiția să îl accepte. Multe aplicații au început să ofere suport pentru formatul de fișier KML după ce acesta a fost adoptat ca standard internațional. KML folosește o structură bazată pe etichete cu elemente și atribute imbricate. Toate etichetele țin cont de majuscule și minuscule, iar ordinea acestor etichete, conform Referinței [KML](https://developers.google.com/kml/documentation/kmlreference), este important de urmat.

## Scurt istoric ##

KML a fost dezvoltat inițial pentru a fi utilizat cu Google Earth, cunoscut inițial ca Keyhole Earth Viewer. KLM a fost adoptat ca standard internațional în 2008 de Open Geospatial Consortium în 2008. Deoarece formatul a fost dezvoltat pentru utilizare cu Google Earth, are distincția de a fi primul care vizualizează și editează fișierele KML. Odată cu trecerea timpului, există acum din ce în ce mai multe proiecte care oferă suport pentru formatele de fișiere KML, inclusiv mai multe API-uri în diferite limbi.

## Specificații de format de fișier KML ##

Referința KML este un ghid complet de referință pentru a avea specificațiile complete ale formatului de fișier. Un fișier KML standard este format din:

* Marcatori de locație
* HTML descriptiv în Marcatori de locație
* Suprapuneri la sol
* Cărări
* Poligoane

În plus față de acestea, o versiune avansată a fișierului KML poate avea:

* Stiluri pentru geometrie
* Stiluri pentru pictogramele evidențiate
* Suprapuneri de ecran
* Legături de rețea

Fiecare element KML are informații lat-long care geo-localizează informațiile prezente în fișier. Cu toate acestea, pot exista și parametri suplimentari, cum ar fi direcția, altitudinea și înclinarea.

### Marcatori de locație ###

Este folosit pentru a reprezenta o poziție pe suprafața Pământului și este identificat prin<Point> element. Mai jos este un exemplu de reprezentare a unui marcator de locație în fișierul KML.

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

### HTML descriptiv în marcatori de locație ###

Informații suplimentare pot fi asociate cu un marcator de locație care îmbunătățește și mai mult reprezentarea marcatorului de locație. Astfel de informații includ linkuri, dimensiunile fonturilor, stilurile și culorile. În plus, include și alinierea textului și tabele care vor face parte din marcatorul de locație.

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

### Suprapuneri la sol ###

Acestea reprezintă stratificarea unei imagini pe suprafața Pământului. The<icon> elment conține linkul către fișierul imagine suprapus.

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

### Căi ###

Căile sunt reprezentate de<LineString> element care este o colecție de perechi lat-long. Folosind acestea, pot fi create multe tipuri diferite de căi în Google Earth.

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

## Referințe spațiale în fișierul KML ##

Informațiile conținute în orice fișier geospațial despre locații geografice pot avea semnificații diferite fără informații de referință spațială. În mod implicit, referința spațială a fișierului KML este definită de World Geodetic System din 1984, WGS84.

## Referințe ##

* [Referință KML](https://developers.google.com/kml/documentation/kmlreference)
* [Tutorial pentru dezvoltatori Google pentru KML](https://developers.google.com/kml/documentation/kml_tut)
* [Format de fișier KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

