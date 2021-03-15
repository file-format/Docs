{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "KML - Keyhole Markup Language",
  "description":"Learn about KML file format and APIs that can create and open KML files.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a KML file?

KML, Keyhole Markup Language) contains geospatial information in XML notation. Files saved as KML can be opened in Geographic Information System (GIS) applications provided they support it. Many applications have started providing support for KML file format after it has been adopted as international standard. KML uses a tag-based structure with nested elements and attributes. All the tags are case-sensitive and the order of these tags, as per [KML](https://developers.google.com/kml/documentation/kmlreference) Reference, is important to follow.

## Brief History ##

KML was originally developed for use with Google Earth which was originally known as Keyhole Earth Viewer. KLM was adopted as international standard in 2008 by the Open Geospatial Consortium in 2008. Since the format was developed for use with Google Earth, it has the distinction to be the first one to view and edit KML files. With the passage of time, there are now more and more projects that provide support for KML file formats including several APIs in different languages.

## KML File Format Specifications ##

The KML Reference is a complete guide for referring in order to have the full file format specifications. A standard KML file consists of:

* Placemarks
* Descriptive HTMLin Placemarks
* Ground Overlays
* Paths
* Polygons

In addition to these, an advanced version of KML file can have:

* Styles for Geometry
* Styles for Highlighted Icons
* Screen Overlays
* Network Links

Each of the KML element has lat-long information that geo-locates the information present in the file. However, there can be additional parameters as well like heading, altitude and tilt.

### PlaceMarks ###

It is used to represent a position on Earth's surface and is identified by the <Point> element. Following is an example how a placemark is represented in KML file.

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

### Descriptive HTML in Placemarks ###

Additional information can be associated with a placemark that further enhances the representation of the placemark. Such information includes links, font sizes, styles, and colours. In addition, it also includes text alignment and tables to be part of the placemark.

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

### Ground Overlays ###

These represent the layering of an image onto the Earth's surface. The <icon> elment contains the link to the overlay image file.

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

### Paths ###

Paths are represented by <LineString> element that is a collection of lat-long pairs. Using these, many different types of paths can be created in Google Earth.

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

## Spatial Referencing in KML File ##

 Information contained in any Geospatial file about Geo-Locations can have different meanings without spatial referencing information. By default, the spatial referencing of KML file are defined by the World Geodetic System of 1984, WGS84.

## References ##

* [KML Reference](https://developers.google.com/kml/documentation/kmlreference)
* [Google Developer Tutorial for KML](https://developers.google.com/kml/documentation/kml_tut)
* [KML File Format](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)
