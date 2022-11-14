{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - NGS SP3-bestand",
  "description":"Meer informatie over de SP3-bestandsindeling en API's die SP3-bestanden kunnen maken en openen.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Wat is een SP3-bestand?

Een bestand met de extensie .sp3 is een orbitaalformaat van National Geodetic Survey (NGS) om orbitale informatie op te slaan. Dit is een uitbreiding op de SP1- en SP2-formaten van NGS en bevat de satellietklokcorrectie-informatie die gelijktijdig met de banen wordt berekend. Het is voornamelijk gebaseerd op positie en klok, en omvat geen snelheden. Het formaat werd voorgesteld in Remondi, 1989 en werd in 1991 aangenomen. Naast informatie over de correctie van de satellietklok bevat het informatie zoals exponenten van de baannauwkeurigheid, commentaarregels, de GPS-week en seconden van de week die verband houden met het eerste tijdperk. SP3-bestanden kunnen worden geopend met Wolfram Research Mathematica.

## SP3-bestandsindeling - Meer informatie

SP3-bestanden worden op schijf opgeslagen in ASCII-bestandsindeling en de inhoud ervan kan in elke teksteditor worden geopend om te bekijken. De structuur van een SP3-bestand is te zien in de volgende afbeelding.

{{< figure src="../sp3-file-format.png" title="" >}}

## Referenties

* [The Extended Standard Product 3 Orbit Format (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,a%20more%20flexible%20header%20structuur)
* [Uitbreiding van de National Geodetic Survey standaard GPS-baanformaten](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

