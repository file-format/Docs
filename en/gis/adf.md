{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ADF - ESRI ArcInfo Binary Grid Format",
  "description":"Learn about ADF file format and APIs that can create and open ADF files.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
    }
  },
  "lastmod" : "2021-08-26"
}

## What is a ADF file?

A file with .adf extension is a raster data file format used by ESRI software applications such as ArcGIS, ArcView, and ArcInfo. Spatial data is stored as a binary grid that is native to ESRI. The grid is made up of rows and columns of cells that can be integer as well as floating point. Integer grids in an ADF file represent discrete data and floating-point grids represent continuous data. Another popular ESRI file format is [SHP](/gis/shp/) file that represents Geospatial information in the form of vector data to be used by Geographic Information Systems (GIS) applications.

## ADF File Format - More Information

ADF files are saved as binary files to disc in a binary grid. Integer grids have attributes that are stored in a value attribute table (VAT). Each unique value in the grid has one record in VAT where the record stores the unique value and the number of cells in the grid is represented by that value.

Floating point grids do not have a VAT.

### Grid Structure

Inside ADF file, grids are implemented using a tiled raster data structure. The basic unit inside this raster data structure is a rectangular block of cells. Each block is stored on disc and compressed in a variable-length file structure, called a tile. Each block is stored as one variable-length record.

GRID rasters are stored in workspaces, where a workspace contains one info subdirectory and a subdirectory for each GRID. There are several files that geographic location and attribute data for the corresponding grid. The Info subdirectory contains several files which maintain certain information about the GRID and other datasets, such as coverages, in the workspace.

## References ##

* [ESRI Grid Format](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)

