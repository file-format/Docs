{
  "date": "2021-08-24",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SP3 - NGS SP3 -tiedosto",
  "description": "Opi SP3-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SP3-tiedostoja.",
  "linktitle": "SP3",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sp-fi3"
}
},
  "lastmod": "2021-09-29"
}

## Mikä on SP3-tiedosto?

A file with .sp3 extension is a National Geodetic Survey (NGS) orbital format to store orbital information. This is an extension to NGS's SP1 and SP2 formats, and includes the satellite clock correction information that is computed simultaneously with the orbits. It is primarily based on position and clock, and does not include velocities. The format was proposed in Remondi, 1989 and was adopted in 1991. Satelliittikellon korjaustietojen lisäksi se sisältää tietoja, kuten kiertoradan tarkkuuseksponentit, kommenttirivit, GPS-viikko ja ensimmäiseen aikakauteen liittyvät viikon sekunnit. SP3-tiedostot voidaan avata Wolfram Research Mathematicalla.

## SP3-tiedostomuoto – lisätietoja

SP3-tiedostot tallennetaan levylle ASCII-tiedostomuodossa ja niiden sisältö voidaan avata missä tahansa tekstieditorissa katselua varten. SP3-tiedoston rakenne näkyy seuraavasta kuvasta.

{{< figure src="../sp3-file-format.png" title="" >}}

## Viitteet

* [The Extended Standard Product 3 Orbit Format (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,a%20more%20flexible%20header%20structure)

* [National Geodetic Survey Standardin GPS-kiertoratamuotojen laajentaminen](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)


