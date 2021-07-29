{
  "date" : "2021-07-29",
  "keywords" : [ "gpkg file", "gpkg file format", "what is a gpkg file", "file", "gpkg example", "gpkg file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "GPKG - GeoPackage Format Files",
  "description":"Learn about GPKG file format and APIs that can create and open GPKG files.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2021-07-29"
}

## What is a GPKG file?
A file with a .gpkg extension consists of a geographic information system implemented as a SQLite database container containing data and metadata tables with typical definitions,  format limitations, integrity assertions and content constraints. It was published in 2014; defined by the OGC (Open Geospatial Consortium) on the behalf of the US military. Various governments, commercial, and open source organizations widely support the GeoPackage.

## GPKG file format
A GeoPackage is made up as an extended SQLite 3 database file; a standard defines a set of rules (required conventions) for:
- Storing tile matrix sets of imagery
- Vector features 
- Raster maps at various scales
- Metadata and schema 

You can extend a GeoPackage by using the extension rules as defined in clause 2.3 of the standard. The purpose of designing a GeoPackage was to make a lightweight database as much possible and include it in a ready-to-use single file. This makes it ideal for mobile applications in off-line mode and fast sharing on cloud storage or USB storage devices, etc.

### GPKG Contents
The GeoPackages contain a number of tables, like other relational databases. These tables can be either user-defined or metadata tables. GeoPackages consist of two mandatory metadata tables:

#### gpkg_contents
A table of contents for a GeoPackage. The mandatory columns in this table are:

- **table_name**: the actual name of the user-defined data table;
- **data_type**: the data type, e.g. titles, features and attributes;
- **identifier and description**: human-readable text ;
- **last_change**: the informational date of last change, in ISO 8601 format ;
- **min_x, min_y, max_x, and max_y**: the spatial extents of the content. ;
- **srs_id**: spatial reference system .

#### gpkg_spatial_ref_sys
For spatial reference content; including but not limited to tiles and features, each row in contents must reference a coordinate reference system; stored in the **gpkg_spatial_ref_sys** table. The mandatory columns in this table are:

- **srs_name, description**: a human readable name and description for the SRS;
- **srs_id**: a unique identifier for the SRS; also the primary key for the table;
- **organization**: Case-insensitive name of the defining organization.
- **organization_coordsys_id**: Numeric ID of the SRS assigned by the organization;
- **definition**: Well Known Text definition of the SRS.


## References

* [GeoPackage - by Wikipedia)](https://en.wikipedia.org/wiki/GeoPackage)
* [Getting Started With GeoPackage](http://www.geopackage.org/guidance/getting-started.html)
