{
  "date": "2020-03-16",
  "keywords": [
"STL fails",
"Formāts",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par STL failu formātu un API, kas var izveidot un atvērt STL failus.",
  "title": "STL faila formāts",
  "linktitle": "STL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-st-lvl"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir STL fails?

STL, stereolitrogrāfijas saīsinājums, ir maināms faila formāts, kas attēlo trīsdimensiju virsmas ģeometriju. Faila formāts tiek izmantots vairākās jomās, piemēram, ātrajā prototipā, 3D drukāšanā un datorizētā ražošanā. Tas attēlo virsmu kā mazu trīsstūru virkni, ko sauc par skaldnēm, kur katra skaldne ir aprakstīta ar perpendikulāru virzienu un trim punktiem, kas attēlo trīsstūra virsotnes. Lietojumprogrammas izmanto iegūtos datus, lai noteiktu 3D formas šķērsgriezumu, ko veido ražotājs. STL faila formātā nav pieejama informācija par krāsu, tekstūras vai citu izplatītu [CAD](/cad/) modeļa atribūtu attēlojumu.

## Īsa vēsture ##

The development of STL file format dates back to 1987. To izstrādāja 3D Systems izmantošanai komerciālos 3D printeros. 2009. gadā tika piedāvāta pārskatīta STL faila formāta versija, kas pazīstama kā STL 2.0, ar faila formāta atjauninājumiem.

## Faila formāta specifikācijas ##

STL fails attēlo virsmas ģeometriju, izmantojot šķautnes. Fasetes nosaka 3D objekta virsmu un ir unikāli identificētas ar normālu vienību, kas ir taisne, kas ir perpendikulāra trijstūrim ar garumu 1,0, un trīs virsotnes. Katrai šķautnei kopā ir saglabāti 12 skaitļi kā parastā, un katra virsotne ir norādīta ar trim koordinātām. StL failā nav nekādas mēroga informācijas; koordinātas ir patvaļīgās vienībās.

STL faila formāta specifikācijas var pārbaudīt no diviem aspektiem.

### Aspektu orientācija ###

Fasetes orientāciju nosaka normālās vienības virziens un virsotņu saraksta secība. Fasešu orientācija ir norādīta divos veidos:

* Parastā virziens ir uz āru

* Virsotnes ir norādītas pretēji pulksteņrādītāja virzienam no ārpuses, ievērojot labās rokas likumu.


### Noteikums no virsotnes līdz virsotnei ###

Saskaņā ar šo noteikumu katram trīsstūrim ir divas virsotnes ar katru blakus esošo trīsstūri. Tādējādi viena trijstūra virsotne nevar atrasties cita trijstūra malā.

## Failu formāti ##

STL ir pieejams ASCII, kā arī bināros attēlojumos kompaktajam faila formātam.

### STL ASCII formāts ###

STL faila formāta ASCII versija ir rakstīta vienkāršā ASCII. Tomēr tā lielā izmēra dēļ faila formāts nav izvēlēts kā vēlamais lietošanai. ASCII STL faila sintakse ir šāda:
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
The bold face words represent keywords that should always be lowercase. Symbols in italics are variables which are to be replaced with user-specified values.  The numerical data in the **facet normal** and **vertex** lines are single precision floats, for example, 1.23456E+789. **normālas šķautnes** koordinātei var būt mīnusa zīme; **virsotnes** koordinātas nedrīkst.

### STL binārais formāts ###

Binārais formāts izmanto IEEE veselu skaitļu un peldošā komata skaitlisko attēlojumu. Faila formāts ir attēlots šādi:

|Lauks|Informācija|
---|---|
|Galvene|80 rakstzīmes|
|Trijstūru skaits|4 baitu mazs endian neparakstīts vesels skaitlis|
|Dati par katru trīsstūri|12 32 bitu peldošā komata skaitļi|

Tālāk ir parādīts detalizētāks faila formāta skats.

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

## Atsauces Nr.

* [STL formāts] (http://www.fabbers.com/tech/STL_Format)

* [STL — Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))


