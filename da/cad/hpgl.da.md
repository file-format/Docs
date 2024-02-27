{
  "date": "2020-07-28",
  "keywords": [
"HPGL",
"Filformat",
"Åben",
"Læs",
"skab",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om HPGL filformat og API'er, der kan oprette og åbne HPGL filer.",
  "title": "HPGL-filformat - Lær af filformateksperter!",
  "linktitle": "HPGL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-hpg-dal"
}
},
  "lastmod": "2020-07-28"
}

## Hvad er HPGL fil?

En HPGFL-fil (Hewlett-Packard Graphics Language) indeholder instruktionssæt til plotterstyring udviklet af HP. HP-plottere bruger denne fil til at tegne og udskrive vektor- og rasterindhold på papiret.

### HPGL-kommando

En HPGL-kommando består af følgende.
 * En kommandosektion af alfabetet med to tegn
 * Et parameterafsnit
 * Terminator sektion

Hver parameter i filen skal opdeles med en separator i tilfælde af flere parametre.

### HPGL-kommandoeksempel

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Koordinatsystem

Koordinatsystemer består af 2-dimensionelle måleindikatorer til at lokalisere enhver specifik placering. HPGL bruger både plotterkoordinat- og brugerkoordinatsystem til dette formål.

#### Plotterkoordinatsystem

Dette koordinatsystem bruges til at plotte tegninger baseret på plotterbevægelse. En typisk XY-enhed med minimal plotterbevægelse er 0,025 mm. Det mulige udvalg af tegninger ændres med plottertyper.

#### Brugerkoordinatsystem

Brugerspecificeret koordinatsystem kan opsættes ved hjælp af skala og oprindelse. Disse konverteres til plotterkoordinater ved hjælp af IP-kommandoen og SC-kommandoen. Plottersystemkoordinater bruges som standard, hvis denne konvertering ikke udføres.

## HPGL filformat
HPGL-filer er i ASCII-format (tekstfil) og starter med få opsætningskommandoer. Dette opsætter visse parametre for plotteren til plotning. En typisk HPGL-fil ser ud som følger.

|Kommando|Betydning
---|---|
|IN;|initialiser, start et plottejob|
|IP;|indstil skaleringspunkterne (P1 og P2) til deres standardpositioner|
|SP1;|vælg pen 1|
|PU0,0;|løft pennen op og gå til startpunktet for næste handling|
|PD100,0,100,100,0,100,0,0;|sæt pennen ned og flyt til følgende steder (tegn en boks rundt om siden)|
|PU50,50;|Pen op og flyt til X,Y koordinater 50,50|
|CI25;|tegn en cirkel med radius 25|
|SS;|vælg standardtegnsættet|
|DT*,1;|indstil tekstadskilleren til stjernen, og udskriv dem ikke (1, der betyder sand)|
|PU20,80;|løft pennen og flyt til 20,80|
|LBHello World*;|tegn en etiket|

## Referencer
 * [HPGL af Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
 * [HPGL-referencevejledning](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

