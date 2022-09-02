{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CPG File Format - ESRI Code Page File",
  "description":"Learn about CPG file format and APIs that can create and open CPG files.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
    }
  },
  "lastmod" : "2022-09-01"
}

## What is a CPG file?

A CPG file is an optional file required the ESRI Shapefile that is used to specify the codepage for identifying the character set to be used. These are stored in plain text file format and contains information about the encoding applied for creating the shapefile. In case a CPG file is not available, then the shapefile uses the system default encoding. A CPG file, if present, must have the same prefix as that of the [SHP](/gis/shp/) file, for exmaple, roads.shp, roads.cpg.

CPG files can be opened with ESRI ArcGIS Pro.

### CPG File Format - More information

When viewing a shapefile in ArcCatalog or any other ArcGIS application, you only see the shapefile. But in reality, shapefile uses other associated files that are read alongside the main shape file. The CPG file is also one of these if it is present alongside the main SHP file.

## References

 * [Shapefile file extensions
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)
