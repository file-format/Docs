{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SHP - ESRI Shapefile",
  "description":"Learn about SHP file format and APIs that can create and open SHP files.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a SHP file?

SHP is the file extension for one of the primary file types used for representation of ESRI Shapefile. It represents Geospatial information in the form of vector data to be used by Geographic Information Systems (GIS) applications. The format has been developed as open specifications in order to facilitate interoperability between ESRI and other software products.

## Data Representation ##

As mentioned, a shapefile format describes geospatial information of a data set as vector features. These vector features include:

* points
* lines
* polygons

These features in combination can represent almost any type of shapes like water wells, country boundaries, spatial points, rivers flow, lakes, etc. Each vector feature can have attributes that actually define the purpose of that feature. For example, a shapefile containing cities of Los Angeles can have city name and temperature as attributes which gives meaningful representation to the spatial data.

## Associated Files ##

A standalone shp file can not be used by software applications to make meaning of the data it contains. In order to make sense of the information contained in such a file, a shapefile makes use of following additional mandatory files.

* shx file - index file
* dbf file - a dBASE file that stores all the attributes of the shapes in the main file
* prj file - stores project information of the file

There can be other optional files as well that share the same name as the main file.

## File Format Specifications ##

Open specifications of shapefile are available online from ESRI in the form of [Technical Description](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) and elaborates the overall structure of the file in detail. Information in main .shp file consists of headers and records. The fixed-length file header is followed by variable-length records where every record is made up of a fixed-length record header followed by variable-length record contents.

### Main File Header ###

The main File Header starts from the beginning of the file and is 100 bytes in length.  Organization of this main file header along with byte position, value, type and byte order is as shown in the following table.


|Bytes|Field|Value|Type|Byte Order
---|---|---|---|---|
|0-3|File Code|9994|Integer|Big Endian
|4-23|Unused|0|Integer|Big Endian
|24-27|File Length|File Length|Integer|Big Endian
|28-31|Version|1000|Integer|Little Endian
|32-35|Shape Type|Shape Type|Integer|Little Endian
|36-67|Minimum Bounding Rectangle|Xmin, Ymin, Xmax and Ymax|double|Little Endian
|68-83|Bounding Box|Zmin, Zmax|double|Little Endian
|84-99|Bounding Box|Mmin, Mmax|double|

It is to be noted that the value of file length is the total length of the file in 16-bit words which also includes the fifty 16-bit words making up the header.

#### Shape Types ####

The values of shape types field in above table are as follow:


|Value|Shape Type
---|---|
|0|Null Shape
|1|Point
|3|Polyline
|5|Polygon
|8|MultiPoint
|11|PointZ
|13|PolyLineZ
|15|PolygonZ
|18|MultiPointZ
|21|PointM
|23|PolyLineM
|25|PolygonM
|28|MultiPointM
|31|MultiPatch

### Data Records ###

The main file header is followed by variable length records where each record consists of a fixed-length record header followed by variable-length record contents.

#### Record Header ####

Record header contains information about the record number and content length of the record in a fixed length of 8 bytes. The organization of record header is as shown follow:


|Bytes|Field|Value|Type|Byte Order
---|---|---|---|---|
|0-3|Record Number|Record Number|Integer|Big
|4-7|Record Length|Record Length|Integer|Big

#### Record Contents ####

A shapefile record contents consist of a shape type followed by the geometric data for that shape. A shape type of 0 represents a null shape that has no geometric data for the shape. The length of the record contents is reflection of the shape parts and vertices. Lets take an example of Point Shape type to elaborate how a record contains information about such a shape type.

A point represents a certain geographic location in the order X,Y where each coordinate is represented by a double-precision value. Following table shows the arrangement of a Point shape type.


|Bytes|Shape Type|Value|Type|Number|Byte Order
---|---|---|---|---|---|
|0-3|Shape Type|1|Integer|1|Little
|4-11|X|X|double|1|Little
|12-19|Y|Y|double|1|Little

Examples of other shape types can be found the ESRI technical description document.

## References ##

* [ESRI Shapefile Technical Description](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) by ESRI
