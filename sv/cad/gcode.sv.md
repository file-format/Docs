{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE-fil – Vad är en .gcode-fil och hur öppnar man den?",
   "description":"Lär dig om GCODE-filformat och API:er som kan skapa och öppna GCODE-filer.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-sv",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Vad är en GCODE fil?

En **GCODE-fil** är en vanlig textfil som innehåller instruktioner för att styra datoriserade verktygsmaskiner och 3D-skrivare; G-kod, eller Geometrisk kod, är ett språk som används för att kontrollera rörelser och handlingar hos **CNC (Computer Numerical Control)**-maskiner; CNC-maskiner inkluderar fräsmaskiner, svarvar, routrar och 3D-skrivare.

G-kodkommandon skrivs i specifik syntax som vanligtvis består av bokstäver och siffror; varje kommando instruerar maskinen att utföra specifik åtgärd som att flytta verktyget till en viss position, byta verktyg eller justera hastigheten.

G-kod genereras ofta av programvaran **CAM (Computer-Aided Manufacturing)**; CAM-programvaran tar 3D-modell eller 2D-design och genererar motsvarande verktygsbanor och G-kodinstruktioner; G-kodfilen laddas sedan in i CNC-maskin eller 3D-skrivare för exekvering.

G-code-filer har vanligtvis filändelsen .nc eller .gcode, till exempel program.nc eller print.gcode.

## GCODE-filstruktur:

GCODE-filer är vanliga textfiler där varje rad innehåller ett specifikt kommando; dessa kommandon sträcker sig från att kontrollera maskinens rörelser till att justera temperatur, hastighet och andra parametrar som är avgörande för tillverkning av ett objekt.

Syntaxen för GCODE involverar en kombination av bokstäver och siffror; var och en representerar distinkt handling eller parameter; Vanliga kommandon inkluderar G0 och G1 för rörelse, M3 och M5 för spindelstyrning, och S och F för hastighets- respektive matningshastighetsjusteringar.

## GCODE Generation:

Skivningsprogram som **Simplify3D** och **Slic3r**, översätter ritningar med datorstödd design (CAD) till GCODE; CAD-programvara används för att skapa 3D-modeller, som sedan exporteras i format som STL; skivningsmjukvaran tar dessa modeller och genererar GCODE-fil som anger detaljer som lagerhöjd, utskriftshastighet och temperaturinställningar.

## Exempel på GCODE

Här är ett enkelt exempel på G-kod för att flytta CNC-maskin:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Hur öppnar man filen GCODE?

För att öppna en G-kodfil kan du använda olika typer av programvara beroende på dina behov.

Om du genererade G-kod för 3D-skrivare; du kan öppna den med programvara som följde med din 3D-skrivare eller dedikerad skivningsprogramvara; exempel inkluderar **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** eller **Repetier-Host**; dessa program har ofta ett användarvänligt gränssnitt som låter dig ladda och visualisera G-kod.

GCODE-filer är vanlig text så att du kan öppna dem med vilken textredigerare som helst; vanliga textredigerare inkluderar **Anteckningar (på Windows)**, **TextEdit (på macOS)** eller **Gedit (på Linux)**; **högerklicka** på G-code-filen, välj **Öppna med** och välj en textredigerare.

