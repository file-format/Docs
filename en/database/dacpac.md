{
  "date" : "2021-09-06",
  "keywords" : [ "dacpac", "extension", "file", "file format", "Database File Type", "Database File Format", "Data Tier AppliCation Package" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DACPAC file format and APIs that can create and open DACPAC files.",
  "title" : "DACPAC - Data Tier AppliCation Package",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-09-06"
}

## What is a DACPAC file?

A file with .dacpac (stands for Data Tier AppliCation Package) extension is a database file, created with Microsoft SQL Server data tier application, that contains the database model for representation of database objects. As it contains the complete model of the database, it is used to restore a database from the details available in the model. DACPAC files are usually handed over to deployment teams for installation at customer's premises to restore database. These can be opened with
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019?ranMID=24542&ranEAID=4LioSo*jxMc&ranSiteID=4LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw&epi=4LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw&irgwc=1&OCID=AID2200057_aff_7593_1243925&tduid=%28ir__gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00%29%287593%29%281243925%29%284LioSo.jxMc-XSp30B6cXpiTS89wo0jYzw%29%28%29&irclickid=_gn1tqusqf0kf6whl2qniaboutn2xruqfmyy1hzec00).

## DACPAC File Format - More Information

The DACPAC data package files are actually compressed ZIP files that contains several [XML](/web/xml/) files containing information about the database model, such as tables and views, used to restore a database. In order to view the contents of DACPAC files, rename the files from .dacpac to [.zip](/compression/zip/) and extract the zip archive using any decompression utility.

Following are few files that are found inside a DACPAC file.

 * [Content_Types].xml
 ```
 <?xml version="1.0" encoding="utf-8"?>
<Types
    xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
    <Default Extension="xml" ContentType="text/xml" />
</Types>
 ```
 * DacMetadata.xml

 ```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
  <Name>CRM</Name>
  <Version>1.0.0.0</Version>
</DacType>
 ```
 * Origin.xml

 * model.xml

 It is to be noted that DACPAC does not contain DATA and other server-level objects. The file can contains all object types which might be kept in SSDT project.

## References

* [Data Tier Applications - Benefits](https://docs.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications?view=sql-server-ver15)
* [Deploying a Data Tier Application - Microsoft](https://docs.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [How to create DACPAC File?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)
