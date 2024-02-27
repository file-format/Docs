{
  "date": "2019-12-12",
  "keywords": [
"PLY",
"fil",
"udvidelse",
"format",
"3D filformat"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om PLY filformat og API'er, der kan oprette og åbne PLY filer.",
  "title": "PLY - Polygon 3D filformat",
  "linktitle": "PLY",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-pl-day"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en PLY fil?

PLY, Polygon File Format, repræsenterer 3D-filformat, der gemmer grafiske objekter beskrevet som en samling af polygoner. Formålet med dette filformat var at etablere en enkel og nem filtype, der er generel nok til at være nyttig for en lang række modeller. PLY-filformatet kommer som ASCII såvel som binært format til kompakt lagring og til hurtig lagring og indlæsning. Filformatet bruges af forskellige programmer, der understøtter læsning af 3D-filer.

Objekter i et PLY-format beskrives af en samling af hjørner, flader og andre elementer, sammen med egenskaber som farve og normal retning, der kan knyttes til disse elementer. Andre egenskaber, der også kan gemmes med objektet, omfatter:

* Overfladenormaler

* tekstur koordinater

*gennemsigtighed

* rækkevidde data konfidens

* egenskaber for forsiden og bagsiden af en polygon


Et objekt repræsenteret ved PLY-format kan være resultatet af forskellige kilder såsom hånddigitaliserede objekter, polygonobjekter fra modelleringsapplikationer, rækkeviddedata, trekanter fra marcherende terninger, terrændata og radiositetsmodeller.

## Kort historie

PLY-formatet blev udviklet i 1990'erne af Greg Turk og andre i Stanfords grafiklaboratorium, og det er derfor, det også er kendt som Stanford Triangle Format. Filformatet har siden da version 1.0, og der blev ikke foretaget yderligere ændringer.

## PLY filformat

Et simpelt PLY-objekt består af en samling af elementer til repræsentation af objektet. Den består af en liste over (x,y,z) tripler af et hjørner og en liste over flader, der faktisk er indekser i listen over knudepunkter. Hjørner og ansigter er to eksempler på elementer, og størstedelen af PLY-filen består af disse to elementer. Nye egenskaber kan også oprettes og knyttes til et objekts elementer, men disse bør tilføjes på en sådan måde, at gamle programmer ikke går i stykker, når disse nye egenskaber stødes på. Sådanne egenskaber kan også kasseres ved at læse applikationer. Desuden kan nye elementer oprettes, og egenskaber kan også defineres med dette element.

### Filstruktur

Filstrukturen for et PLY-filformat er som følger:

|Felt
---|
|Filhoved
|Vertex Liste
|Ansigtsliste
|Liste over andre elementer

#### Eksempelstruktur

Vi vil bruge følgende eksempel nedenfor i vores efterfølgende diskussion til forskellige dele af et PLY-filformat.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Filhoved

PLY filformat header består af ASCII tekst for både ASCII og det binære format. Starten og slutningen af overskriftssektionen er identificeret ved ply og end-header nøgleord. Starten af headeren har det magiske ord ply, som bruges til genkendelse af PLY-filformat af læsere. Den næste linje viser versionsnummeret for denne fil. Kommentarer i et PLY-filformat starter med kommentarnøgleord i starten af hver kommentarlinje.

#### Element søgeord

Elementnøgleordet fortæller derefter, hvad der er inde i filen. Det efterfølges af egenskaber for den specifikke elementtype, hvor hver egenskab har sin egenskabstype og rækkefølge angivet som vist nedenfor:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

I dette særlige eksempel har det specifikke vertex-element 3 egenskaber af typen float med deres rækkefølge angivet.

#### Typer af datatyper

Der er to typer datatyper, som en ejendom kan have.

Scalar': De skalære datatyper er som vist nedenfor:

|#Navn|#Type|#Antal bytes
|tegn|karakter|1
|uchar|usigneret tegn|1
|kort|kort heltal|2
|short|usigned kort heltal|2
|int|Heltal|4
|uint|usigneret heltal|4
|float|enkeltpræcisionsflyder|4
|dobbelt|dobbelt præcisionsflyder|8

`Liste`: Der er en speciel form for egenskabsdefinitioner, der bruger listedatatypen. Et eksempel på dette er fra kubefilen ovenfor:

`egenskabsliste uchar int vertex_index`

Det betyder, at egenskaben vertex_index først indeholder et usigneret tegn, der fortæller, hvor mange indekser egenskaben indeholder, efterfulgt af en liste, der indeholder så mange heltal. Hvert heltal i denne liste med variabel længde er et indeks til et toppunkt.

## Referencer ##

* [PLY-filformat](http://paulbourke.net/dataformats/ply/)

* [PLY - Af Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))


