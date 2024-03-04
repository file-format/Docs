{
  "date": "2019-10-11",
  "keywords": [
"sh failą",
".sh failą",
"pratęsimas",
"formatu",
"sh failo pavyzdys",
"sh failo formatas",
"kaip paleisti sh failą"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SH – „Bash Shell“ scenarijaus failas",
  "description": "Sužinokite apie SH failo formatą ir API, kurios gali kurti ir atidaryti SH failus.",
  "linktitle": "SH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-s-lth"
}
},
  "lastmod": "2021-05-21"
}

## Kas yra SH failas?

Failas su plėtiniu .sh yra skriptų kalbos komandų failas, kuriame yra kompiuterio programa, kurią turi paleisti Unix apvalkalas. Jame gali būti keletas komandų, kurios paleidžiamos nuosekliai, kad būtų galima atlikti tokias operacijas kaip failų apdorojimas, programų vykdymas ir kitos panašios užduotys. Juos vartotojas vykdo iš komandinės eilutės sąsajos arba atlieka paketą, kad vienu metu būtų galima atlikti kelias operacijas. Scenarijaus failus galima atidaryti tokiuose teksto rengyklėse kaip Notepad, Notepad++, Vim, Apple Terminal ir kitose panašiose Windows, MacOS ir Linux OS programose.

## SH failo formatas

SH failai parašyti paprastu tekstu pagal apibrėžtą sintaksę. Šie scenarijaus failai palaiko:

 * Komentarai – komentarai prasideda simboliu #, o apvalkalas į juos nepaiso.
 * Spartieji klavišai – juos galima naudoti norint pervardyti komandą, kad būtų galima trumpai ir lengvai vykdyti.
 * Paketiniai darbai – gali būti automatiškai vykdomos kelios komandos, kurias kitu atveju reikėtų įvesti rankiniu būdu. Tai pašalina poreikį laukti, kol vartotojas suaktyvins kiekvieną sekos etapą.
 * Apibendrinimas – naudojant paprastas kilpas, daug daugiau apibendrinimo pasiekiama atliekant tokias operacijas kaip vaizdų konvertavimas iš vienos vietos į kitą.

## SH failo pavyzdys

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Kaip paleisti SH failą?
SH failai paprastai veikia Linux, net Windows turite prisijungti prie Linux terminalo naudojant programinę įrangą, pvz., Putty, kad paleistumėte sh failus. Toliau pateikiami žingsniai, kaip paleisti SH failą Linux terminale.

1. Atidarykite Linux terminalą ir eikite į katalogą, kuriame yra SH failas.
2. Naudodami komandą chmod, nustatykite scenarijaus vykdymo leidimą (jei dar nenustatyta).
3. Vykdykite scenarijų naudodami vieną iš šių veiksmų
	1. ./filename.sh.
	2.  sh failo pavadinimas.sh.
	3.  bash script-name-here.sh.

## Nuorodos

* [Bashscripting for Beginners](https://help.ubuntu.com/community/Beginners/BashScripting)

* [Shellscript](https://www.shellscript.sh/)


