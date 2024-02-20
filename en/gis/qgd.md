{
  "date": "2021-03-18",
  "author": {
    "display_name": "Muhammad Umar",
    "keywords": [
      "QGD",
      "Sqlite Database of the QGIS Project",
      "extension",
      "format",
      "QGIS",
      "Auxilary Database",
      "What is a QGD file"
    ]
  },
  "draft": "false",
  "toc": true,
  "title": "QGD - Sqlite Database of the QGIS Project",
  "description": "Learn about QGD which is an sqlite database of the QGIS project and APIs that can create and open QGD files.",
  "linktitle": "QGD",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qgd"
    }
  },
  "lastmod": "2021-03-18"
}

## What is a QGD file?

The file with extension .QGD file is actually the associated sqlite database of the **QGIS** project that accommodates the auxiliary data for the project. The QGD file will remain empty, if there will be no auxiliary data for the project.

## Details about QGD File Format

In classic mode, the auxiliary database is saved as a file with .qgd extension along the xml file. The **Auxiliary Database** system allows to read and write data in the system as an alternative way. When Creating the QGZ which is a zipped container, the .qgd file includes into the .qgz. 

## What is Auxilary Database?
The Auxiliary Database is actually a standby db system that is created as a response of the duplication of the target database. The auxiliary database is actually a case of a duplicate database would be the database you are duplicating to. E.g. if you setup a standby database using duplicate database, the source database will be the target and the standby database will be known as the auxiliary.


## References

* [QGZ – A new default project file format for QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)
