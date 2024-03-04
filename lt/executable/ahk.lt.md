{
  "date": "2022-04-25",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie AHK failo formatą ir API, kurios gali kurti ir atidaryti AHK failus.",
  "title": "AHK failo formatas - AutoHotkey scenarijaus failas",
  "linktitle": "AHK",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ah-ltk"
}
},
  "lastmod": "2022-04-25"
}

## Kas yra AHK failas?

AHK failas yra scenarijaus failas, sukurtas naudojant AutoHotkey programinę įrangą, kuris naudojamas automatizuoti užduotis Microsoft Windows. Jame pateikiamos užduočių automatizavimo instrukcijos, naudojant sparčiuosius klavišus, kurie gali būti naudojami momentiniams veiksmams atlikti. Failas paleidžiamas AutoHotkey ir visi veiksmai atliekami nuosekliai. AHK failai yra pakankamai galingi, kad galėtų atlikti sudėtingas užduotis naudojant sparčiuosius klavišus, apibrėžtus naudojant sparčiuosius klavišus. AHK failus galima atidaryti naudojant teksto redaktorius, tokius kaip Microsoft Notepad ir Notepad++.

## AHK failo formatas

AHK failai išsaugomi diske kaip paprasto teksto failai ir juose yra kodo eilučių, kurias gali vykdyti AutoHotkey. AutoHotkey yra nemokama atvirojo kodo scenarijų kalba, leidžianti vartotojams kurti paprastus ir sudėtingus scenarijus, kad būtų galima atlikti tokius veiksmus, kaip formų užpildymas, automatinis spustelėjimas, makrokomandų vykdymas ir kt. AHK failas gali atlikti bent vieną veiksmą ir tada išeiti. .

Yra įrankių, kuriuos galima naudoti konvertuojant AHK į [Exe](/executable/exe/) failus.

### AHK pavyzdys

Šiame pavyzdyje naudojamas Win+Z klavišas, kad paleistumėte Microsoft Notepad arba iškeltumėte jį į priekį, jei jis jau veikia.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Kaip sukurti AHK failą?

Norėdami sukurti AHK failą, galite atlikti šiuos veiksmus. Jie daro prielaidą, kad AutoHotkey jau įdiegtas įrenginyje.

* Dešiniuoju pelės mygtuku spustelėkite darbalaukį.

* Meniu raskite „Naujas“.

* Meniu „Naujas“ spustelėkite „AutoHotkey Script“.

* Suteikite scenarijui naują pavadinimą.

* Raskite naujai sukurtą failą darbalaukyje ir spustelėkite jį dešiniuoju pelės mygtuku.

* Spustelėkite „Redaguoti scenarijų“.

* Turėjo pasirodyti langas, tikriausiai užrašų knygelė.

* Išsaugokite failą.


## Nuorodos

* [AutoHotkey](https://www.autohotkey.com/)

* [Paketinis failas – pateikė Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)


