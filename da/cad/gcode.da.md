{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE-fil - Hvad er en .gcode-fil, og hvordan åbner man den?",
   "description":"Lær om GCODE-filformat og API'er, der kan oprette og åbne GCODE-filer.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-da",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Hvad er en GCODE fil?

En **GCODE-fil** er en almindelig tekstfil, der indeholder instruktioner til styring af computeriserede værktøjsmaskiner og 3D-printere; G-kode, eller Geometrisk kode, er et sprog, der bruges til at styre bevægelser og handlinger af **CNC (Computer Numerical Control)** maskiner; CNC-maskiner omfatter fræsemaskiner, drejebænke, routere og 3D-printere.

G-kode kommandoer er skrevet i specifik syntaks, typisk bestående af bogstaver og tal; hver kommando instruerer maskinen til at udføre specifik handling, såsom at flytte værktøjet til en bestemt position, skifte værktøj eller justere hastigheden.

G-kode genereres ofte af **CAM (Computer-Aided Manufacturing)**-software; CAM-software tager 3D-modeller eller 2D-design og genererer tilsvarende værktøjsbaner og G-kode instruktioner; G-kode-filen indlæses derefter i CNC-maskine eller 3D-printer til udførelse.

G-code-filer har typisk .nc eller .gcode filtypenavnet, f.eks. program.nc eller print.gcode.

## GCODE-filstruktur:

GCODE-filer er almindelige tekstfiler, hvor hver linje indeholder en bestemt kommando; disse kommandoer spænder fra styring af maskinens bevægelse til justering af temperatur, hastighed og andre parametre, der er afgørende for fremstilling af et objekt.

Syntaksen for GCODE involverer en kombination af bogstaver og tal; hver repræsenterer særskilt handling eller parameter; Almindelige kommandoer omfatter G0 og G1 til bevægelse, M3 og M5 til spindelstyring og S og F til henholdsvis hastigheds- og tilspændingsjusteringer.

## GCODE Generation:

Slicing-software såsom **Simplify3D** og **Slic3r**, oversætter tegninger med computerstøttet design (CAD) til GCODE; CAD-software bruges til at skabe 3D-modeller, som derefter eksporteres i formater som STL; udskæringssoftwaren tager disse modeller og genererer GCODE-fil, der specificerer detaljer såsom laghøjde, udskrivningshastighed og temperaturindstillinger.

## Eksempel på GCODE

Her er et simpelt eksempel på G-kode til flytning af CNC-maskine:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Hvordan åbner jeg filen GCODE?

For at åbne en G-kode fil kan du bruge forskellige typer software afhængigt af dine behov.

Hvis du genererede G-kode til 3D-printer; du kan åbne den ved hjælp af software, der fulgte med din 3D-printer eller dedikeret udskæringssoftware; eksempler inkluderer **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** eller **Repetier-Host**; disse programmer har ofte en brugervenlig grænseflade, der giver dig mulighed for at indlæse og visualisere G-kode.

GCODE-filer er almindelig tekst, så du kan åbne dem med en hvilken som helst teksteditor; almindelige tekstredigeringsprogrammer inkluderer **Notesblok (på Windows)**, **TextEdit (på macOS)** eller **Gedit (på Linux)**; **højreklik** på G-kode-filen, vælg **Åbn med,** og vælg en teksteditor.

