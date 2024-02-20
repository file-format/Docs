{
  "date": "2022-12-07",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "DT0 File - DTED Level 0 File Format",
  "description": "Learn about DT0 file format and APIs that can create and open DT0 files.",
  "linktitle": "DT0",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dt0"
    }
  },
  "lastmod": "2022-12-07"
}

## What is a DT0 file?

A DT0 file is a Digital Terrain Elevation Data (DTED) file that contains Level 0 information to study terrain elevation data. Elevation data is uniformly spaced in a DT0 file and can be read by popular GIS programs such as ESRI ArcGIS Pro, TatukGIS, Blue Marble Geographic Global Mapper, and Pitney Bowes MapInfo. DT0 files are mostly used by scientific and technical communities to study the slope, elevation, and surface roughness of global terrains.

DT0 file format is similar to [DT1](/gis/dt1/) and [DT2](/gis/dt2/) file types but with less granularity.

### DT0 File Format

DT0 files are save as binary files to disc. These can be read using many GIS applications. DT0 files can be merged into a File Geodatabase Raster Catalog that can be used to create one big mosaic.

## How to Convert Raster to DTED files?

There are multiple tools that can convert Raster to DTED files. [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm) is one such tool that can be convert Raster to DTED.

## References

 * [ArgGIS Pro](https://pro.arcgis.com/en/pro-app/latest/tool-reference/data-management/raster-to-dted.htm)
 * [KML File Format](/gis/kml/)
