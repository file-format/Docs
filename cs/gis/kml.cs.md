{
  "date" : "2019-10-11",
  "keywords" :[ "soubor kml", "co je soubor kml", "soubor", "příklad kml", "přípona souboru kml", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Keyhole Markup Language",
  "description":"Další informace o formátu souboru KML a rozhraních API, která mohou vytvářet a otevírat soubory KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor KML?

KML, Keyhole Markup Language) obsahuje geoprostorové informace v notaci XML. Soubory uložené jako KML lze otevřít v aplikacích geografického informačního systému (GIS), pokud to podporují. Mnoho aplikací začalo poskytovat podporu pro formát souborů KML poté, co byl přijat jako mezinárodní standard. KML používá strukturu založenou na značkách s vnořenými prvky a atributy. Všechny značky rozlišují velká a malá písmena a je důležité dodržovat pořadí těchto značek podle [KML](https://developers.google.com/kml/documentation/kmlreference) reference.

## Stručná historie ##

KML byl původně vyvinut pro použití s aplikací Google Earth, která byla původně známá jako Keyhole Earth Viewer. KLM byl přijat jako mezinárodní standard v roce 2008 konsorciem Open Geospatial Consortium v roce 2008. Vzhledem k tomu, že formát byl vyvinut pro použití s aplikací Google Earth, má tu výhodu, že je prvním, kdo prohlíží a upravuje soubory KML. S postupem času nyní existuje stále více projektů, které poskytují podporu pro formáty souborů KML včetně několika rozhraní API v různých jazycích.

## Specifikace formátu souboru KML ##

Referenční příručka KML je úplný průvodce odkazem, abyste získali úplné specifikace formátu souboru. Standardní soubor KML se skládá z:

* Značky míst
* Popisné HTMLin značky míst
* Překryvy země
* Cesty
* Polygony

Kromě toho může mít pokročilá verze souboru KML:

* Styly pro geometrii
* Styly pro zvýrazněné ikony
* Překrytí obrazovky
* Síťové odkazy

Každý prvek KML obsahuje informace o zeměpisné délce, které geograficky lokalizují informace přítomné v souboru. Mohou však existovat další parametry, jako je kurz, nadmořská výška a sklon.

### Značky místa ###

Používá se k reprezentaci polohy na zemském povrchu a je identifikován<Point> živel. Následuje příklad, jak je značka místa reprezentována v souboru KML.

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

### Popisný kód HTML ve značkách míst ###

Ke značce místa lze přiřadit další informace, které dále vylepšují reprezentaci značky místa. Tyto informace zahrnují odkazy, velikosti písma, styly a barvy. Kromě toho také zahrnuje zarovnání textu a tabulky, které mají být součástí značky místa.

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

### Překryvy země ###

Ty představují vrstvení obrazu na zemský povrch. The<icon> prvek obsahuje odkaz na soubor překryvného obrázku.

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

### Cesty ###

Cesty jsou reprezentovány<LineString> prvek, který je sbírkou párů šířky a délky. Pomocí nich lze v aplikaci Google Earth vytvořit mnoho různých typů cest.

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

## Prostorové odkazy v souboru KML ##

Informace obsažené v jakémkoli Geoprostorovém souboru o Geo-Locations mohou mít různý význam bez prostorových referenčních informací. Ve výchozím nastavení jsou prostorové odkazy souboru KML definovány světovým geodetickým systémem z roku 1984, WGS84.

## Reference ##

* [Reference KML](https://developers.google.com/kml/documentation/kmlreference)
* [Výukový program pro vývojáře Google pro KML](https://developers.google.com/kml/documentation/kml_tut)
* [Formát souboru KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

