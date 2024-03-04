{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE failas – kas yra .gcode failas ir kaip jį atidaryti?",
   "description":"Sužinokite apie GCODE failo formatą ir API, kurios gali kurti ir atidaryti GCODE failus.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-lt",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Kas yra GCODE failas?

**GCODE failas** yra paprasto teksto failas, kuriame yra kompiuterinių staklių ir 3D spausdintuvų valdymo instrukcijos; G kodas arba geometrinis kodas yra kalba, naudojama valdyti **CNC (kompiuterinio skaitmeninio valdymo)** mašinų judesius ir veiksmus; CNC staklės apima frezavimo stakles, tekinimo stakles, maršrutizatorius ir 3D spausdintuvus.

G kodo komandos parašytos specifine sintaksė, kurią paprastai sudaro raidės ir skaičiai; kiekviena komanda nurodo mašinai atlikti konkretų veiksmą, pvz., perkelti įrankį į tam tikrą padėtį, pakeisti įrankį arba reguliuoti greitį.

G kodą dažnai generuoja **CAM (kompiuterinė gamyba)** programinė įranga; CAM programinė įranga paima 3D modelį arba 2D dizainą ir generuoja atitinkamas įrankių juostas bei G kodo instrukcijas; Tada G kodo failas įkeliamas į CNC mašiną arba 3D spausdintuvą vykdyti.

G kodo failai paprastai turi .nc arba .gcode failo plėtinį, pavyzdžiui, program.nc arba print.gcode.

## GCODE failo struktūra:

GCODE failai yra paprasto teksto failai, kurių kiekvienoje eilutėje yra konkreti komanda; Šios komandos svyruoja nuo mašinos judėjimo valdymo iki temperatūros, greičio ir kitų parametrų, būtinų objekto gamybai, reguliavimo.

GCODE sintaksė apima raidžių ir skaičių derinį; kiekvienas reiškia atskirą veiksmą arba parametrą; Įprastos komandos yra G0 ir G1 judėjimui, M3 ir M5 suklio valdymui ir S ir F atitinkamai greičio ir pastūmos reguliavimui.

## GCODE karta:

Pjaustymo programinė įranga, pvz., **Simplify3D** ir **Slic3r**, verčia kompiuterinio projektavimo (CAD) brėžinius į GCODE; CAD programinė įranga naudojama kuriant 3D modelius, kurie vėliau eksportuojami tokiais formatais kaip STL; pjaustymo programinė įranga paima šiuos modelius ir sugeneruoja GCODE failą, kuriame nurodoma tokia informacija kaip sluoksnio aukštis, spausdinimo greitis ir temperatūros nustatymai.

## GCODE pavyzdys

Čia yra paprastas G kodo, skirto perkelti CNC mašiną, pavyzdys:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Kaip atidaryti GCODE failą?

Norėdami atidaryti G kodo failą, galite naudoti įvairių tipų programinę įrangą, atsižvelgiant į jūsų poreikius.

Jei sugeneravote 3D spausdintuvo G kodą; galite atidaryti naudodami programinę įrangą, gautą su 3D spausdintuvu, arba specialią pjaustymo programinę įrangą; pavyzdžiai: **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** arba **Repetier-Host**; Šios programos dažnai turi patogią sąsają, leidžiančią įkelti ir vizualizuoti G kodą.

GCODE failai yra paprastas tekstas, todėl galite juos atidaryti naudodami bet kurią teksto rengyklę; įprastos teksto rengyklės apima **Notepad (sistemoje Windows)**, **TextEdit (sistemoje macOS)** arba **Gedit (sistemoje Linux)**; tiesiog **dešiniuoju pelės mygtuku spustelėkite** G kodo failą, pasirinkite **Atidaryti naudojant** ir pasirinkite teksto rengyklę.

