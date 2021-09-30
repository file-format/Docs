{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SBN - ESRI Spatial Index Binary File",
  "description":"Learn about SBN file format and APIs that can create and open SBN files.",
  "linktitle" : "SBN",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2021-09-29"
}

## What is an SBN file?

A file with .sbn extension is a spatial index file that comes associated with the ESRI ArcGIS [.shp](/gis/shp/) file. It is used to optimize spatial queries when an index has been performed on the data. The other file type used alongside .sbn is .sbx file. The SBN and SBX files together make up a shape index to speed up spatial queries. SBN files are optional and can be opened with [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview).

## SBN File Format - More Information

SBN files are stored to disc as binary files and their internal file format details are not available. These store the binary representation of a SHP file for spatial queries. The SBX index file is used alongside the SBN files for speeding up the spatial queries on shapefiles.

## References

* [ESRI ShapeFile Technical Description](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf)
* [ESRI ArcGIS Pro](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview)
