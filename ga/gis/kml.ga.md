{
  "date": "2019-10-11",
  "keywords": [
"comhad kml",
"cad is comhad kml ann",
"comhad",
"sampla kml",
"síneadh comhad kml",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KML - Teanga Mharcála Eochrach",
  "description": "Foghlaim faoi fhormáid comhaid KML agus APIanna ar féidir leo comhaid KML a chruthú agus a oscailt.",
  "linktitle": "KML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-gal"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad KML ann?

KML, Keyhole Markup Language) tá eolas geospásúil i nodaireacht XML. Is féidir comhaid a shábháiltear mar KML a oscailt i bhfeidhmchláir an Chórais Faisnéise Geografaí (GIS) ar an gcoinníoll go dtacaíonn siad leis. Thosaigh go leor feidhmchlár ag tabhairt tacaíochta d'fhormáid comhaid KML tar éis glacadh leis mar chaighdeán idirnáisiúnta. Úsáideann KML struchtúr clibe-bhunaithe le heilimintí neadaithe agus tréithe. Tá na clibeanna go léir cás-íogair agus tá sé tábhachtach ord na gclibeanna seo, de réir Tagairt [KML](https://developers.google.com/kml/documentation/kmlreference), a leanúint.

## Stair Ghearr ##

KML was originally developed for use with Google Earth which was originally known as Keyhole Earth Viewer. KLM was adopted as international standard in 2008 by the Open Geospatial Consortium in 2008. Ó forbraíodh an fhormáid le húsáid le Google Earth, tá an t-idirdhealú ann gurb í an chéad cheann a bhreathnaíonn agus a chuirfidh in eagar comhaid KML. Le himeacht ama, tá níos mó agus níos mó tionscadal ann anois a sholáthraíonn tacaíocht d’fhormáidí comhaid KML lena n-áirítear roinnt API i dteangacha éagsúla.

## Sonraíochtaí Formáid Chomhaid KML ##

Is treoir iomlán é an Tagairt KML chun tagairt a dhéanamh ionas go mbeidh na sonraíochtaí iomlána formáid comhaid ann. Is éard atá i gcomhad caighdeánach KML:

* Placemarks

* Placemarks HTMLin Tuairisciúla

* Forleagain Talún

* Cosáin

* Polagáin


Chomh maith leo seo, is féidir le leagan ardleibhéil de chomhad KML:

* Stíleanna do Chéimseata

* Stíleanna do Dheilbhíní Aibhsithe

* Forleagain Scáileáin

* Naisc Líonra


Tá faisnéis lat-fada i ngach eilimint KML a geo-aimsíonn an fhaisnéis atá sa chomhad. Mar sin féin, is féidir paraiméadair bhreise a bheith ann chomh maith le ceannteideal, airde agus tilt.

###Marcanna Áit ###

Úsáidtear é chun suíomh ar dhromchla an Domhain a léiriú agus sainaithnítear é ag an<Point> eilimint. Seo a leanas sampla den chaoi a léirítear áitmharc i gcomhad KML.

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

### HTML Tuairisciúil in Áitmharcanna ###

Is féidir faisnéis bhreise a cheangal le hionadmharc a chuireann tuilleadh le léiriú an logainm. Áirítear le faisnéis dá leithéid naisc, clómhéid, stíleanna agus dathanna. Ina theannta sin, cuimsíonn sé ailíniú téacs agus táblaí le bheith mar chuid den logainm.

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

### Forleagan Talún ###

Léiríonn siad seo leagan íomhá ar dhromchla an Domhain. Tá an<icon> tá nasc chuig an gcomhad íomhá forleagan sa eilimint seo.

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

### cosáin ###

Tá cosáin léirithe ag<LineString> eilimint atá ina bhailiúchán de phéirí lat-fada. Agus iad seo á n-úsáid, is féidir go leor cineálacha éagsúla cosán a chruthú in Google Earth.

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

## Spástagairt i gComhad KML ##

Is féidir le bríonna éagsúla a bheith ag faisnéis atá in aon chomhad Geospásúil faoi Gheo-shuímh gan faisnéis tagartha spáis. De réir réamhshocraithe, sainmhínítear tagairt spásúil an chomhaid KML ag Córas Geodasaí an Domhain 1984, WGS84.

## Tagairtí ##

* [Tagairt KML] ( https://developers.google.com/kml/documentation/kmlreference )

* [Teagasc Forbróra Google le haghaidh KML](https://developers.google.com/kml/documentation/kml_tut)

* [Formáid Chomhaid KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)


