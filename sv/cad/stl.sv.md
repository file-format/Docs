{
  "date" : "2020-03-16",
  "keywords" :[ "STL-fil", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om STL-filformat och API:er som kan skapa och öppna STL-filer.",
  "title" :"STL-filformat",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är STL fil?

STL, förkortning för stereolitrografi, är ett utbytbart filformat som representerar 3-dimensionell ytgeometri. Filformatet finner sin användning inom flera områden som snabb prototypframställning, 3D-utskrift och datorstödd tillverkning. Den representerar en yta som en serie små trianglar, så kallade fasetter, där varje fasett beskrivs med en vinkelrät riktning och tre punkter som representerar triangelns hörn. Resulterande data används av applikationer för att bestämma tvärsnittet av 3D-formen som ska byggas av fabbern. Det finns ingen information tillgänglig i STL-filformatet för representation av färg, textur eller andra vanliga [CAD](/sv/cad/) modellattribut.

## Kortfattad bakgrund ##

Utvecklingen av STL-filformat går tillbaka till 1987. Det utvecklades av 3D Systems för dess användning i kommersiella 3D-skrivare. En reviderad version av STL-filformatet, känt som STL 2.0, föreslogs 2009 med uppdateringar av filformatet.

## Filformatspecifikationer ##

En STL-fil representerar en ytgeometri med hjälp av fasetter. Fasetterna definierar ytan på ett 3D-objekt och identifieras unikt av en enhetsnormal, som är en linje vinkelrät mot triangeln med längden 1,0 och av tre hörn. Det finns totalt 12 nummer lagrade för varje fasett som Normal och varje vertex specificeras av tre koordinater vardera. StL-filen innehåller ingen skalinformation; koordinaterna är i godtyckliga enheter.

Specifikationerna för STL-filformat kan granskas utifrån följande två aspekter.

### Fasettorientering ###

Orienteringen av en fasett bestäms av riktningen för enhetsnormalen och ordningen i vilken hörnen listas. Fasetternas orientering specificeras på två sätt som följer:

* Normalens riktning är utåt
* Topparna är listade i moturs ordning utifrån, i enlighet med högerhandsregeln.

### Vertex to Vertex Regel ###

Enligt denna regel delar varje triangel två hörn med var och en av sina intilliggande trianglar. Således kan en vertex av en triangel inte ligga på sidan av en annan triangel.

## Filformat ##

STL är tillgängligt i ASCII samt binära representationer för kompakt filformat.

### STL ASCII-format ###

ASCII-versionen av STL-filformatet är skriven i vanlig ASCII. Men på grund av dess stora storlek väljs inte filformatet som föredraget format för användning. Syntaxen för en ASCII STL-fil är som följer:
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
De fetstilta orden representerar nyckelord som alltid ska vara gemener. Symboler i kursiv stil är variabler som ska ersättas med användarspecificerade värden. De numeriska data i linjerna **facettnormal** och **vertex** är enkelprecisionsflottor, till exempel 1.23456E+789. En **fasettnormal**-koordinat kan ha ett inledande minustecken; en **vertex**-koordinat kanske inte.

### STL binärt format ###

Det binära formatet använder IEEE heltal och flyttals numerisk representation. Filformatet representeras enligt följande:

|Fält|Information|
---|---|
|Rubrik|80 tecken|
|Antal trianglar|4-byte litet endian heltal utan tecken|
|Data för varje triangel|12 32-bitars flyttalsnummer|

En mer genomarbetad bild av filformatet visas nedan.

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

## Referenser ##

* [STL-formatet](http://www.fabbers.com/tech/STL_Format)
* [STL - av Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))

