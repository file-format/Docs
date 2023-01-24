{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HDR File- ESRI BIL Header File Format",
  "description":"What is an HDR file?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
    }
  },
  "lastmod" : "2023-01-23"
}

## What is a HDR file?

An HDR file is a GIS header file that contains header information for a Band interleaved by line (.BIL) file. It describes the image data and has the same name as that of the image file. An HDR file comprises of a set of entries, each of which describes a particular attribute of the image. The HDR file describes the layout and formatting of the BIL file for translation to real world coordinates in combination with a separate georeferencing file.

## HDR File Format

HDR files are saved in ASCII text file format. It contains a set of entries where each entry describes a particular attribute of the image. Each HDR file has the following format:

```
<keyword> <value>
```

`<keyword>` - It indicates the particular attribute that is being set
`<value>` - It is the value to which the attribute is being set

There is no limitation on the order of the entries in the header. However, each entry must be on a separate line of the line to comply with the parsing method used by HDR readers.

## Summary of Keywords used in HDR File

|Keyword	|Acceptable Value	|Default|
---|---|---|
|nrows	|any integer > 0|	none
|ncols	|any integer > 0|	none
|nbands	|any integer > 0|	1
|nbits	|1, 4, 8, 16, 32|	8
|byteorder|	I = Intel;M = Motorola	|same as host machine|
|layout|	bil, bip, bsq|	bil|
|skipbytes|	any integer ≥ 0|	0
|ulxmap	|any real number|	0|
|ulymap	|any real number	|nrows - 1|
|xdim	|any real number|	1
|ydim	|any real number|	1
|bandrowbytes	|any integer > 0|	smallest integer ≥ (ncols x nbits) / 8|
|totalrowbytes	|any integer > 0|	for bil: nbands x bandrowbytes;for bip: smallest integer ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes	|any integer ≥ 0|	0|

## References

* [HRD File Format - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)
