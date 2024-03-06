{
  "date": "2019-10-11",
  "keywords": [
"shp failu",
"shp faila formātā",
"kas ir shp fails",
"failu",
"shp piemērs",
"shp faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SHP — ESRI Shapefile",
  "description": "Uzziniet par SHP failu formātu un API, kas var izveidot un atvērt SHP failus.",
  "linktitle": "SHP",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-lvp"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir SHP fails?

SHP ir faila paplašinājums vienam no primārajiem failu tipiem, ko izmanto ESRI Shapefile attēlošanai. Tas attēlo ģeotelpisko informāciju vektordatu veidā, ko izmantos ģeogrāfiskās informācijas sistēmu (GIS) lietojumprogrammās. Formāts ir izstrādāts kā atvērtas specifikācijas, lai veicinātu sadarbspēju starp ESRI un citiem programmatūras produktiem.

## Datu reprezentācija

Kā minēts, formas faila formāts apraksta datu kopas ģeotelpisko informāciju kā vektora elementus. Šīs vektora funkcijas ietver:

* punkti

* līnijas

* daudzstūri


Šie elementi kombinācijā var attēlot gandrīz jebkura veida formas, piemēram, ūdens akas, valsts robežas, telpiskos punktus, upju plūsmu, ezerus utt. Katram vektora elementam var būt atribūti, kas faktiski nosaka šī objekta mērķi. Piemēram, formas failam, kurā ir Losandželosas pilsētas, var būt pilsētas nosaukums un temperatūra kā atribūti, kas sniedz jēgpilnu telpisko datu attēlojumu.

## Saistītie faili

Programmatūras lietojumprogrammas nevar izmantot atsevišķu shp failu, lai saprastu tajā ietvertos datus. Lai izprastu šādā failā ietverto informāciju, shape fails izmanto šādus papildu obligātos failus.

* shx fails - indeksa fails

* dbf fails - dBASE fails, kurā tiek saglabāti visi galvenā faila formu atribūti

* prj fails - saglabā faila projekta informāciju


Var būt arī citi izvēles faili, kuriem ir tāds pats nosaukums kā galvenajam failam.

## SHP faila formāta specifikācijas

Shapefile atvērtās specifikācijas ir pieejamas tiešsaistē no ESRI [Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) formātā, un tajās ir sīki izstrādāta faila vispārējā struktūra. Informācija galvenajā .shp failā sastāv no galvenēm un ierakstiem. Fiksēta garuma faila galvenei seko mainīga garuma ieraksti, kur katrs ieraksts sastāv no fiksēta garuma ieraksta galvenes, kam seko mainīga garuma ieraksta saturs.

### Galvenā SHP faila galvene

Galvenā faila galvene sākas no faila sākuma un ir 100 baiti garš. Šī galvenā faila galvenes struktūra kopā ar baitu pozīciju, vērtību, veidu un baitu secību ir tāda, kā parādīts nākamajā tabulā.


|Baiti|lauks|vērtība|tips|baitu secība
---|---|---|---|---|
|0-3|Faila kods|9994|Vesels skaitlis|Big Endian
|4-23|Nelietots|0|Vesels skaitlis|Big Endian
|24-27|Faila garums|Faila garums|Vesels skaitlis|Big Endian
|28-31|Versija|1000|Vesels skaitlis|Little Endian
|32-35|Formas tips|Formas tips|Vesels skaitlis|Mazais endijs
|36-67|Minimālais ierobežojošais taisnstūris|Xmin, Ymin, Xmax un Ymax|double|Little Endian
|68-83|Ierobežojoša kaste|Zmin, Zmax|dubults|Mazais endians
|84-99|Ierobežojošais laukums|Mmin, Mmax|dubultais|

Jāatzīmē, ka faila garuma vērtība ir faila kopējais garums 16 bitu vārdos, kas ietver arī piecdesmit 16 bitu vārdus, kas veido galveni.

#### Formu veidi

Formu tipu lauka vērtības iepriekšējā tabulā ir šādas:


|Vērtība|Formas veids
---|---|
|0|Null Shape
|1|Punkts
|3|Polyline
|5|Daudzstūris
|8|Daudzpunktu
|11|PunktsZ
|13|PolyLineZ
|15|DaudzstūrisZ
|18|MultiPointZ
|21|PunktsM
|23|PolyLineM
|25|DaudzstūrisM
|28|MultiPointM
|31|MultiPatch

### Datu ieraksti ###

Pēc galvenās faila galvenes seko mainīga garuma ieraksti, kur katrs ieraksts sastāv no fiksēta garuma ieraksta galvenes, kam seko mainīga garuma ieraksta saturs.

#### Ieraksta galvene ####

Ieraksta galvenē ir informācija par ieraksta numuru un ieraksta satura garumu fiksētā 8 baitu garumā. Ieraksta galvenes organizācija ir šāda:


|Baiti|lauks|vērtība|tips|baitu secība
---|---|---|---|---|
|0-3|Ieraksta numurs|Ieraksta numurs|Vesels skaitlis|Liels
|4-7|Ieraksta garums|Ieraksta garums|Vesels skaitlis|Liels

#### Ierakstīt saturu ####

Shape faila ieraksta saturs sastāv no formas tipa, kam seko šīs formas ģeometriskie dati. Formas veids 0 apzīmē nulles formu, kurai nav formas ģeometrisku datu. Ieraksta satura garums atspoguļo formas daļas un virsotnes. Ņemsim punkta formas tipa piemēru, lai precizētu, kā ieraksts satur informāciju par šādu formas tipu.

Punkts apzīmē noteiktu ģeogrāfisko atrašanās vietu X,Y secībā, kur katra koordināta ir attēlota ar dubultas precizitātes vērtību. Nākamajā tabulā parādīts punkta formas veida izkārtojums.


|Baiti|Formas veids|Vērtība|Tips|Numurs|Baitu secība
---|---|---|---|---|---|
|0-3|Formas veids|1|Vesels skaitlis|1|Maz
|4-11|X|X|dubultais|1|Maz
|12-19|Y|Y|double|1|Maz

Examples of other shape types can be found the ESRI technical description document.

## Atsauces Nr.

* [ESRI Shapefile tehniskais apraksts](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf), ESRI


