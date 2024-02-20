{
  "date": "2021-03-18",
  "keywords": [
    "qgz file",
    "qgz file format",
    "what is an qgz file",
    "file",
    "qgz example",
    "qgz file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "title": "QGZ - Quantum GIS Compressed Project",
  "description": "Learn about QGZ file format which is just a compressed QGS and APIs that can create and open QGZ files.",
  "linktitle": "QGZ",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qgz"
    }
  },
  "lastmod": "2021-03-18"
}

## What is a QGZ file?

The **QGZ** file format is a compressed archive containing a [QGS](/gis/qgs/) file and a QGD file. Whereas, The QGD file is the sqlite database of the qgis project that consists of auxiliary data for the project. If there is no auxiliary data, the QGD file will remain empty.

## Details about QGZ File Format

The QGZ was introduced as a new variant of  the **QGIS 3 project file format**. This format is a zipped container for the QGS xml file. If users choose QGD that is an optional format, in this case the container is beneficial to store the auxiliary storage database.

In classic mode, the auxiliary database is saved as a file with .qgd extension along the xml file. When choosing the zipped container, the .qgd file includes into the .qgz, It just facilitates the users without any issue, the users can’t delete it or forget to copy it when sharing project files!


## References

* [QGZ – A new default project file format for QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)
