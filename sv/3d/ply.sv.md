{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "fil", "tillägg", "format", "3D-filformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om PLY-filformat och API:er som kan skapa och öppna PLY-filer.",
  "title" :"PLY - Polygon 3D-filformat",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en PLY fil?

PLY, Polygon File Format, representerar 3D-filformat som lagrar grafiska objekt som beskrivs som en samling polygoner. Syftet med detta filformat var att skapa en enkel och lättillgänglig filtyp som är tillräckligt generell för att vara användbar för ett brett utbud av modeller. PLY filformat kommer som ASCII samt binärt format för kompakt lagring och för snabb lagring och laddning. Filformatet används av olika applikationer som ger stöd för läsning av 3D-filer.

Objekt i ett PLY-format beskrivs av en samling av hörn, ytor och andra element, tillsammans med egenskaper som färg och normal riktning som kan fästas på dessa element. Andra egenskaper som också kan lagras med objektet inkluderar:

* Ytnormaler
* texturkoordinater
* transparens
* intervalldatasäkerhet
* egenskaper för fram- och baksidan av en polygon

Ett objekt som representeras av PLY-format kan vara resultatet av olika källor såsom handdigitaliserade objekt, polygonobjekt från modelleringsapplikationer, avståndsdata, trianglar från marschkuber, terrängdata och radiositetsmodeller.

## Kortfattad bakgrund

PLY-formatet utvecklades på 1990-talet av Greg Turk och andra i Stanfords grafiklab och det är därför det också är känt som Stanford Triangle Format. Filformatet har version 1.0 sedan dess och inga ytterligare ändringar har gjorts.

## PLY filformat

Ett enkelt PLY-objekt består av en samling av element för representation av objektet. Den består av en lista med (x,y,z) trippel av ett hörn och en lista med ansikten som faktiskt är index i listan över hörn. Vertices och faces är två exempel på element och majoriteten av PLY-filen består av dessa två element. Nya egenskaper kan också skapas och kopplas till elementen i ett objekt, men dessa bör läggas till på ett sådant sätt att gamla program inte går sönder när dessa nya egenskaper påträffas. Sådana egenskaper kan också förkastas genom att läsa applikationer. Dessutom kan nya element skapas och egenskaper kan definieras även med detta element.

### Filstruktur

Filstrukturen för ett PLY-filformat är som följer:

|Fält
---|
|Filhuvud
|Vertexlista
|Ansiktslista
|Lista över andra element

#### Exempelstruktur

Vi kommer att använda följande exempel nedan i vår efterföljande diskussion för olika delar av ett PLY-filformat.

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

#### Filhuvud

PLY-filformatshuvudet består av ASCII-text för både ASCII- och binärformatet. Början och slutet av rubriksektionen identifieras med nyckelord för ply och end-header. Början av rubriken har det magiska ordet ply som används för att känna igen PLY-filformat av läsare. Nästa rad visar versionsnumret för denna fil. Kommentarer i ett PLY-filformat börjar med kommentar nyckelord i början av varje kommentarsrad.

#### Element nyckelord

Elementnyckelordet berättar sedan vad som finns inuti filen. Den följs av egenskaper för den specifika elementtypen där varje egenskap har sin egenskapstyp och ordning specificerad enligt nedan:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

I det här specifika exemplet har det specifika vertexelementet 3 egenskaper av typen float med deras ordning specificerad.

#### Typer av datatyper

Det finns två typer av datatyper som en egenskap kan ha.

`Skalär`: De skalära datatyperna visas nedan:

|#Namn|#Typ|#Antal byte
|tecken|tecken|1
|uchar|osignerat tecken|1
|kort|kort heltal|2
|short|osignerat kort heltal|2
|int|Heltal|4
|uint|osignerat heltal|4
|float|single-precision float|4
|dubbel|dubbel precisionsflyttning|8

`List`: Det finns en speciell form av egenskapsdefinitioner som använder listdatatypen. Ett exempel på detta är från kubfilen ovan:

`egenskapslista uchar int vertex_index`

Det betyder att egenskapen "vertex_index" först innehåller ett osignerat tecken som talar om hur många index egenskapen innehåller, följt av en lista som innehåller så många heltal. Varje heltal i denna lista med variabel längd är ett index till en vertex.

## Referenser ##

* [PLY-filformat](http://paulbourke.net/dataformats/ply/)
* [PLY - av Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))

