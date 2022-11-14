{
  "date" : "2019-10-11",
  "keywords" :[ "file kml", "che cos'è un file kml", "file", "esempio kml", "estensione file kml", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Linguaggio di markup del buco della serratura",
  "description":"Scopri il formato di file KML e le API che possono creare e aprire file KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file KML?

KML, Keyhole Markup Language) contiene informazioni geospaziali in notazione XML. I file salvati come KML possono essere aperti nelle applicazioni GIS (Geographic Information System) a condizione che lo supportino. Molte applicazioni hanno iniziato a fornire supporto per il formato di file KML dopo che è stato adottato come standard internazionale. KML utilizza una struttura basata su tag con elementi e attributi nidificati. Tutti i tag fanno distinzione tra maiuscole e minuscole e l'ordine di questi tag, come da [KML](https://developers.google.com/kml/documentation/kmlreference) Riferimento, è importante da seguire.

## Breve storia ##

KML è stato originariamente sviluppato per l'uso con Google Earth, originariamente noto come Keyhole Earth Viewer. KLM è stato adottato come standard internazionale nel 2008 dall'Open Geospatial Consortium nel 2008. Poiché il formato è stato sviluppato per l'utilizzo con Google Earth, si distingue per essere il primo a visualizzare e modificare file KML. Con il passare del tempo, ora ci sono sempre più progetti che forniscono supporto per formati di file KML incluse diverse API in diverse lingue.

## Specifiche del formato file KML ##

Il riferimento KML è una guida completa per fare riferimento al fine di avere le specifiche complete del formato di file. Un file KML standard è costituito da:

* Segnaposto
* HTML descrittivo in segnaposto
* Sovrapposizioni di terra
* Percorsi
* Poligoni

Oltre a questi, una versione avanzata del file KML può avere:

* Stili per la geometria
* Stili per icone evidenziate
* Sovrapposizioni dello schermo
* Collegamenti di rete

Ciascuno degli elementi KML ha informazioni lat-long che geo-localizza le informazioni presenti nel file. Tuttavia, possono esserci parametri aggiuntivi come direzione, altitudine e inclinazione.

### Segnaposto ###

È usato per rappresentare una posizione sulla superficie terrestre ed è identificato dal<Point> elemento. Di seguito è riportato un esempio di come viene rappresentato un segnaposto nel file KML.

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

### HTML descrittivo nei segnaposto ###

Ulteriori informazioni possono essere associate a un segnaposto che migliora ulteriormente la rappresentazione del segnaposto. Tali informazioni includono collegamenti, dimensioni dei caratteri, stili e colori. Inoltre, include anche l'allineamento del testo e le tabelle da inserire nel segnaposto.

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

### Sovrapposizioni di terra ###

Questi rappresentano la stratificazione di un'immagine sulla superficie terrestre. Il<icon> elment contiene il collegamento al file di immagine sovrapposto.

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

### Percorsi ###

I percorsi sono rappresentati da<LineString> elemento che è una raccolta di coppie lat-long. Utilizzando questi, è possibile creare molti diversi tipi di percorsi in Google Earth.

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

## Riferimento spaziale nel file KML ##

Le informazioni contenute in qualsiasi file geospaziale sulle geolocalizzazioni possono avere significati diversi senza informazioni di riferimento spaziale. Per impostazione predefinita, i riferimenti spaziali del file KML sono definiti dal World Geodetic System del 1984, WGS84.

## Riferimenti ##

* [Riferimento KML](https://developers.google.com/kml/documentation/kmlreference)
* [Esercitazione per sviluppatori Google per KML](https://developers.google.com/kml/documentation/kml_tut)
* [Formato file KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

