{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE fails — kas ir .gcode fails un kā to atvērt?",
   "description":"Uzziniet par GCODE faila formātu un API, kas var izveidot un atvērt GCODE failus.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-lv",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Kas ir GCODE fails?

**GCODE fails** ir vienkārša teksta fails, kurā ir norādījumi datorizētu darbgaldu un 3D printeru vadīšanai; G-kods jeb ģeometriskais kods ir valoda, ko izmanto, lai kontrolētu **CNC (Computer Numerical Control)** iekārtu kustības un darbības. CNC mašīnas ietver frēzēšanas mašīnas, virpas, maršrutētājus un 3D printerus.

G-koda komandas ir rakstītas īpašā sintaksē, kas parasti sastāv no burtiem un cipariem; katra komanda uzdod mašīnai veikt noteiktas darbības, piemēram, pārvietot instrumentu uz noteiktu pozīciju, mainīt instrumentu vai pielāgot ātrumu.

G-kodu bieži ģenerē **CAM (Computer-Aided Manufacturing)** programmatūra; CAM programmatūra ņem 3D modeli vai 2D dizainu un ģenerē atbilstošus rīku ceļus un G-koda instrukcijas; G-koda fails pēc tam tiek ielādēts CNC iekārtā vai 3D printerī izpildei.

G-koda failiem parasti ir faila paplašinājums .nc” vai .gcode”, piemēram, program.nc” vai print.gcode”.

## GCODE faila struktūra:

GCODE faili ir vienkārša teksta faili, kuros katrā rindā ir noteikta komanda; šīs komandas svārstās no mašīnas kustības kontroles līdz temperatūras, ātruma un citu parametru pielāgošanai, kas ir būtiski objekta izgatavošanai.

GCODE sintakse ietver burtu un ciparu kombināciju; katrs attēlo atsevišķu darbību vai parametru; Kopējās komandas ietver G0 un G1 kustībai, M3 un M5 vārpstas vadībai un S un F attiecīgi ātruma un padeves regulēšanai.

## GCODE paaudze:

Sagriešanas programmatūra, piemēram, **Simplify3D** un **Slic3r**, pārvērš datorizētās projektēšanas (CAD) rasējumus GCODE; CAD programmatūra tiek izmantota, lai izveidotu 3D modeļus, kas pēc tam tiek eksportēti tādos formātos kā STL; sagriešanas programmatūra izmanto šos modeļus un ģenerē GCODE failu, norādot tādu informāciju kā slāņa augstums, drukāšanas ātrums un temperatūras iestatījumi.

## GCODE piemērs

Šeit ir vienkāršs G-koda piemērs CNC mašīnas pārvietošanai:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Kā atvērt GCODE failu?

Lai atvērtu G-koda failu, atkarībā no jūsu vajadzībām varat izmantot dažāda veida programmatūru.

Ja esat ģenerējis G-kodu 3D printerim; varat to atvērt, izmantojot 3D printera komplektācijā iekļauto programmatūru vai speciālu griešanas programmatūru; piemēri ietver **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** vai **Repetier-Host**; šīm programmām bieži ir lietotājam draudzīgs interfeiss, kas ļauj ielādēt un vizualizēt G kodu.

GCODE faili ir vienkāršs teksts, tāpēc varat tos atvērt ar jebkuru teksta redaktoru; izplatītākie teksta redaktori ietver **Notepad (operētājsistēmā Windows)**, **TextEdit (operētājsistēmā macOS)** vai **Gedit (operētājsistēmā Linux)**; vienkārši **ar peles labo pogu noklikšķiniet** uz G-koda faila, izvēlieties **Atvērt ar** un atlasiet teksta redaktoru.

