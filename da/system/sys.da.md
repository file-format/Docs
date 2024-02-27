{
  "date": "2021-07-08",
  "keywords": [
"SYS",
"udvidelse",
"fil",
"format",
"system",
"Chauffør",
"Systemfil",
"programmer",
"computer",
"Ansøgning"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "SYS - Systemfilformat",
  "description": "Lær om SYS filformat og API'er, der kan oprette og åbne SYS filer.",
  "linktitle": "SYS",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sy-das"
}
},
  "lastmod": "2021-07-08"
}

## Hvad er SYS fil? ##

SYS-filerne er Systemfiler, der bruges i Windows OS og MS-DOS-applikationer. Disse filer kan ikke åbnes direkte og består af enhedens driver og konfiguration. SYS-filerne er ansvarlige for at indeholde filer med kernefunktioner i operativsystemet. Disse betragtes som kritiske filer for enhedsføreren og kan også bruges, når ethvert problem med racerkøreren skal løses. Disse er ansvarlige for, at et computersystem fungerer korrekt, og .sys-filerne skal være korrekte og fuldstændige.


## Teknisk specifikation ##

.sys-filerne er faktisk undersættet af [BMP](/image/bmp/)-formatet, da det kun tillader specifikke kombinationer. Det sædvanlige format for disse filer er som LOGOS.SYS, LOGOW.SYS og LOGO.SYS. Andre filer har ikke dette format.

Disse filer bruges mest i mappen *C* i Windows på installationstidspunktet. De fleste problemer, der drejer sig om enhedsdrivere, løses ved at opdatere Windows OS. Detaljerne og oplysningerne om disse filer kan ses ved at bruge de indbyggede programmer i Windows OS. Disse omfatter også referencerne til forskellige moduler i et operativsystem.
Nogle af eksemplerne på systemfiler er:

* IO.SYS (Disse lagrer enhedsdrivere til diskoperativsystemet)

* MSDOS.SYS (Disse indeholder kerne eller kernekoden for operativsystemet)

* CONFIG.SYS (Disse indeholder forskellige konfigurationsmuligheder)

* KEYBOARD.SYS (Disse indeholder oplysninger om tastaturlayout) 

* COUNTRY.SYS (Disse indeholder lande- og kodetabel relaterede oplysninger)


## SYS-filformat ##

Microsoft udviklede filerne med .sys-udvidelser. Variabler og funktioner er inkluderet i SYS-filer. Disse bruges mest af Microsoft-operativsystemet. Disse filer er hovedsageligt placeret i rodmappen på disken:

* C:\Windows\system32\drivere

* C:\Windows\WinSxS


Nogle almindelige advarsler om SYS filer er som følger:

* Navnene på disse filer bør ikke ændres, da disse filer er ansvarlige for kernefunktioner og variabler i operativsystemet
* Disse filer bør ikke slettes, fordi deres fravær af disse filer kan forårsage fejl
* .sys-filerne bør ikke downloades fra internettet, før du er sikker på kildens legitimitet
* Man bør ikke rode med disse filer, da det at ændre dem eller rode med disse forårsager alvorlige systemfejl
* Hvis disse filer bliver ødelagt af virus eller malware, skal disse geninstalleres

## SYS eksempel ##

Det følgende er et eksempel på en simpel SYS-systemkonfigurationsfil:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
