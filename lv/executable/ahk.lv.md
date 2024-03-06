{
  "date": "2022-04-25",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par AHK failu formātu un API, kas var izveidot un atvērt AHK failus.",
  "title": "AHK faila formāts - AutoHotkey skripta fails",
  "linktitle": "AHK",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ah-lvk"
}
},
  "lastmod": "2022-04-25"
}

## Kas ir AHK fails?

AHK fails ir skripta fails, kas ģenerēts ar AutoHotkey programmatūras lietojumprogrammu, ko izmanto uzdevumu automatizēšanai sistēmā Microsoft Windows. Tajā ir norādījumi par uzdevumu automatizāciju, izmantojot īsinājumtaustiņus, kurus var izmantot tūlītēju darbību veikšanai. Failu izpilda AutoHotkey, un visas darbības tiek veiktas secīgi. AHK faili ir pietiekami jaudīgi, lai veiktu sarežģītus uzdevumus, izmantojot karstos taustiņus, kas definēti, izmantojot karstos taustiņus. AHK failus var atvērt ar teksta redaktoriem, piemēram, Microsoft Notepad un Notepad++.

## AHK faila formāts

AHK faili tiek saglabāti diskā kā vienkārša teksta faili, un tajos ir koda rindas, kuras var izpildīt, izmantojot funkciju AutoHotkey. AutoHotkey ir bezmaksas atvērtā koda skriptu valoda, kas ļauj lietotājiem izveidot vienkāršus vai sarežģītus skriptus, lai veiktu tādas darbības kā veidlapu aizpildīšana, automātiskā noklikšķināšana, makro izpilde utt. AHK fails var veikt vismaz vienu darbību un pēc tam iziet. .

Ir pieejami rīki, kurus var izmantot, lai pārveidotu AHK par [Exe](/executable/exe/) failiem.

### AHK piemērs

Nākamajā piemērā tiek izmantots taustiņš Win+Z, lai palaistu Microsoft Notepad vai parādītu to priekšā, ja tas jau darbojas.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Kā izveidot AHK failu?

Lai izveidotu AHK failu, var izmantot šādas darbības. Tie pieņem, ka AutoHotkey jau ir instalēts mašīnā.

* Ar peles labo pogu noklikšķiniet uz darbvirsmas.

* Izvēlnē atrodiet "Jauns".

* Izvēlnē "Jauns" noklikšķiniet uz "AutoHotkey Script".

* Piešķiriet skriptam jaunu nosaukumu.

* Darbvirsmā atrodiet jaunizveidoto failu un ar peles labo pogu noklikšķiniet uz tā.

* Noklikšķiniet uz "Rediģēt skriptu".

* Vajadzēja parādīties logam, iespējams, Notepad.

* Saglabājiet failu.


## Atsauces

* [AutoHotkey](https://www.autohotkey.com/)

* [Pakešfails — Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)


