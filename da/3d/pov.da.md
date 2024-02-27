
{
  "date": "2023-01-05",
  "keywords": [
"pov fil",
"pov filformat",
"hvad er en pov-fil",
"fil",
"pov eksempel",
"pov filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om POV-filformater og API'er, der kan åbne og oprette POV-filer.",
  "title": "POV - Persistence of Vision File",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-dav"
}
},
  "lastmod": "2023-01-05"
}

## Hvad er en POV fil?

En POV-fil er en almindelig tekstfil, der indeholder instruktioner til POV-Ray-strålesporingssoftwaren. Disse instruktioner er skrevet i et specielt scriptsprog, der er specifikt for POV-Ray. Den specificerer scenen, der skal gengives, inklusive 3D-objekter, materialer, belysning og andre egenskaber, der definerer scenens udseende. POV-filer bruger et specielt scriptsprog, der er specifikt for POV-Ray og kan bruges til at skabe komplekse og detaljerede 3D-scener. Filtypenavnet for en POV-fil er typisk .pov eller .povray. Når du åbner en POV-fil i POV-Ray, læser softwaren instruktionerne i filen og bruger dem til at generere et gengivet billede af scenen.

.pov-filerne bruges ofte af kunstnere og designere til at skabe 3D-grafik og animationer til en række forskellige applikationer, herunder film, tv, videospil og marketingmaterialer.

## POV filformat

**.pov-filen** begynder typisk med en række **#include**-udsagn, som bruges til at inkludere biblioteker med foruddefinerede farver, teksturer og andre ressourcer, der kan bruges i scenen. Derefter definerer filen objekter, materialer og andre egenskaber for scenen ved hjælp af en række blokke. Der er mange andre typer objekter, materialer og andre egenskaber, som du kan angive i en .pov-fil, og du kan bruge loops og betingede sætninger til at skabe mere komplekse og detaljerede scener.

## Softwareapplikationer til POV

.pov-filformatet bruges af POV-Ray-strålesporingssoftwaren, så det primære program til at åbne .pov-filer er selve POV-Ray-softwaren. Du kan downloade den seneste version af POV-Ray fra den officielle hjemmeside på https://www.povray.org/.

Ud over POV-Ray er der en række andre programmer, der kan åbne og redigere .pov-filer, herunder:

- BRL-CAD: En open source 3D-modelleringssoftware, der kan importere og eksportere .pov-filer
- MeshLab: En 3D mesh-behandlingssoftware, der kan importere og eksportere .pov-filer
- Blender: En populær open source 3D-grafiksoftware, der kan importere og eksportere .pov-filer

Der kan være andre softwareprogrammer, der også kan åbne .pov-filer, så du kan prøve at bruge et filfremviser- eller konverterværktøj, hvis du ikke er i stand til at åbne en .pov-fil med ovenstående programmer.

## POV eksempel

Her er f.eks. et eksempel på en .pov-fil, der definerer en scene med en enkelt blå cylinder:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

I dette eksempel specificerer kamerablokken kameraets position og orientering i scenen, `lyskilde`-blokken erklærer en lyskilde og specificerer dens position og farve, og `cylinder`-blokken erklærer et cylinderobjekt og specificerer dets endepunkter, radius og materialeegenskaber. Når du åbner denne .pov-fil i POV-Ray-softwaren, vil den gengive et billede af en enkelt blå cylinder.

## Referencer
 * [POV-Ray - Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Dokumentation POV-Ray Website](http://www.povray.org/documentation/)

