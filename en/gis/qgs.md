{
  "date": "2019-10-11",
  "keywords": [
    "qgs file",
    "qgs file format",
    "what is a qgs file",
    "file",
    "qgs example",
    "qgs file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "QGS - QGIS Project File Format",
  "description": "Learn about QGS file format and APIs that can create and open QGS files.",
  "linktitle": "QGS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qgs"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a QGS file?

A file with .qgs extension is a project file created with [QGIS](https://www.qgis.org/en/site/), which is an open-source cross-platform GIS application. All the project settings such as layer properties and auxiliary data for the project. It is created when a map project is saved to disc. It is actually a configuration file that retains information such as pointers to the GIS data, styling information about the layers, and project title. QGS files can be opened with QGIS software that is freely available to download.

## QGS File Format

QGS files are in [XML](/web/xml/) format and store projects data as XML tags. A QGS file contains information such as:

 * project title
 * project CRS
 * the layer tree
 * snapping settings
 * relations
 * the map canvas extent
 * project models
 * legend
 * mapview docks (2D and 3D)
 * the layers with links to the underlying datasets (data sources) and other layer properties including extent, SRS, joins, styles, renderer, blend mode, opacity and more.
 * project properties

### QGS Top Level XML Tags

{{< figure src="../qgstoplevel.png" title="" >}}

### Extended Top Level Project Layer Tags

{{< figure src="../qgstoplevel.png" title="" >}}

## References

* [QGIS](https://www.qgis.org/en/site/)
