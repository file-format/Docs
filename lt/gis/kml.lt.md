{
  "date": "2019-10-11",
  "keywords": [
"kml failą",
"kas yra kml failas",
"failą",
"kml pavyzdys",
"kml failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KML – Keyhole Markup Language",
  "description": "Sužinokite apie KML failo formatą ir API, kurios gali kurti ir atidaryti KML failus.",
  "linktitle": "KML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-ltl"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra KML failas?

KML, Keyhole Markup Language) yra geografinė informacija XML žymėjimu. KML formatu išsaugotus failus galima atidaryti geografinės informacijos sistemos (GIS) programose, jei jos tai palaiko. Daugelis programų pradėjo teikti KML failo formato palaikymą po to, kai jis buvo priimtas kaip tarptautinis standartas. KML naudoja žymomis pagrįstą struktūrą su įdėtais elementais ir atributais. Visose žymose skiriamos didžiosios ir mažosios raidės, todėl svarbu laikytis šių žymų eilės, nurodytos [KML](https://developers.google.com/kml/documentation/kmlreference) nuorodoje.

## Trumpa istorija ##

KML was originally developed for use with Google Earth which was originally known as Keyhole Earth Viewer. KLM was adopted as international standard in 2008 by the Open Geospatial Consortium in 2008. Kadangi formatas buvo sukurtas naudoti su Google žeme, jis pasižymi tuo, kad pirmasis peržiūri ir redaguoja KML failus. Laikui bėgant, atsiranda vis daugiau projektų, kurie palaiko KML failų formatus, įskaitant kelias API skirtingomis kalbomis.

## KML failo formato specifikacijos ##

KML nuoroda yra išsamus vadovas, kaip pateikti nuorodas, norint turėti visas failo formato specifikacijas. Standartinį KML failą sudaro:

* Vietos žymekliai

* Aprašomieji HTML vietos žymekliuose

* Antžeminės perdangos

* Keliai

* Daugiakampiai


Be šių, išplėstinė KML failo versija gali turėti:

* Geometrijos stiliai

* Paryškintų piktogramų stiliai

* Ekrano perdangos

* Tinklo nuorodos


Kiekvienas KML elementas turi plataus ilgio informaciją, kuri geografiškai nustato faile esančią informaciją. Tačiau gali būti ir papildomų parametrų, tokių kaip kursas, aukštis ir posvyris.

### Vietos žymės ###

Jis naudojamas padėčiai Žemės paviršiuje pavaizduoti ir identifikuojamas pagal<Point> elementas. Toliau pateikiamas pavyzdys, kaip vietos žymeklis vaizduojamas KML faile.

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

### Aprašomasis HTML vietos žymekliuose ###

Papildoma informacija gali būti susieta su vietos žymekliu, kuris dar labiau pagerina vietos žymeklio vaizdą. Tokia informacija apima nuorodas, šriftų dydžius, stilius ir spalvas. Be to, jis taip pat apima teksto lygiavimą ir lenteles, kurios yra vietos žymeklio dalis.

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

### Antžeminės perdangos ###

Tai reiškia vaizdo sluoksniavimąsi ant Žemės paviršiaus. The<icon> elment yra nuoroda į perdangos vaizdo failą.

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

### Keliai ###

Takus vaizduoja<LineString> elementas, kuris yra lat-long porų rinkinys. Naudojant juos, Google žemėje galima sukurti daugybę skirtingų kelių.

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

## Erdvinės nuorodos KML faile Nr.

Informacija, esanti bet kuriame geografiniame faile apie geografines vietas, gali turėti skirtingas reikšmes be erdvinės nuorodos informacijos. Pagal numatytuosius nustatymus erdvinę KML failo nuorodą apibrėžia 1984 m. Pasaulinė geodezinė sistema WGS84.

## Nuorodos Nr.

* [KML nuoroda](https://developers.google.com/kml/documentation/kmlreference)

* [KML skirta „Google Developer Tutorial“](https://developers.google.com/kml/documentation/kml_tut)

* [KML failo formatas](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)


