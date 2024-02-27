{
  "date": "2021-08-24",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SP3 - NGS SP3 fil",
  "description": "Lær om SP3-filformater og API'er, der kan oprette og åbne SP3-filer.",
  "linktitle": "SP3",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sp-da3"
}
},
  "lastmod": "2021-09-29"
}

## Hvad er en SP3 fil?

A file with .sp3 extension is a National Geodetic Survey (NGS) orbital format to store orbital information. This is an extension to NGS's SP1 and SP2 formats, and includes the satellite clock correction information that is computed simultaneously with the orbits. It is primarily based on position and clock, and does not include velocities. The format was proposed in Remondi, 1989 and was adopted in 1991. Ud over satellit-ur-korrektionsinformation inkluderer den information såsom eksponenter for kredsløbsnøjagtighed, kommentarlinjer, GPS-ugen og ugesekunder forbundet med den første epoke. SP3-filer kan åbnes med Wolfram Research Mathematica.

## SP3-filformat - flere oplysninger

SP3-filer gemmes på disk i ASCII-filformat, og indholdet kan åbnes i ethvert tekstredigeringsprogram til visning. Strukturen af en SP3-fil kan ses fra det følgende billede.

{{< figure src="../sp3-file-format.png" title="" >}}

## Referencer

* [The Extended Standard Product 3 Orbit Format (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,en%20mere%20fleksibel%20header%20struktur)

* [Udvidelse af National Geodetic Survey Standard GPS Orbit Formats](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)


