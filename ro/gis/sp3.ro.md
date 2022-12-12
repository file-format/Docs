{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - Fișier NGS SP3",
  "description":"Aflați despre formatul de fișier SP3 și despre API-urile care pot crea și deschide fișiere SP3.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## Ce este un fișier SP3?

Un fișier cu extensia .sp3 este un format orbital National Geodetic Survey (NGS) pentru a stoca informații orbitale. Aceasta este o extensie a formatelor SP1 și SP2 ale NGS și include informațiile de corecție a ceasului satelitului care sunt calculate simultan cu orbitele. Se bazează în primul rând pe poziție și ceas și nu include viteze. Formatul a fost propus în Remondi, 1989 și a fost adoptat în 1991. Pe lângă informațiile de corecție a ceasului satelitului, acesta include informații precum exponenții de precizie a orbitei, liniile de comentarii, săptămâna GPS și secundele săptămânii asociate cu prima epocă. Fișierele SP3 pot fi deschise cu Wolfram Research Mathematica.

## Format de fișier SP3 - Mai multe informații

Fișierele SP3 sunt salvate pe disc în format de fișier ASCII și conținutul acestuia poate fi deschis în orice editor de text pentru vizualizare. Structura unui fișier SP3 poate fi văzută din imaginea următoare.

{{< figure src="../sp3-file-format.png" title="" >}}

## Referințe

* [Formatul Extended Standard Product 3 Orbit (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,a%20more%20flexible%20header%20structure)
* [Extinderea formatelor standard de orbită GPS pentru studiul geodezic național](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

