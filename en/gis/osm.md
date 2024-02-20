{
  "date": "2019-10-11",
  "keywords": [
    "osm file",
    "what is an osm file",
    "file",
    "osm example",
    "osm file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "OSM - OpenStreetMap File Format",
  "description": "Learn about OSM file format and APIs that can create and open OSM files.",
  "linktitle": "OSM",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-osm"
    }
  },
  "lastmod": "2019-09-10"
}

## What is an OSM file?

OpenStreetMap (OSM) is a huge collection of volunteered geographic information stores in different types of files, using different encoding schemes to convert this data into bits and bytes. OSM is a collaborative effort toward the creation of a free editable map of the world.  The primary output of this collaborative effort is geographic data rather than the map itself. The constraints on the use or availability of geographic information across much of the world triggers the need to create an OSM. 

The data available from OSM is ready to replace Google Maps for classical applications (Facebook, Craigslist etc.) and default data for GPS receiver’s applications.Although data quality is diverse across the world yet OpenStreetMap data can be conveniently compared with patent data sources.

## Brief History of OSM File Format

Inspired by the success of Wikipedia, in 2004, Steve Coast a British entrepreneur, created this community-based world mapping project in the UK. He initially focused on mapping the United Kingdom. OpenStreetMap Foundation was first established in April 2006 to support the evolution, expansion, and circulation of free geospatial for anybody. In December 2006, Yahoo aided OpenStreetMap with its aerial photography for map production.

Complete road data for the Netherlands and trunk road data for India and China was contributed to OSM in April 2007 by Automotive Navigation Data (AND). In December 2007, Oxford University was the most prominent organization who integrated OpenStreetMap data within their main website. Since then, over 2 million registered users contribute data in this project using GPS devices, aerial photography, and manual surveys. This community contributed data is made available under the Open Database License. An England registered, non-profit organization OpenStreetMap Foundation maintained the OSM site.

## OSM File Format

There are lot of ways and file formats to store geographic data but **OSM** file format is restricted to OpenStreetMap. OSM is especially designed standard format intended to be transported easily across the internet. A structured ordered format, coded in XML constitute .osm file. In OpenStreetMap there are four pivot elements to store topological data structure:

{{< figure src="../OSM.png" alt="OSM File Format" >}}


|Nodes|Ways|Relations|Tags
---|---|---|---|
|<ul><li> Represents geographic position stored as pairs of a latitude and a longitude.</li> <li> Used to represent map features without a size, such as mountain peaks.</li></ul>|<ul><li> Sorted lists of nodes, signifying a polyline, or a polygon</li> <li>Represent linear features such as roads and rivers, and zones, like parking areas jungles, and parks.</li></ul>|<ul><li> Sorted lists of nodes and ways represent their relation like barriers and u turns on roads, motorways span different existing ways and areas with holes.</li></ul>|<ul><li> Store metadata about the map objects.*  Always attached to any node, way or a relation</li></ul>


Tags are used to characterize on ground physical features (buildings and roads etc.) in OpenStreetMap. Each tag relates a geographic characteristic of the feature represented by that specific node or relation. In this free tagging system, to describe a feature, unlimited number of attributes can be included in a map. Specific key and value combinations endorsed by registered users act as informal standards for the frequent used tags. However, new tags can be created whenever new aspects require to analyze previously unmapped attributes of the features. Most features use only a small number of tags for description.

Three types of files are used by OSM to store its main data.

OSM handles all these files with the information about their formatting details. But same internal objects are produced by these files. For data files the visible flag on OSM objects is always true which is not the case for history and change files.

In common use, there is a diversity in OSM file formats. File formats define the content encoding on disk or wire in bits and bytes. OSM is capable of read and write maximum of these formats.

**XML**

The original OSM format is XML-based. The return data of main OSM database API is in XML format.

**PBF**

Protocol Buffers encoding stand on binary format and one of the most compact format.

**O5M/O5C**

Binary format based simpler format but relatively less used. OSM can read but cannot write this format.

**OPL**

A simple format proposed to use with standard UNIX command line tools. Close to CSV-files, allows one OSM entity on one line.

**DEBUG**

A text-based format intended to create for debugging. The OSM can write this format but cannot read.

**BLACKHOLE**

A dummy format that dispose of all data. The OSM can write this format but cannot read.

## OSM Data Storage ##

OSM's main **PostgreSQL** database keeps the main copy of the OSM data with PostGIS extension. For each data primitive, main database maintains a table whose rows store individual objects. All edits update this database and all other formats are formed using this database. Numerous downloadable database pools are created to transfer data from one place to another. Two formats, one using XML and other using Protocol Buffer Binary Format (PBF) define these pools. The complete data is stored in a file called planet.osm

## Compression in OSM Files ##

Text-based formats (XML, OPL, and Debug) use gzip or bzip2 compression optionally.

## References ##

* [OSM file Formats Manual](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Learn OSM](https://learnosm.org/en/osm-data/getting-data/)
