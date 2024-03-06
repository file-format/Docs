{
  "date": "2021-08-24",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SP3 — NGS SP3 fails",
  "description": "Uzziniet par SP3 failu formātu un API, kas var izveidot un atvērt SP3 failus.",
  "linktitle": "SP3",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sp-lv3"
}
},
  "lastmod": "2021-09-29"
}

## Kas ir SP3 fails?

A file with .sp3 extension is a National Geodetic Survey (NGS) orbital format to store orbital information. This is an extension to NGS's SP1 and SP2 formats, and includes the satellite clock correction information that is computed simultaneously with the orbits. It is primarily based on position and clock, and does not include velocities. The format was proposed in Remondi, 1989 and was adopted in 1991. Papildus satelīta pulksteņa korekcijas informācijai tajā ir iekļauta tāda informācija kā orbītas precizitātes eksponenti, komentāru līnijas, GPS nedēļa un nedēļas sekundes, kas saistītas ar pirmo laikmetu. SP3 failus var atvērt ar Wolfram Research Mathematica.

## SP3 faila formāts — plašāka informācija

SP3 faili tiek saglabāti diskā ASCII faila formātā, un to saturu var atvērt jebkurā teksta redaktorā apskatei. SP3 faila struktūru var redzēt nākamajā attēlā.

{{< figure src="../sp3-file-format.png" title="" >}}

## Atsauces

* [The Extended Standard Product 3 Orbit Format (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,a%20vairāk%20elastīga%20header%20struktūra)

* [Nacionālo ģeodēzisko apsekojumu standarta GPS orbītas formātu paplašināšana](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)


