{
  "date": "2019-10-11",
  "keywords": [
    "qlr file",
    "qlr file format",
    "what is an qlr file",
    "file",
    "qlr example",
    "qlr file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "QLR - QGIS Layer Definition File",
  "description": "Learn about QLR file format and APIs that can create and open QLR files.",
  "linktitle": "QLR",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qlr"
    }
  },
  "lastmod": "2021-03-14"
}

## What is a QLR file?

A file with .qlr is a Layer Definition file that contains a pointer to the layer data source. This is in addition to the [QGIS](https://www.qgis.org/en/site/) style information for the layer. Having references to all related styles, this file is used as a single source for data to be used for getting the styling information. Using the QLR files, information to the data sources can be put in this single file that can be read by other applications to load the styling information. QLR files can be opened with any text editor such as Notepad++.

## QLR File Format

QLR, similar to [QGS](/gis/qgs/), is an XML file that contains pointers to layer data source in the form of XML tags. It is similar to ArcGIS .lyr file. The top level tags of a QML file are as shown in the image below.

{{< figure src="../qlr.png" title="" >}}

## References

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)
