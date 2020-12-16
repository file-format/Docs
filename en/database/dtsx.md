{
  "date" : "2020-11-11",
  "keywords" : [ "DTSX", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DTSX file format and APIs that can create and open DTSX files.",
  "title" : "DTSX File Format - SQL Server DTS Settings File",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-08-12"
}

## What is a DTSX file?

A file with .dtsx (Data Transformation Services Package XML) extension is a Data Transformation Services (DTS) file that is used by Microsoft SQL for referring to data migration steps/rules for transfer of data from one database to another. This includes the transformations and any optional processing steps that may be required during the data transfer between the originating and destination points. SQL Server Integration Services (SSIS), a  component of Microsoft SQL Server, uses the DTSX files to identify the steps for processing of data between database servers. DTSX files can be opened with Microsoft SQL Server 2019.

## DTSX File Forrmat

Data movement between database servers requires rules and processing steps to ensure the integrity of data during this operation. SSIS ensures that all these activities, to move and conform data from different sources in an enterprise, take place conveniently. That is where DTSX comes that defines the structures to be used by SSIS to establish the steps where the data can be processed as it follows through these steps.

The data flow described by DTSX is as shown in the following image.

{{< figure src="../DataFlowDTSX.png" alt="Data Flow DTSX" >}}

DTSX is [XML](/web/xml/)-based and is documented in [MS-DTSX](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). The enhanced refactoring of DTSX XML is DTSX 2.0 that includes new attributes to the structures, replacement of named properties as parent XML attributes, specifies defaults for most attribute values, and placement of repeated elements inside a parent element. DTSX structures are described using these [XML Schemas](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) and the structural format is celar-text XML.

## References

 * [DTSX Format - Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)

 * [DTSX 2 Format - By Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)
