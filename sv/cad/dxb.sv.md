{
"datum": "2023-05-10",
  "keywords": [
"dxb-fil",
"vad är en dxb-fil",
"vilket är formatet på dxb-filen",
"vad innehåller dxb-filen",
"fil",
"dxb filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "DXB-filformat - Drawing Exchange Binary",
  "description":"Läs mer om DXB-format och API:er som kan skapa och öppna DXB-filer.",
  "linktitle": "DXB",
  "menu": {
    "docs": {
      "identifier": "cad-dxb",
      "parent": "cad"
}
},
"lastmod": "2023-05-10"
}

## Vad är en DXB fil?

DXB står för Drawing Exchange Binary, vilket är ett filformat som används i programvara för datorstödd design (CAD). DXB-filer innehåller binära data som representerar 2D vektorgrafik och används för att utbyta ritningar mellan olika CAD-program. De skapas vanligtvis genom att exportera ritningar från CAD-program i DXB-format och sedan importera det till ett annat CAD-program.

DXB-format är mindre vanligt idag än andra CAD-filformat som DXF eller DWG. Vissa äldre CAD-program kan dock fortfarande använda DXB som filformat för att exportera eller importera ritningar.

Om du har en DXB-fil och behöver visa eller redigera den, behöver du CAD-program som stöder DXB-format. Några exempel på CAD-program som stöder DXB inkluderar AutoCAD, DraftSight och LibreCAD.

## DXB-filformat - Mer information

DXB (Drawing Exchange Binary) är en binär version av filformatet DXF (Drawing Exchange Format), som är ett standardformat för utbyte av CAD-ritningar mellan olika program.

DXB-filer innehåller binära data som representerar 2D-vektorgrafik precis som DXF-filer. DXB-filer är dock mer kompakta och snabbare att ladda än DXF-filer eftersom de lagras i binärt format istället för vanlig text.

För att skapa en DXB-fil kan ett CAD-program exportera ritning i DXB-format, vilket genererar binär fil som kan läsas av andra CAD-program som stöder DXB. För att importera DXB-filer kan ett CAD-program läsa binär data och konvertera den till sitt eget interna format för redigering.

## Vilket är formatet på filen DXB?

DXB (Drawing Exchange Binary) filformat är ett binärt filformat, vilket innebär att det består av binära data som kan tolkas direkt av datorn.

Det binära formatet som används av DXB är mer kompakt och snabbare att ladda än det textbaserade DXF-filformatet (Drawing Exchange Format) som också används för att utbyta CAD-ritningar mellan olika program.

Strukturen för DXB-filen består av serier av binära poster som var och en innehåller rubrik och data som representerar ett enda objekt eller entitet i ritningen. Rubriken innehåller information om typen av objekt eller enhet som representeras av data samt dess storlek och andra egenskaper.

Data i DXB-filen är organiserad hierarkiskt, med poster på högre nivå som innehåller referenser till poster på lägre nivå som representerar underobjekt eller komponenter i ritningen. Till exempel kan en post som representerar polylinjen innehålla referenser till poster som representerar individuella linjesegment som utgör polylinjen.

## Vad innehåller DXB-filen?

DXB-filen (Drawing Exchange Binary) innehåller binära data som representerar 2D-vektorgrafik som linjer, bågar, cirklar, text och andra geometriska former som utgör CAD-ritning.

När CAD-program exporterar en ritning till DXB-format, skapar det en binär fil som innehåller all information som behövs för att återskapa ritningen i ett annat CAD-program som stöder DXB. Detta inkluderar information om plats, storlek, färg och stil för varje objekt i ritningen samt eventuell text eller anteckningar som kan inkluderas.

Eftersom DXB-filer lagras i binärt format är de vanligtvis mindre i storlek och snabbare att ladda än DXF-filer (Drawing Exchange Format), som lagras i vanlig text. DXB-filer kan dock bara läsas av CAD-program som stöder DXB-formatet, medan DXF-filer kan läsas av fler program.

## Referenser
* [DXB-filformat](http://web.archive.org/web/20060824054154/https://www.autodesk.com/techpubs/autocad/acadr14/dxf/the_dxb_file_format_al_u05_b.htm)

