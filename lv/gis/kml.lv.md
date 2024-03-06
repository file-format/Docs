{
  "date": "2019-10-11",
  "keywords": [
"kml failu",
"kas ir kml fails",
"failu",
"kml piemērs",
"kml faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KML — atslēgas cauruma iezīmēšanas valoda",
  "description": "Uzziniet par KML failu formātu un API, kas var izveidot un atvērt KML failus.",
  "linktitle": "KML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-lvl"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir KML fails?

KML, Keyhole Markup Language) satur ģeotelpisko informāciju XML apzīmējumā. Failus, kas saglabāti kā KML, var atvērt ģeogrāfiskās informācijas sistēmas (GIS) lietojumprogrammās, ja tās to atbalsta. Daudzas lietojumprogrammas ir sākušas nodrošināt atbalstu KML failu formātam pēc tam, kad tas ir pieņemts kā starptautisks standarts. KML izmanto uz tagiem balstītu struktūru ar ligzdotiem elementiem un atribūtiem. Visi tagi ir reģistrjutīgi, un ir svarīgi ievērot šo tagu secību, kas norādīta [KML](https://developers.google.com/kml/documentation/kmlreference) atsaucē.

## Īsa vēsture ##

KML was originally developed for use with Google Earth which was originally known as Keyhole Earth Viewer. KLM was adopted as international standard in 2008 by the Open Geospatial Consortium in 2008. Tā kā formāts tika izstrādāts izmantošanai programmā Google Earth, tas izceļas ar to, ka tas ir pirmais, kas skatās un rediģē KML failus. Laikam ejot, tagad ir arvien vairāk projektu, kas nodrošina atbalstu KML failu formātiem, tostarp vairākām API dažādās valodās.

## KML faila formāta specifikācijas ##

KML uzziņa ir pilnīga atsauces rokasgrāmata, lai iegūtu visas faila formāta specifikācijas. Standarta KML fails sastāv no:

* Vietas atzīmes

* Aprakstošs HTML vietas atzīmes

* Zemes pārklājumi

* Ceļi

* Daudzstūri


Papildus tiem KML faila uzlabotajā versijā var būt:

* Ģeometrijas stili

* Izcelto ikonu stili

* Ekrāna pārklājumi

* Tīkla saites


Katram KML elementam ir lata garuma informācija, kas nosaka failā esošās informācijas ģeogrāfisko atrašanās vietu. Tomēr var būt arī papildu parametri, piemēram, virziens, augstums un slīpums.

### Vietas atzīmes ###

To izmanto, lai attēlotu pozīciju uz Zemes virsmas, un to identificē ar<Point> elements. Tālāk ir sniegts piemērs, kā vietas atzīme tiek attēlota KML failā.

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

### Aprakstošais HTML vietas atzīmēs ###

Papildinformāciju var saistīt ar vietas atzīmi, kas vēl vairāk uzlabo vietas atzīmes attēlojumu. Šāda informācija ietver saites, fontu izmērus, stilus un krāsas. Turklāt tajā ir iekļauts arī teksta līdzinājums un tabulas, kas ir daļa no vietas atzīmes.

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

### Zemes pārklājumi ###

Tie attēlo attēla slāņošanos uz Zemes virsmas. The<icon> elment satur saiti uz pārklājuma attēla failu.

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

### Ceļi ###

Ceļus pārstāv<LineString> elements, kas ir lat-garu pāru kolekcija. Izmantojot tos, programmā Google Earth var izveidot daudz dažādu veidu ceļus.

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

## Telpiskās atsauces KML failā ##

Informācijai, kas ietverta jebkurā ģeotelpiskajā failā par ģeogrāfiskajām atrašanās vietām, bez telpiskās atsauces informācijas var būt dažādas nozīmes. Pēc noklusējuma KML faila telpiskās atsauces nosaka 1984. gada Pasaules ģeodēziskā sistēma WGS84.

## Atsauces Nr.

* [KML atsauce](https://developers.google.com/kml/documentation/kmlreference)

* [Google izstrādātāja apmācība KML](https://developers.google.com/kml/documentation/kml_tut)

* [KML faila formāts](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)


