{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PMF File - ESRI Published Map File Format",
  "description":"Learn about PMF file format and APIs that can create and open PMF files.",
  "linktitle" : "PMF",
  "menu" : {
    "docs" : {
      "identifier": "gis-pmf",
      "parent" : "gis"
    }
  },
  "lastmod" : "2023-01-02"
}

## What is a PMF file?

A PMF file is a read-only map file generated with ArcMap. You can say it is a shorter version of MXD file format that has limited information to be shared with users who doesn't have a paid version of ArcGIS software. This lets sharing of geographic information with others while at the same time. PMF files can be shared with other users via email due to their small sizes as a result of constrained information they contain.

PMF files can be opened with ESRI ArcReader and ESRI ArcGIS Pro.

## PMF File Format

PMF files limit the level of data accessible to users based on their subscription. If a user is using a free version of ArcGIS software, PMF files will limit the information display such as data views, layouts, navigation, printing, querying, panning, and zooming capabilities of the map. The data may not be actually contained in the limit file, but accessed from a remote location hosted on ArcMap server or available over the internet.

## References

* [How To: Configure a PMF to open in ArcMap](https://support.esri.com/en/technical-article/000011615)
