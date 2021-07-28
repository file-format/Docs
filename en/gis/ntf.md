{
  "date" : "2021-07-28",
  "keywords" : [ "ntf file", "ntf file format", "what is an ntf file", "file", "ntf example", "ntf file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "NTF - National Transfer Format Files",
  "description":"Learn about NTF file format and APIs that can create and open NTF files.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2021-07-28"
}

## What is an NTF file?
The files with extension .ntf extension are called the **National Transfer Format (NTF)** Files; mostly used by the U.K. Ordnance Survey (OS); specifically for the transfer of geospatial data. It is managed by the British Standards Institution. It has become the standard transfer format for Ordnance Survey digital data. The UK's National Grid projection, which is a type of Transverse Mercator, holds all the georeferenced information for NTF files.

## NTF file format
The NTF file format is owned by Ordnance Survey in the United Kingdom; supported by the GDB library for import. The Present version of the NTF file format is 2.0. This file format was introduced to address a limitation of **PCIDSK** vector segment which has only one attribute field per structure, but there are a variety of attributes that can be extracted with vector data. To get around the NTF file format is constituted as having two segments. Each segment consists of the same vectors, but with different attributes. The first Segment of an NTF vector file contains the vectors with the feature code number as the attribute. The second segment contains the vectors with the value as the attribute.

### Coordinate referencing system
The GDB library represents raster and vector data with the appropriate TM projection characteristics:

- Reference Longitude: 49.0
- Reference Latitude: 2.0
- False Easting: 400000
- False Northing: -100000
- Scale: 0.9996012717
- Ellipsoid: Airy 1830 (E009)
No support is available for updating, or writing NTF files, nor can the DTM files be linked to.

### Ogrinfo example
Following example uses **ogrinfo** on an NTF file to retrieve layer numbers:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## References

* [UK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Web Mapping - Illustrated by Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)
