{
  "date" : "2021-07-18",
  "keywords" : [ "LOC", "file", "extension", "file format", "GPS Location", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "LOC - GPS Location File Format",
  "description":"Learn about LOC file format and APIs that can create and open LOC files.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2021-07-18"
}

## What is an LOC file?

A file with .loc extension is a GPS location file that contains geospatial locations as waypoints. A waypoint is a pair of Latitude-Longitude values that refers to a location used by Geographical Information System (GIS) applications. GPS mapping programs, such as DeLorme Topo, use LOC files to read and display information contained with these LOC files as selectable layers by end users. In addition, these are used to exchange GPS data between applications. LOC files can be opened using applications such as [TopoGrafix EasyGPS](https://www.easygps.com/) that displays the contents of such files as layers and data plotted on the map at respective geolocation.

## LOC File Format - More Information

LOC files have similarities to [GPX](/gis/gpx/) files but are saved in different format. These are saved as [XML](/web/xml/) files where the content of waypoints and associated information are contained in structured tags. Since XML is a generalized language for exchange of data between different applications, this facilitates the exchange of LOC data with other applications.

## LOC File Format - Example

Following is the header and text of one waypoint from an LOC file. As can be seen, the header information contains the source of location for the data. The waypoint contains information such as the `ID` and associated content data associated with the waypoint. Finally, the waypoint is a collection of latitude and longitude values and the text associated with this particular waypoint.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## References

* [TopGraphic EasyGPS](https://www.easygps.com/)
