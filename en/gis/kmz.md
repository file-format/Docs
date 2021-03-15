{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "KMZ - KML Zipped File Format",
  "description":"Learn about KMZ file format and APIs that can create and open KMZ files.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a KMZ file?

KMZ (KML Zipped) file is a representation of zipped [KML](/gis/kml/) file that contains geospatial information viewable in GIS applications like Google Earth. Information about placemarks is represented in the file as latitude and longitude along with a custom name. The single packaged KMZ file can be shared with other users easily. KMZ files can include 3D model data as well for geo-representation of the model. A KMZ file can be opened in Google Maps by saving the file to an online location and then typing the URL in the Google Maps Search box.

## File Structure ##

The contents of a MKZ file consist of a main KML file and zero or more associated files. It can be extracted using standard decompression utility like WinZIP. KMZ file format is also compressed to an archive with compression ratio of 10:1. You can export data from Google Earth like applications directly to KMZ file format. The main KML file is named **doc.kml**. While packaging a KMZ file, more than one KML files can be added to it, but this will be of no benefit as Google Earth searches for the first KML file when opening the KMZ file and reads it. It ignores any further KML files found in the archive. In order to be sure that the desired KML file is read by Google Earth, only a single KML file is recommended to be placed inside the KMZ file.

The images, models, textures, sound files and other resources referenced in the doc.kml file are placed in another subfolder inside the main folder. This may involve some complexity as well depending upon the number of supporting files. Links to these constituent resources can be reference relatively or via absolute referencing.

### Relative Referencing ###

When resources are placed alongside the main doc.kml inside a sub-folder within the main folder, the relative referencing can point to these supporting files as shown in the following example (for icon only).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Absolute Referencing ###

Resources can be referenced absolutely as well. Absolute references contain the full URL for the linked file. When files are posted on a central server, absolute referencing makes it sure that these remain unambiguous as compared to relative referencing. Local file are not recommended to be referenced absolutely as these links will break when the files are moved to a new system. An example of absolute referencing is as follow:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## See Also ##

* [GeoJSON](/gis/geojson/)

## References ##

* [Google Earth and KMZ Files](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)
