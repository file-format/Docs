{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SP3 - NGS SP3 File",
  "description":"Learn about SP3 file format and APIs that can create and open SP3 files.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2021-09-29"
}

## What is an SP3 file?

A file with .sp3 extension is a National Geodetic Survey (NGS) orbital format to store orbital information. This is an extension to NGS's SP1 and SP2 formats, and includes the satellite clock correction information that is computed simultaneously with the orbits. It is primarily based on position and clock, and does not include velocities. The format was proposed in Remondi, 1989 and was adopted in 1991. In addition to satellite clock correction information, it includes informaiton such as orbit accuracy exponents, comment lines, the GPS week, and seconds of week associated with first epoch. SP3 files can be opened with Wolfram Research Mathematica.

## SP3 File Format - More Information

SP3 files are saved to disc in ASCII file format and its contents can be opened in any text editor for viewing. The structure of an SP3 file can as be seen from in the following image.

{{< figure src="../sp3-file-format.png" title="" >}}

## References

* [The Extended Standard Product 3 Orbit Format (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar,a%20more%20flexible%20header%20structure)
* [Extending the  National Geodetic Survey Standard GPS Orbit Formats](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)
