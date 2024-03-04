{
  "date": "2021-07-12",
  "keywords": [
"cmd failą",
"kas yra cmd failas",
"failą",
"cmd pavyzdys",
"cmd failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie CMD failo formatą ir API, kurios gali kurti ir atidaryti CMD failus.",
  "title": "CMD – „Windows“ komandų failo formatas",
  "linktitle": "CMD",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cm-ltd"
}
},
  "lastmod": "2021-07-12"
}

## Kas yra CMD failas?
CMD failą sudaro scenarijus, kuriame yra viena ar kelios paprasto teksto komandos, kurios vykdomos įvairioms užduotims atlikti. Jis panašus į [BAT](/executable/bat/) failą, kuris taip pat paprastai naudojamas vykdomų komandų paketui saugoti. CMD failai plačiai naudojami Microsoft Windows operacinėje sistemoje. Šie failai buvo pristatyti beveik 90-aisiais, bet vis dar naudojami naujausioje Windows operacinėje sistemoje. Šie failai paprastai yra parašyti taip, kad iš eilės būtų vykdoma daugiau nei viena komanda.

## CMD failo formatas
CMD yra failo formatas, naudojamas CP/M stiliaus vykdomosiose programose. Paprastai jį galima palyginti su [COM](/executable/com/) CP/M-80 ir [EXE](/executable/exe/) DOS. CMD faile yra nuo 1 iki 8 kodų arba duomenų grupių ir 128 baitų antraštės. Kiekviena grupė gali būti iki 1 MB dydžio. CMD failuose taip pat gali būti informacijos apie perkėlimą ir nuolatinių sistemos plėtinių (RSX) vėlesnėse versijose. CMD yra naujokas, palyginti su [BAT](/executable/bat/) failu; naudojamas MS-DOS prieš išleidžiant Windows MS-DOS. Nors ir šiandien vis dar galite išsaugoti failus su plėtiniu .bat, daugelis žmonių naudoja plėtinį .cmd, kad išsaugotų vykdomuosius scenarijus.

### CMD formato specifikacija

Antraštės pradžioje yra faile esančių grupių sąrašas ir jų tipai. Kiekvienas tipas gali būti naudojamas daugiausia vieną kartą. Šie tipai yra:

- Kodas
- Duomenys
- Papildomai
- Sukrauti
– 1 vartotojas
- 2 vartotojas
– 3 vartotojas
– 4 vartotojas
- Bendras kodas

Taip pat programos segmento priešdėlis DOS, pirmieji 256 duomenų grupės baitai yra lygūs nuliui. Jie bus užpildyti CP/M-86 su nuliniu puslapiu. Jei duomenų grupės nėra, vietoj jos bus naudojami pirmieji 256 kodų grupės baitai.
## CMD failo pavyzdys
Toliau pateikiamas CMD scenarijaus, skirto sistemos informacijai rodyti, pavyzdys.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Nuorodos 

* [Kaip parašyti CMD scenarijų](https://smallbusiness.chron.com/write-cmd-script-53226.html)

* [CMD failas (CP/M) – Vikipedijos](https://en.wikipedia.org/wiki/CMD_file_(CP/M))


