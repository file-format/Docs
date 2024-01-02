{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SSF - Trimble Standard Storage Format File",
  "description":"Learn about SSF file format and APIs that can create and open SSF files.",
  "linktitle" : "SSF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2021-08-24"
}

## What is an SSF file?

A file with .ssf file is a Geospatial data storage file format used by the [Trimble](https://www.trimble.com) Navigation GIS software applications. It stores GPS data recorded from field using Trimble devices. The GPS log is then imported in one of the applications of Trimble applications suite. The GPS log contained in an SSF is used to create custom coordinate systems. SSF files can be opened with [Trimble Navigation GPS Pathfinder Office](https://geospatial.trimble.com/en/products/software/office-software), Trimble Navigation GPS Pathfinder Tools SDK, and ESRI ArcGIS for Desktop with Trimble GPS Analyst plug-in.

## SSF File Format - More Information

When GPS data is transferred from Trimble device to computer for post processing, all of these files are combined together in to a single .ssf file. This raw unprocessed file is used by the post processing software to make corrections and aids in data management.

SSF files are stored to disc as Trimble proprietary file format and its detail specifications are not available publicly. It is specific to Trimble devices and represents data of the GPS unit. Till date, no non-commercial free solution is available to read or convert SSF files.

## References

* [Trimble News Release](https://www.trimble.com/news/release.aspx?id=050510b)
