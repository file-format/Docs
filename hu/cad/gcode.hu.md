{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE Fájl - Mi az .gcode fájl és hogyan nyitható meg?",
   "description":"Ismerje meg a GCODE fájlformátumot és az API-kat, amelyek GCODE-fájlokat hozhatnak létre és nyithatnak meg.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-hu",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Mi az a GCODE fájl?

A **GCODE fájl** egy egyszerű szöveges fájl, amely utasításokat tartalmaz a számítógépes szerszámgépek és 3D nyomtatók vezérléséhez; A G-kód vagy geometriai kód” egy nyelv, amelyet a **CNC (számítógépes numerikus vezérlés)** gépek mozgásának és műveleteinek vezérlésére használnak; A CNC gépek közé tartoznak a marógépek, esztergagépek, útválasztók és 3D nyomtatók.

A G-kód parancsokat meghatározott szintaxisban írják, amely jellemzően betűkből és számokból áll; minden parancs arra utasítja a gépet, hogy bizonyos műveleteket hajtson végre, mint például a szerszám mozgatása egy adott pozícióba, a szerszám megváltoztatása vagy a sebesség beállítása.

A G-kódot gyakran **CAM (Computer-Aided Manufacturing)** szoftver állítja elő; A CAM szoftver 3D-s modellt vagy 2D-s tervezést készít, és megfelelő szerszámpályákat és G-kód utasításokat generál; a G-kód fájl ezután betöltődik CNC gépbe vagy 3D nyomtatóba végrehajtásra.

A G-code fájlok általában .nc” vagy .gcode” kiterjesztéssel rendelkeznek, például program.nc” vagy print.gcode”.

## GCODE fájlszerkezet:

A GCODE fájlok egyszerű szöveges fájlok, amelyek minden sorában meghatározott parancs található; ezek a parancsok a gép mozgásának vezérlésétől a hőmérséklet, a sebesség és egyéb, egy tárgy elkészítéséhez elengedhetetlen paraméterek beállításáig terjednek.

A GCODE szintaxisa betűk és számok kombinációját foglalja magában; mindegyik külön műveletet vagy paramétert képvisel; A gyakori parancsok közé tartozik a G0 és G1 a mozgáshoz, az M3 és az M5 az orsóvezérléshez, valamint az S és F a fordulatszám és előtolás beállításához.

## GCODE generáció:

A szeletelő szoftverek, mint például a **Simplify3D** és a **Slic3r**, lefordítják a számítógéppel segített tervezési (CAD) rajzokat GCODE-ba; A CAD-szoftver 3D modellek létrehozására szolgál, amelyeket aztán olyan formátumban exportálnak, mint az STL; a szeletelő szoftver ezeket a modelleket veszi, és GCODE-fájlt generál, amely megadja az olyan részleteket, mint a rétegmagasság, a nyomtatási sebesség és a hőmérséklet-beállítások.

## GCODE példa

Íme egy egyszerű példa a G-kódra a mozgó CNC gépekhez:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## GCODE fájl - Mivel nyitható meg egy GCODE fájl?

A G-kód fájl megnyitásához különböző típusú szoftvereket használhat az igényeitől függően.

Ha G-kódot generált 3D nyomtatóhoz; megnyithatja a 3D nyomtatóhoz mellékelt szoftverrel vagy erre a célra szolgáló szeletelőszoftverrel; például a **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** vagy **Repetier-Host**; ezek a programok gyakran felhasználóbarát felülettel rendelkeznek, amely lehetővé teszi a G-kód betöltését és megjelenítését.

A GCODE fájlok egyszerű szövegesek, így bármilyen szövegszerkesztővel megnyithatja őket; a gyakori szövegszerkesztők közé tartozik a **Jegyzettömb (Windows rendszeren)**, **TextEdit (macOS rendszeren)** vagy **Gedit (Linux rendszeren)**; egyszerűen **kattintson jobb gombbal** a G-kód fájlra, válassza a **Megnyitás** lehetőséget, és válasszon egy szövegszerkesztőt.

