{
  "date" : "2021-04-08",
  "keywords" : [ "oar file", "oar file format", "what is an oar file", "file", "oar example", "oar file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "OAR - OpenSimulator Archive File Format",
  "description":"Learn about OAR file format and APIs that can create and open OAR files.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-15"
}

## What is an OAR file?

A file with .oar extension is an archive file used by the OpenSimulator application which is an open-source 3D application server for creating a virtual environment accessible to multi-users over the network. The OAR file format provides necessary asset data required to fully load the terrain, object textures, and inventories on a different system. OpenSimulator also has optional hypergrid that allows users to visit other OpenSimulator installations across the web. OAR files have internet MIME type application/oar and contains one or more archived files.


## OAR File Format

OAR are binary files that are stored in compressed archive file format. The latest version of OAR file format is [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) that has major changes from its previous [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). The latest version supports storing multiple regions in a single OAR and is not backwards compatible with versions of OpenSimulator before 0.7.5. An OAR file is a gzipped tar file (tar.gz) in the the original unix tar format (not USTAR).

## OAR Regions Example
AOR files can contain multiple regions. The structure of the archive is as follows (this example contains 4 regions):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

The archive control file contains a major version number for defining compatibility with future format changes. The presence of assets in an OAR format is indicated by the boolean element <assets_included>. Information about the included regions is contained in a manifest that is present in the control file. An example of Archive.xml is as follow.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## References

 * [OAR Format v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
 * [OpenSimulator](http://opensimulator.org/wiki/Main_Page)
