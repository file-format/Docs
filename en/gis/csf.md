{
  "date" : "2023-01-27",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CSF File - GeoMedia Coordinate System File Format",
  "description":"Learn about CSF file format and APIs that can create and open CSF files.",
  "linktitle" : "CSF",
  "menu" : {
    "docs" : {
      "identifier":"gis-csf",
      "parent" : "gis"
    }
  },
  "lastmod" : "2023-01-27"
}

## What is an CSF file?

A CSF file is a Coordinate System File that contains information about the coordinate system of a GIS file. It is used by Intergraph's GeoMedia software to define the parameters of a particular coordinate system. These include information parameters such as datum, projection, and units of measurement. This information is used to produce maps for the output data that does not have a coordinate system in place. This information is used by GeoMedia to correctly display and manipulate geographic data in the correct coordinate system.

## CSF File Format

CSF files are stored as text file with details of the geographic coordinate system. GeoMedia allows importing geographic information files from input data that has no coordinate systems defined. Using the projection and coordinate system, GIS systems display the map file with exact values. A CSF file is created at the same location as the output file.

## References

* [How do you correctly display or serve shapefile data into GeoMedia?](https://supportsi.hexagon.com/help/s/article/How-do-you-correctly-display-or-serve-shapefile-data-into?language=en_US)
