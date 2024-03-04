{
  "date": "2023-03-07",
  "keywords": [
"reg failą",
"kas yra reg failas",
"failą",
"reg failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "REG failo formatas – „Windows“ registro failas",
  "description": "Sužinokite apie REG formatą ir API, kurios gali kurti ir atidaryti REG failus.",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg-lt",
      "parent": "system"
}
},
  "lastmod": "2023-03-07"
}

## Kas yra REG failas?

REG failas yra failo formatas, naudojamas Windows registro duomenims importuoti arba eksportuoti. Windows registras yra hierarchinė duomenų bazė, kurioje saugomi Windows operacinės sistemos ir įdiegtų programų konfigūracijos nustatymai ir parinktys. Registre yra tokia informacija kaip vartotojo nuostatos, programos nustatymai, aparatinės ir programinės įrangos konfigūracijos duomenys ir kt.

REG failas paprastai turi .reg failo plėtinį ir yra paprasto teksto failas, kuriame yra tam tikro formato registro įrašų ir reikšmių serija. Formatą sudaro antraštės skyrius, identifikuojantis failą kaip registro failą, o po to seka raktų ir reikšmių poros, atspindinčios registro įrašus.

## REG failo formatas – daugiau informacijos

Čia yra reg failo formato pavyzdys:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Pirmoje failo eilutėje nurodoma registro rengyklės versija. Šiose eilutėse yra registro įrašai rakto kelio formatu, po kurio nurodomas reikšmės pavadinimas ir reikšmės duomenys. Šiame pavyzdyje reg faile yra du įrašai: vienas prideda programą pavadinimu Example.exe į Windows paleisties sąrašą, o kitas Windows Explorer išplėstiniuose nustatymuose nustato Hidden reikšmę į true.

Reg failus galima kurti ir redaguoti naudojant teksto rengyklę, pvz., Notepad. Jie dažnai naudojami atsarginėms kopijoms kurti ir atkurti, taip pat konfigūruoti kelis kompiuterius su tais pačiais registro parametrais.

## Importuokite arba eksportuokite „Windows“ registrą

REG failas yra failo tipas, naudojamas duomenims importuoti arba eksportuoti iš Windows registro. Windows registras yra hierarchinė duomenų bazė, kurioje saugomi Windows operacinės sistemos ir įdiegtų programų konfigūracijos nustatymai ir parinktys. Registre yra tokia informacija kaip vartotojo nuostatos, programos nustatymai, aparatinės ir programinės įrangos konfigūracijos duomenys ir kt.

Reg failai gali būti naudojami registro įrašams kurti arba modifikuoti, jie dažnai naudojami atsarginėms kopijoms kurti ir atkurti, taip pat keliems kompiuteriams su tais pačiais registro parametrais konfigūruoti. Štai kaip naudoti reg failą naujam registro įrašui pridėti prie Windows registro:

1. Sukurkite naują tekstinį failą naudodami teksto rengyklę, pvz., Notepad.
2. Įveskite registro įrašą tinkamu formatu. Formatą sudaro antraštės skyrius, identifikuojantis failą kaip registro failą, o po to seka raktų ir reikšmių poros, atspindinčios registro įrašus. Štai pavyzdys:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Tai sukuria naują raktą pavadinimu Pavyzdys pagal raktą Programinė įranga dabartinio vartotojo registro avilyje ir nustato Setting1 reikšmę į Value1.

3. Išsaugokite failą su .reg failo plėtiniu.
4. Dukart spustelėkite .reg failą, kad įtrauktumėte naują registro įrašą į Windows registrą.

Būsite paraginti patvirtinti, kad norite įtraukti įrašą į registrą. Kai patvirtinsite, naujas įrašas bus įtrauktas į registrą ir galėsite jį patikrinti naudodami registro rengyklės įrankį.

## Nuorodos
* [Windows registras](https://en.wikipedia.org/wiki/Windows_Registry)


