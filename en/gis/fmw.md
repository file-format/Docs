{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "FMW File - FME Workbench File Format",
  "description":"Learn about FMW file format and APIs that can create and open FMW files.",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw",
      "parent" : "gis"
    }
  },
  "lastmod" : "2022-05-06"
}

## What is a FMW file?

An FMW file is a project file created with FME Workbench software (comes as part of FME Desktop suite) that is used for spatial data transformation. It contains user defined settings used for spatial data manipulation such as input data sets, translation properties, projections, and output settings. The spatial data manipulation settings are stored as a visual layout and are easy to be edited and saved again.

You can open FMW files using [Safe Software FME Desktop](https://fme.safe.com/platform/).

## FMW File Format - More Information

FMW files are stored to disc as binary files and can be read using the FME Desktop software only. The software can also read data from a number of relational database formats and also supports a range of data formats.

### FMW Quick Facts

|Fact|Value|
---|---|
|Reader/Writer|Reader|
|Licensing Level|Base|
|Dependencies|None|
|Dataset Type|File|
|Feature Type|Fixed|
|Typical File Extensions|.fmw|
|Automated Translation Support|Yes|
|User-Defined Attributes|No|
|Coordinate System Support|No|
|Generic Color Support|No|
|Spatial Index|No|
|Schema Required|No|
|Transaction Support|No|
|Geometry Type Attribute|None|
|Encoding Support|No|

### FMW Geometry Support

|Geometry|Supported?|
---|---|
|aggregate|no|
|circles|no|
|circular arc|no|
|donut polygon|no|
|elliptical arc|no|
|ellipses|no|
|line|no|
|none|yes|
|point|no|
|polygon|no|
|raster|no|
|solid|no|
|surface|no|
|text|no|
|z values|no|


## References

* [Safe Software FME Desktop](https://fme.safe.com/platform/)
* [FMW Quick Facts](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)
