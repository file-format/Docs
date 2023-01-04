{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SDF File - Spatial Data Format File",
  "description":"Learn about SDF file format and APIs that can create and open SDF files.",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "identifier":"gis-sdf",
      "parent" : "gis"
    }
  },
  "lastmod" : "2021-09-29"
}

## What is an SDF file?

A Spatial Data File (SDF) is a Geodatabase file format that was developed by Autodesk. It stores geospatial data and is used by Autodesk GIS program MapGuide and AutoCAD Map 3D. SDF file format is based on the single file database file format SQLite3. It is considered as an optimized file format for large datasets of spatial information.

You can open an SDF file using Autodesk AutoCAD Map 3D 2022 and Autodesk AutoCAD Civil 3D 2023.

## SDF File Format - More Information

SDF file format are stored to disc as binary files. It is based on the SQLite database that utilizes low-level storage components for binary serialization of data. An SDF file contains multiple feature classes per file and multiple geometry properties for each feature class. Data in an SDF file is accessible at high speed due to indexing of each geometry property using an R-tree.

## References

* [SDF Data Format](https://en.wikipedia.org/wiki/Spatial_Data_File)
* [Importing Autodesk SDF](http://docs.autodesk.com/CIV3D/2013/ENU/index.html?url=filesMAPC3D/GUID-EC7140D6-F14F-4F7B-B431-FF0BAD7AE86C.htm,topicNumber=MAPC3Dd30e43012)
