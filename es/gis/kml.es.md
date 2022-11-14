{
  "date" : "2019-10-11",
  "keywords" :[ "archivo kml", "qué es un archivo kml", "archivo", "ejemplo de kml", "extensión de archivo kml","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Lenguaje de marcado de ojo de cerradura",
  "description":"Obtenga información sobre el formato de archivo KML y las API que pueden crear y abrir archivos KML",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo KML?

KML, Keyhole Markup Language) contiene información geoespacial en notación XML. Los archivos guardados como KML se pueden abrir en las aplicaciones del Sistema de Información Geográfica (GIS), siempre que lo admitan. Muchas aplicaciones han comenzado a admitir el formato de archivo KML después de que se haya adoptado como estándar internacional. KML utiliza una estructura basada en etiquetas con elementos y atributos anidados. Todas las etiquetas distinguen entre mayúsculas y minúsculas y es importante seguir el orden de estas etiquetas, según [KML](https://developers.google.com/kml/documentation/kmlreference) Referencia.

## Breve historia ##

KML se desarrolló originalmente para su uso con Google Earth, que originalmente se conocía como Keyhole Earth Viewer. KLM fue adoptado como estándar internacional en 2008 por el Open Geospatial Consortium en 2008. Dado que el formato se desarrolló para su uso con Google Earth, tiene la distinción de ser el primero en ver y editar archivos KML. Con el paso del tiempo, ahora hay más y más proyectos que brindan soporte para formatos de archivo KML que incluyen varias API en diferentes idiomas.

## Especificaciones del formato de archivo KML ##

La referencia de KML es una guía completa para hacer referencia con el fin de tener las especificaciones completas de formato de archivo. Un archivo KML estándar consta de:

* Marcas de posición
* HTML descriptivo en marcas de posición
* Superposiciones de tierra
* Caminos
* Polígonos

Además de estos, una versión avanzada del archivo KML puede tener:

* Estilos para Geometría
* Estilos para iconos resaltados
* Superposiciones de pantalla
* Enlaces de red

Cada uno de los elementos KML tiene información de latitud y longitud que geolocaliza la información presente en el archivo. Sin embargo, puede haber parámetros adicionales, como rumbo, altitud e inclinación.

### Marcas de lugar ###

Se utiliza para representar una posición en la superficie de la Tierra y se identifica por el<Point> elemento. El siguiente es un ejemplo de cómo se representa una marca de posición en un archivo KML.

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

### HTML descriptivo en marcas de posición ###

Se puede asociar información adicional con una marca de posición que mejora aún más la representación de la marca de posición. Dicha información incluye enlaces, tamaños de fuente, estilos y colores. Además, también incluye alineación de texto y tablas para que formen parte de la marca de posición.

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

### Superposiciones de suelo ###

Estos representan la superposición de una imagen en la superficie de la Tierra. los<icon> El elemento contiene el enlace al archivo de imagen de superposición.

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

### Caminos ###

Los caminos están representados por<LineString> elemento que es una colección de pares lat-long. Con estos, se pueden crear muchos tipos diferentes de rutas en Google Earth.

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

## Referencia espacial en archivo KML ##

La información contenida en cualquier archivo Geoespacial sobre Geolocalizaciones puede tener diferentes significados sin información de referencia espacial. De forma predeterminada, la referencia espacial del archivo KML está definida por el Sistema Geodésico Mundial de 1984, WGS84.

## Referencias ##

* [Referencia KML](https://developers.google.com/kml/documentation/kmlreference)
* [Tutorial para desarrolladores de Google para KML](https://developers.google.com/kml/documentation/kml_tut)
* [Formato de archivo KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

