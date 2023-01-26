{
  "date" : "2023-01-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MSD File - Map Service Definition File Format",
  "description":"Learn about MSD file format and APIs that can create and open MSD files.",
  "linktitle" : "MSD",
  "menu" : {
    "docs" : {
      "identifier":"gis-msd",
      "parent" : "gis"
    }
  },
  "lastmod" : "2023-01-25"
}

## What is an MSD file?

An MSD file is a Map Service Distribution file created with the GIS mapping software ArcGIS Desktop. It contains the published map exported from a [.mxd](/gis/mxd/) map file. An MSD file contains information about a map service that is hosted on the ArcGIS Server. The hosted map is accessible over the internet for others. MSD file has the map document, layer information and table properties.

## MSD File Format

MSD files are saved to disk in binary file format. These are used by ArcGIS server application to create and manage the map service for hosting purpose. MSD files are also used by ArcMap to connect to the map service and display the contents on the map.

## References

* [Using MXD Templates](https://desktop.arcgis.com/en/arcmap/10.3/map/page-layouts/using-mxd-templates.htm)
