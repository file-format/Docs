
{
  "date": "2023-01-05",
  "keywords": [
"pov-fil",
"pov filformat",
"vad är en pov-fil",
"fil",
"pov exempel",
"pov filtillägg",
"förlängning",
"formatera"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Lär dig om POV-filformat och API:er som kan öppna och skapa POV-filer.",
  "title": "POV - Persistence of Vision File",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-svv"
}
},
  "lastmod": "2023-01-05"
}

## Vad är en POV fil?

En POV-fil är en vanlig textfil som innehåller instruktioner för programvaran för POV-Ray-strålspårning. Dessa instruktioner är skrivna på ett speciellt skriptspråk som är specifikt för POV-Ray. Den specificerar scenen som ska renderas, inklusive 3D-objekt, material, belysning och andra egenskaper som definierar scenens utseende. POV-filer använder ett speciellt skriptspråk som är specifikt för POV-Ray och kan användas för att skapa komplexa och detaljerade 3D-scener. Filtillägget för en POV-fil är vanligtvis .pov eller .povray. När du öppnar en POV-fil i POV-Ray läser programvaran instruktionerna i filen och använder dem för att generera en renderad bild av scenen.

.pov-filerna används ofta av konstnärer och designers för att skapa 3D-grafik och animationer för en mängd olika applikationer, inklusive film, tv, videospel och marknadsföringsmaterial.

## POV-filformat

**.pov-filen** börjar vanligtvis med en serie **#include**-satser, som används för att inkludera bibliotek med fördefinierade färger, texturer och andra resurser som kan användas i scenen. Sedan definierar filen objekt, material och andra egenskaper för scenen med hjälp av en serie block. Det finns många andra typer av objekt, material och andra egenskaper som du kan ange i en .pov-fil, och du kan använda loopar och villkorliga uttalanden för att skapa mer komplexa och detaljerade scener.

## Programvaruapplikationer för POV

.pov-filformatet används av POV-Ray ray tracing programvara, så det primära programmet för att öppna .pov filer är själva POV-Ray programvaran. Du kan ladda ner den senaste versionen av POV-Ray från den officiella webbplatsen på https://www.povray.org/.

Förutom POV-Ray finns det ett antal andra program som kan öppna och redigera .pov-filer, inklusive:

- BRL-CAD: En 3D-modelleringsprogramvara med öppen källkod som kan importera och exportera .pov-filer
- MeshLab: En 3D-mesh-bearbetningsprogramvara som kan importera och exportera .pov-filer
- Blender: Ett populärt 3D-grafikprogram med öppen källkod som kan importera och exportera .pov-filer

Det kan finnas andra program som kan öppna .pov-filer också, så du kanske vill prova att använda ett filvisare eller konverteringsverktyg om du inte kan öppna en .pov-fil med ovanstående applikationer.

## POV Exempel

Här är till exempel ett exempel på en .pov-fil som definierar en scen med en enda blå cylinder:

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

I det här exemplet specificerar kamerablocket kamerans position och orientering i scenen, light_source-blocket deklarerar en ljuskälla och specificerar dess position och färg, och cylinder-blocket deklarerar ett cylinderobjekt och specificerar dess slutpunkter, radie och materialegenskaper. När du öppnar den här .pov-filen i POV-Ray-mjukvaran renderar den en bild av en enda blå cylinder.

## Referenser
 * [POV-Ray - Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Dokumentation POV-Ray webbplats](http://www.povray.org/documentation/)

