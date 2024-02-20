{
  "date": "2021-07-29",
  "keywords": [
    "shx file",
    "shx file format",
    "what is an shx file",
    "file",
    "shx example",
    "shx file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "title": "SHX - Shapefile Shape Index Format",
  "description": "Learn about SHX file format and APIs that can create and open SHX files.",
  "linktitle": "SHX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-shx"
    }
  },
  "lastmod": "2021-07-29"
}

## What is an SHX file?
The SHX file belongs to shape index format which is a positional index of the feature geometry to enable seeking forwards and backwards quickly. The SHX is a direct access offset file. There is no data in this file, only a duplicate copy of the first hundred bytes, record number and offset to the starting byte of that record in the shp. Please note that the file with .shx extension does not tie the [SHP](/gis/shp/) and [DBF](/database/dbf/).

## SHX file format
The SHX format contains positional index of the feature geometry and 100-byte header similar to the SHP file, followed by any number of 8-byte fixed-length records which contain the following two fields:
| Bytes | Type  | Endianness |              Usage              |
-------|-------|------------|---------------------------------|
|  0–3  | int32 |    big     | Record offset (in 16-bit words) |
|  4–7  | int32 |    big     | Record length (in 16-bit words) |

This index makes it possible to seek backwards in the shapefile by, first, seeking backwards in the shape index and then reading the record offset. That offset can be used to seek to the correct position in the SHP file. You can also seek forwards; an arbitrary number of records using the same method. Although, it is possible to generate complete index along with an SHP file, but it can increase the chances to make the SHP file corrupt quickly.


## References

* [Shapefile - by Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)

