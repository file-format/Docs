{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "FileGDB",
  "description":"Learn about FileGDB file format and APIs that can create and open FileGDB files.",
  "linktitle" : "FileGDB",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is a FileGDB file? #

ESRI file Geodatabase (FileGDB) is a collection of files in a folder on disc that hold related geospatial data such as feature datasets, feature classes and associated tables. It requires certain other files to be kept alongside the .gdb file in the same directory for it to work. Queries can be executed on the .gdb file to manage spatial as well as non-spatial data.

File geodatabases are made up of seven system tables plus user data. User data can be stored in the following types of datasets:

* Feature class
* Feature dataset
* Mosaic dataset
* Raster catalog
* Raster dataset
* Schematic dataset
* Table (nonspatial)
* Toolboxes

Feature datasets can contain feature classes as well as the following types of datasets:

* Attachments
* Feature-linked annotation
* Geometric networks
* Network datasets
* Parcel fabrics
* Relationship classes
* Terrains
* Topologies

The default maximum size of datasets in file geodatabases is 1 TB. The maximum size can be increased to 256 TB for large datasets (usually raster). This is controlled by a configuration keyword. See Configuration keywords for file geodatabases for more information.

File geodatabases can also contain subtypes and domains and participate in checkout/check-in replication and one-way replicas.

A file geodatabase can be accessed simultaneously by several users. If the users are editing, they must edit different datasets.

## File Format Specifications ##

File GDB is ESRI proprietary format and its specifications are not available publicly. Due to this reason, the file format details for FIle GDB could not be documented anywhere other than some sources who have done it [partially](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) by reverse engineering.

## References ##

* [FGDB Specifications](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)
