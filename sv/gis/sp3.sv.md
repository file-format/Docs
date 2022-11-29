{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - NGS SP3-fil",
  "description":"Läs mer om SP3-filformat och API:er som kan skapa och öppna SP3-filer.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Vad är en SP3-fil?

En fil med tillägget .sp3 är ett orbitalformat för National Geodetic Survey (NGS) för att lagra orbitalinformation. Detta är en förlängning av NGS:s SP1- och SP2-format och inkluderar information om satellitklockkorrigering som beräknas samtidigt med banorna. Den är främst baserad på position och klocka, och inkluderar inte hastigheter. Formatet föreslogs i Remondi, 1989 och antogs 1991. Förutom information om korrigering av satellitklockor, inkluderar det information som exponenter för omloppsnoggrannhet, kommentarslinjer, GPS-veckan och veckosekunder associerade med första epok. SP3-filer kan öppnas med Wolfram Research Mathematica.

## SP3-filformat - Mer information

SP3-filer sparas på skiva i ASCII-filformat och dess innehåll kan öppnas i valfri textredigerare för visning. Strukturen för en SP3-fil kan ses i följande bild.

{{< figure src="../sp3-file-format.png" title="" >}}

## Referenser

* [The Extended Standard Product 3 Orbit Format (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,en%20mer%20flexibel%20header%20struktur)
* [Utöka National Geodetic Survey Standard GPS Orbit Formats](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

