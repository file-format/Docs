{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"Fișier GCODE - Ce este un fișier .gcode și cum se deschide?",
   "description":"Aflați despre formatul de fișier GCODE și despre API-urile care pot crea și deschide fișiere GCODE.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-ro",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Ce este un fișier GCODE?

Un **fișier GCODE** este un fișier text simplu care conține instrucțiuni pentru controlul mașinilor-unelte computerizate și a imprimantelor 3D; Codul G sau Codul geometric” este un limbaj folosit pentru a controla mișcările și acțiunile mașinilor **CNC (Control numeric pe computer)**; Mașinile CNC includ mașini de frezat, strunguri, routere și imprimante 3D.

Comenzile G-code sunt scrise într-o sintaxă specifică constând de obicei din litere și cifre; fiecare comandă instruiește mașina să efectueze o acțiune specifică, cum ar fi mutarea sculei într-o anumită poziție, schimbarea sculei sau reglarea vitezei.

Codul G este adesea generat de software-ul **CAM (Computer-Aided Manufacturing)**; Software-ul CAM preia modelul 3D sau designul 2D și generează traseele de instrumente corespunzătoare și instrucțiunile G-code; fișierul G-code este apoi încărcat în mașina CNC sau în imprimanta 3D pentru execuție.

Fișierele G-code au de obicei extensia de fișier .nc” sau .gcode”, de exemplu, program.nc” sau print.gcode”.

## Structura fișierului GCODE:

Fișierele GCODE sunt fișiere text simplu, fiecare linie conține o comandă specifică; aceste comenzi variază de la controlul mișcării mașinii până la reglarea temperaturii, vitezei și a altor parametri cruciali pentru fabricarea unui obiect.

Sintaxa GCODE implică o combinație de litere și numere; fiecare reprezentând o acțiune sau un parametru distinct; comenzile comune includ G0 și G1 pentru mișcare, M3 și M5 pentru controlul axului și S și F pentru reglarea vitezei și, respectiv, a vitezei de avans.

## Generarea GCODE:

Software-ul de tăiere, cum ar fi **Simplify3D** și **Slic3r**, traduce desenele de proiectare asistată de computer (CAD) în GCODE; Software-ul CAD este folosit pentru a crea modele 3D, care sunt apoi exportate în formate precum STL; software-ul de tăiere preia aceste modele și generează fișierul GCODE care specifică detalii precum înălțimea stratului, viteza de imprimare și setările de temperatură.

## Exemplu GCODE

Iată un exemplu simplu de cod G pentru mutarea mașinii CNC:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Cum se deschide un fișier GCODE?

Pentru a deschide un fișier G-code puteți utiliza diferite tipuri de software, în funcție de nevoile dvs.

Dacă ați generat cod G pentru imprimanta 3D; îl puteți deschide folosind software-ul livrat cu imprimanta dvs. 3D sau software-ul dedicat de tăiere; exemplele includ **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** sau **Repetier-Host**; aceste programe au adesea o interfață ușor de utilizat, care vă permite să încărcați și să vizualizați codul G.

Fișierele GCODE sunt text simplu, așa că le puteți deschide cu orice editor de text; editorii de text obișnuiți includ **Notepad (pe Windows)**, **TextEdit (pe macOS)** sau **Gedit (pe Linux)**; pur și simplu **clic-dreapta** pe fișierul G-code, alege **Deschide cu** și selectează un editor de text.

