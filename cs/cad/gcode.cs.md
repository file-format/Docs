{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"Soubor GCODE – Co je soubor .gcode a jak jej otevřít?",
   "description":"Přečtěte si o formátu souboru GCODE a rozhraních API, která mohou vytvářet a otevírat soubory GCODE.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-cs",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Co je soubor GCODE?

**Soubor GCODE** je prostý textový soubor, který obsahuje pokyny pro ovládání počítačových obráběcích strojů a 3D tiskáren; G-code neboli Geometric Code je jazyk používaný k ovládání pohybů a akcí **CNC (Computer Numerical Control)** strojů; Mezi CNC stroje patří frézky, soustruhy, routery a 3D tiskárny.

Příkazy G-kódu jsou psány ve specifické syntaxi, která se obvykle skládá z písmen a čísel; každý příkaz dává stroji pokyn k provedení specifické akce, jako je přesun nástroje do konkrétní polohy, výměna nástroje nebo nastavení rychlosti.

G-kód je často generován softwarem **CAM (Computer-Aided Manufacturing)**; CAM software přebírá 3D model nebo 2D návrh a generuje odpovídající dráhy nástroje a instrukce G-kódu; soubor G-kódu je poté načten do CNC stroje nebo 3D tiskárny pro provedení.

Soubory G-code mají obvykle příponu .nc nebo .gcode, například program.nc nebo print.gcode.

## Struktura souboru GCODE:

Soubory GCODE jsou soubory ve formátu prostého textu, přičemž každý řádek obsahuje specifický příkaz; tyto příkazy sahají od řízení pohybu stroje až po nastavení teploty, rychlosti a dalších parametrů rozhodujících pro výrobu objektu.

Syntaxe GCODE zahrnuje kombinaci písmen a čísel; každý představuje odlišnou akci nebo parametr; běžné příkazy zahrnují G0 a G1 pro pohyb, M3 a M5 pro ovládání vřetena a S a F pro nastavení rychlosti a rychlosti posuvu.

## Generování GCODE:

Software pro řezání, jako je **Simplify3D** a **Slic3r**, převádí výkresy CAD (Computer-Aided Design) do GCODE; CAD software se používá k vytváření 3D modelů, které jsou následně exportovány ve formátech jako STL; řezací software vezme tyto modely a vygeneruje soubor GCODE specifikující podrobnosti, jako je výška vrstvy, rychlost tisku a nastavení teploty.

## Příklad GCODE

Zde je jednoduchý příklad G-kódu pro pohyblivý CNC stroj:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Jak otevřít soubor GCODE?

K otevření souboru G-code můžete použít různé typy softwaru v závislosti na vašich potřebách.

Pokud jste vygenerovali G-kód pro 3D tiskárnu; můžete jej otevřít pomocí softwaru dodaného s vaší 3D tiskárnou nebo speciálního softwaru pro krájení; příklady zahrnují **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** nebo **Repetier-Host**; tyto programy mají často uživatelsky přívětivé rozhraní, které vám umožňuje načíst a zobrazit G-kód.

Soubory GCODE jsou prostý text, takže je můžete otevřít v libovolném textovém editoru; mezi běžné textové editory patří **Poznámkový blok (v systému Windows)**, **TextEdit (v systému macOS)** nebo **Gedit (v systému Linux)**; jednoduše **klikněte pravým tlačítkem** na soubor G-code, zvolte **Otevřít pomocí,** a vyberte textový editor.

