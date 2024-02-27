{
  "date": "2020-03-16",
  "keywords": [
"STL fil",
"Format",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om STL filformat og API'er, der kan oprette og åbne STL filer.",
  "title": "STL filformat",
  "linktitle": "STL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-st-dal"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er STL fil?

STL, forkortelse for stereolitrography, er et udskifteligt filformat, der repræsenterer 3-dimensionel overfladegeometri. Filformatet finder sin anvendelse inden for flere områder, såsom hurtig prototyping, 3D-print og computerstøttet fremstilling. Det repræsenterer en overflade som en række små trekanter, kendt som facetter, hvor hver facet er beskrevet med en vinkelret retning og tre punkter, der repræsenterer trekantens hjørner. Resulterende data bruges af applikationer til at bestemme tværsnittet af den 3D-form, der skal bygges af fabberen. Der er ingen tilgængelige oplysninger i STL-filformatet til repræsentation af farve, tekstur eller andre almindelige [CAD](/cad/)-modelattributter.

## Kort historie ##

The development of STL file format dates back to 1987. Det blev udviklet af 3D Systems til dets brug i kommercielle 3D-printere. En revideret version af STL-filformatet, kendt som STL 2.0, blev foreslået i 2009 med opdateringer til filformatet.

## Filformatspecifikationer ##

En STL-fil repræsenterer en overfladegeometri ved hjælp af facetter. Facetterne definerer overfladen af et 3D-objekt og identificeres entydigt af en enhedsnormal, som er en linje vinkelret på trekanten med en længde på 1,0, og med tre spidser. Der er i alt 12 numre gemt for hver facet som Normal, og hvert hjørne er specificeret med tre koordinater hver. StL-filen indeholder ingen skalainformation; koordinaterne er i vilkårlige enheder.

Specifikationerne for STL-filformat kan undersøges ud fra følgende to aspekter.

### Facetorientering ###

Orienteringen af en facet bestemmes af retningen af enhedsnormalen og rækkefølgen, hvori hjørnerne er opført. Facetternes orientering er specificeret på to måder som følger:

* Normalens retning er udad

* Hjørnerne er opstillet i rækkefølge mod uret udefra, i overensstemmelse med højrehåndsreglen.


### Vertex to Vertex-regel ###

Ifølge denne regel deler hver trekant to hjørner med hver af dens tilstødende trekanter. Et toppunkt i en trekant kan således ikke ligge på siden af en anden trekant.

## Filformater ##

STL er tilgængelig i ASCII samt binære repræsentationer til kompakt filformat.

### STL ASCII-format ###

ASCII-versionen af STL-filformatet er skrevet i almindelig ASCII. På grund af dens store størrelse er filformatet dog ikke valgt som det foretrukne format til brug. Syntaksen for en ASCII STL-fil er som følger:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
The bold face words represent keywords that should always be lowercase. Symbols in italics are variables which are to be replaced with user-specified values.  The numerical data in the **facet normal** and **vertex** lines are single precision floats, for example, 1.23456E+789. En **facet normal** koordinat kan have et førende minustegn; en **vertex**-koordinat må ikke.

### STL binært format ###

Det binære format bruger IEEE-heltals- og flydende numerisk repræsentation. Filformatet er repræsenteret som følger:

|Felt|Info|
---|---|
|Overskrift|80 tegn|
|Antal trekanter|4-byte lille endian usigneret heltal|
|Data for hver trekant|12 32-bit flydende kommatal|

En mere uddybet visning af filformatet er som vist nedenfor.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Referencer ##

* [STL-formatet](http://www.fabbers.com/tech/STL_Format)

* [STL - af Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))


