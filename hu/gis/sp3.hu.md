{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 – NGS SP3 fájl",
  "description":"További információ az SP3 fájlformátumról és az API-król, amelyek SP3 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Mi az SP3 fájl?

Az .sp3 kiterjesztésű fájl a National Geodetic Survey (NGS) orbitális formátuma a pályaadatok tárolására. Ez az NGS SP1 és SP2 formátumának kiterjesztése, és tartalmazza a műhold órakorrekciós információit, amelyeket a pályákkal egyidejűleg számítanak ki. Elsősorban pozíción és órajelen alapul, és nem tartalmazza a sebességeket. A formátumot 1989-ben Remondi javasolta, és 1991-ben fogadták el. A műhold óra korrekciós információi mellett olyan információkat is tartalmaz, mint a pályapontossági kitevők, megjegyzéssorok, a GPS hét és az első korszakhoz kapcsolódó hét másodpercei. Az SP3 fájlok a Wolfram Research Mathematica segítségével nyithatók meg.

## SP3 fájlformátum – További információ

Az SP3 fájlok ASCII fájlformátumban kerülnek a lemezre, és azok tartalma bármely szövegszerkesztőben megnyitható megtekintés céljából. Az SP3 fájl szerkezete a következő képen látható.

{{< figure src="../sp3-file-format.png" title="" >}}

## Hivatkozások

* [The Extended Standard Product 3 Orbit Format (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,a%20more%20flexible%20header%20struktúra)
* [A National Geodetic Survey Standard GPS pályaformátumok kiterjesztése](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

