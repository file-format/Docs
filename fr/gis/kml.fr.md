{
  "date" : "2019-10-11",
  "keywords" :[ "fichier kml", "qu'est-ce qu'un fichier kml", "fichier", "exemple kml", "extension de fichier kml","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Langage de balisage Keyhole",
  "description":"En savoir plus sur le format de fichier KML et les API qui peuvent créer et ouvrir des fichiers KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier KML ?

KML, Keyhole Markup Language) contient des informations géospatiales en notation XML. Les fichiers enregistrés au format KML peuvent être ouverts dans des applications de système d'information géographique (SIG) à condition qu'elles le prennent en charge. De nombreuses applications ont commencé à prendre en charge le format de fichier KML après son adoption en tant que norme internationale. KML utilise une structure basée sur des balises avec des éléments et des attributs imbriqués. Toutes les balises sont sensibles à la casse et il est important de suivre l'ordre de ces balises, conformément à la référence [KML](https://developers.google.com/kml/documentation/kmlreference).

## Bref historique ##

KML a été développé à l'origine pour être utilisé avec Google Earth, qui était à l'origine connu sous le nom de Keyhole Earth Viewer. KLM a été adopté comme norme internationale en 2008 par l'Open Geospatial Consortium en 2008. Depuis que le format a été développé pour être utilisé avec Google Earth, il a la particularité d'être le premier à afficher et éditer des fichiers KML. Au fil du temps, de plus en plus de projets prennent en charge les formats de fichiers KML, y compris plusieurs API dans différentes langues.

## Spécifications du format de fichier KML ##

La référence KML est un guide complet de référence afin d'avoir les spécifications complètes du format de fichier. Un fichier KML standard se compose de :

* Repères
* Repères HTML descriptifs
* Superpositions au sol
* Chemins
* Polygones

En plus de ceux-ci, une version avancée du fichier KML peut avoir :

* Styles de géométrie
* Styles pour les icônes en surbrillance
* Superpositions d'écran
* Liens réseau

Chacun des éléments KML contient des informations lat-long qui géolocalisent les informations présentes dans le fichier. Cependant, il peut également y avoir des paramètres supplémentaires comme le cap, l'altitude et l'inclinaison.

### PlaceMarks ###

Il est utilisé pour représenter une position sur la surface de la Terre et est identifié par le<Point> élément. Voici un exemple de représentation d'un repère dans un fichier KML.

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

### HTML descriptif dans les repères ###

Des informations supplémentaires peuvent être associées à un repère qui améliore encore la représentation du repère. Ces informations incluent les liens, les tailles de police, les styles et les couleurs. En outre, il inclut également l'alignement du texte et des tableaux pour faire partie du repère.

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

### Superpositions au sol ###

Ceux-ci représentent la superposition d'une image sur la surface de la Terre. La<icon> L'élément contient le lien vers le fichier image de superposition.

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

### Chemins ###

Les chemins sont représentés par<LineString> élément qui est une collection de paires lat-long. Grâce à ceux-ci, de nombreux types de chemins différents peuvent être créés dans Google Earth.

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

## Référencement spatial dans le fichier KML ##

Les informations contenues dans tout fichier géospatial sur les géolocalisations peuvent avoir différentes significations sans informations de référencement spatial. Par défaut, le référencement spatial du fichier KML est défini par le World Geodetic System de 1984, WGS84.

## Références ##

* [Référence KML](https://developers.google.com/kml/documentation/kmlreference)
* [Tutoriel de développement Google pour KML](https://developers.google.com/kml/documentation/kml_tut)
* [Format de fichier KML] (https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

