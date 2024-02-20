{
  "date": "2019-10-11",
  "keywords": [
    "qml file",
    "qml file format",
    "what is an qml file",
    "file",
    "qml example",
    "qml file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "QML - The QGIS Style File Format",
  "description": "Learn about QML file format and APIs that can create and open QML files.",
  "linktitle": "QML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qml"
    }
  },
  "lastmod": "2021-03-14"
}

## What is a QML file?

A file with .qml extesion is a XML file that stores layer styling information for QGIS layers. QGIS is an open-source cross-platform GIS application used to display geospatial data with the capability of organizing data in the form of layers. QML files contain information that is used by the QGIS to render feature geometries including symbol definitions, sizes and rotations, labelling, opacity, blend mode, and much more. Unlike the QLR files, QML files contains all the styling information in itself. QML files can be opened in any text editor such as Notepad++.

## QML File Format

QLR, similar to [QGS](/gis/qgs/) and [QLR](/gis/qlr/), is an XML file that contains styling information for the layers.

The figure below shows the top level tags of a QML file (with only renderer_v2 and its symbol tag expanded).

{{< figure src="../qml.png" title="" >}}

## References

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)
