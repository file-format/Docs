{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CUBE File - Gaussian Cube File - Vad är .cube-fil och hur man öppnar den?",
  "description" : "Lär dig om Gaussian Cube File och hur du öppnar den.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-sv-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Vad är en CUBE-fil?

CUBE-filformat, även känt som Gaussian Cube-fil (.cube) används i beräkningskemi för lagring av molekylär data, särskilt information om elektrondensitet som härrör från kvantkemiberäkningar. Det här formatet förknippas vanligtvis med **Gaussian mjukvarupaket**, som används ofta för att utföra ab initio elektroniska strukturberäkningar.

Gaussiska kubfiler lagrar tredimensionella data, typiskt representerande elektrondensitet eller andra egenskaper hos molekyler, erhållna genom kvantkemiberäkningar. Filen innehåller rubriksektion med metadata (såsom ursprung, antal datapunkter längs varje axel och avstånd), följt av rutnät med numeriska värden som representerar egenskapen av intresse (t.ex. elektrondensitet) vid varje rutnätspunkt i rymden.

Gaussian Cube-fil (.cube) är en vanlig textfil med specifik struktur. Rubriken innehåller information om molekylära system och datanät, och datavärden är ordnade i tredimensionellt rutnätsformat. Gaussiska kubfiler används ofta för att visualisera molekylära egenskaper med hjälp av programvara för molekylär visualisering. Program som **VMD (Visual Molecular Dynamics)** eller **PyMOL** kan läsa Gaussian Cube-filer för att visa molekylära ytor, elektrondensitet eller andra beräknade egenskaper.

## Förenklat exempel på Gaussian Cube-fil:

```
Exempel på kubfil
Genererad av Gaussian
   0 1 0 0 0 0 0 0 0 0
   0,0000000000000000E+00 0,00000000000000000E+00 0,0000000000000000E+00
  50 0,1000000000000000E+01 0,0000000000000000E+00 0,00000000000000000E+00
  50 0,00000000000000000E+00 0,1000000000000000E+01 0,00000000000000000E+00
  50 0,00000000000000000E+00 0,0000000000000000E+00 0,10000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (datavärden för elektrondensitet vid varje rutnätspunkt)
```

## Om Gaussian

Gaussian är en svit av mjukvaruapplikationer för kvantkemi och beräkningskemi. Gaussians primära fokus ligger på ab initio kvantkemimetoder, som är mycket exakta men beräkningsintensiva metoder för att studera elektroniska strukturer hos molekyler. Mjukvaran används ofta i forskning och akademiska miljöer för olika tillämpningar, inklusive att förutsäga molekylära egenskaper, studera reaktionsmekanismer och utforska molekylära strukturer.

## Om NWChem

NWChem är en programvara för beräkningskemi med öppen källkod designad för högpresterande kvantkemi-simuleringar. Den använder ab initio metoder som Hartree-Fock och densitetsfunktionsteori, stöder parallell beräkning för effektiva beräkningar på kluster och hittar tillämpningar inom olika vetenskapliga områden, inklusive beräkningskemi, biokemi och materialvetenskap. NWChem är känt för sin mångsidighet, vilket gör det möjligt för forskare att studera olika kemiska system, och dess öppen källkod uppmuntrar samhällsbidrag och anpassning.

## Om VMD

VMD, som står för Visual Molecular Dynamics, är ett kraftfullt och allmänt använt molekylärt visualiseringsprogram för att visa, analysera och animera molekylära dynamikbanor (MD) såväl som statiska molekylära strukturer. Det är särskilt populärt inom områdena beräkningskemi, molekylärbiologi och strukturell bioinformatik. VMD utmärker sig när det gäller att visualisera molekylära strukturer och tillhandahåller högkvalitativa 3D-renderingar av molekyler och molekylära komplex. Den stöder olika molekylära filformat.

## Om PyMOL

PyMOL är ett molekylärt visualiseringssystem och mjukvaruverktyg som används för tredimensionell visualisering av molekylära strukturer. Det är särskilt populärt inom områdena strukturell biologi, bioinformatik och beräkningskemi. PyMOL tillhandahåller högkvalitativa 3D-renderingar av molekylära strukturer, vilket gör det möjligt för användare att visualisera och utforska former, ytor och interaktioner av biologiska makromolekyler.

## Hur öppnar man filen CUBE?

CUBE-filen kan öppnas och refereras med följande program.

- **NWChem** (gratis) för (Windows, MAC, Linux)

## Referenser
* [Gaussian Cube File Format](https://paulbourke.net/dataformats/cube/)
