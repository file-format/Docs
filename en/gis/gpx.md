{
  "date" : "2019-10-11",
  "keywords" : [ "gpx file", "what is an gpx file", "file", "gpx example", "gpx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "GPX - GPX Exchange File Format",
  "description":"Learn about GPX file format and APIs that can create and open GPX files.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a GPX file?

Files with GPX extension represent GPS Exchange format for interchange of GPS data between applications and web services on the internet. It is a light-weight XML file format that contains GPS data i.e. waypoints, routes and tracks to be imported and red by multiple programs. GPX file format is open and is supported by variety of applications and GPS devices. GPS data from such files can be loaded for display on mapping applications for geo-spatial purposes.

## GPX File Format ##

A GPX file consists of latitude and longitude location data, elevation values and other possibly other descriptive information. Location data is expressed as decimal degrees and elevation is expressed in meters. Time in a GPX file is are in Coordinated Universal Time (UTC) using ISO 8601 format. The benefits of using a GPX file are as follow:

* GPX allows you to exchange data with a growing list of programs for Windows, MacOS, Linux, Palm, and PocketPC.
* GPX can be transformed into other file formats using a simple webpage or converter program.
* GPX is based on the XML standard, so many of the new programs you use (Microsoft Excel, for example) can read GPX files.
* GPX makes it easy for anyone on the web to develop new features which will instantly work with your favourite programs.

The [GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) shows the representation fo GPX file format for reference.

### Essential Data ###

Following is essential data that is part of a GPX file for representation of GPS data.

* **Waypoints**:  A waypoint is a WGS84 (GPS) coordinates of a point and represent layer of features of OGR type wkbPoint
* **Routes**: Represent a layer of features of OGR type wkbLineString. It includes a list of track points, which are waypoints showing a turn or stage points which lead to a destination
* **Tracks**: Tracks represent layer of features of OGR type wkbMultiLineString. It is made of at least one segment containing waypoints in an ordered list of points describing a path. It consists of a list of track points which represent a continuous GPS track.

### GPX Example File ###

The following GPX file shows the organization of GPS data in a GPX file and can give a good idea about the contents of a GPX file.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## References ##

* [GPX File Format](https://www.topografix.com/gpx.asp)
* [GPX - By Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)
