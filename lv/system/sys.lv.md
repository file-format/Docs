{
  "date": "2021-07-08",
  "keywords": [
"SYS",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"Šoferis",
"Sistēmas fails",
"programmas",
"dators",
"pieteikumu"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "SYS — sistēmas faila formāts",
  "description": "Uzziniet par SYS faila formātu un API, kas var izveidot un atvērt SYS failus.",
  "linktitle": "SYS",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-sy-lvs"
}
},
  "lastmod": "2021-07-08"
}

## Kas ir SYS fails? ##

SYS faili ir sistēmas faili, ko izmanto Windows OS un MS-DOS lietojumprogrammās. Šos failus nevar atvērt tieši, un tie sastāv no ierīces draivera un konfigurācijas. SYS faili ir atbildīgi par operētājsistēmas pamatfunkciju failu saturēšanu. Tie tiek uzskatīti par kritiskiem ierīces draivera failiem, un tos var izmantot arī tad, ja ir jāatrisina kāda sacīkšu braucēja problēma. Tie ir atbildīgi par pareizu datorsistēmas darbību, un .sys failiem ir jābūt pareiziem un pilnīgiem.


## Tehniskā specifikācija Nr.

.sys faili faktiski ir [BMP](/image/bmp/) formāta apakškopa, jo tas pieļauj tikai noteiktas kombinācijas. Šo failu parastais formāts ir LOGOS.SYS, LOGOW.SYS un LOGO.SYS. Citos failos nav šī formāta.

Šie faili instalēšanas laikā galvenokārt tiek izmantoti Windows *C* direktorijā. Lielākā daļa problēmu, kas saistītas ar ierīču draiveriem, tiek atrisinātas, atjauninot Windows OS. Detalizētu informāciju un informāciju par šiem failiem var skatīt, izmantojot Windows OS iebūvētās programmas. Tie ietver arī atsauces uz dažādiem operētājsistēmas moduļiem.
Daži sistēmas failu piemēri ir:

* IO.SYS (tie saglabā diska operētājsistēmas ierīču draiverus)

* MSDOS.SYS (tie satur kodolu vai operētājsistēmas pamata kodu)

* CONFIG.SYS (tajos ir dažādas konfigurācijas opcijas)

* KEYBOARD.SYS (tajos ir ietverta informācija par tastatūras izkārtojumu) 

* COUNTRY.SYS (Šī informācija ir saistīta ar valsti un kodulapu)


## SYS faila formāts ##

Microsoft izstrādāja failus ar .sys paplašinājumiem. Mainīgie lielumi un funkcijas ir iekļautas SYS failos. Tos galvenokārt izmanto Microsoft operētājsistēma. Šie faili galvenokārt atrodas diska saknes direktorijā:

* C:\Windows\system32\drivers

* C:\Windows\WinSxS


Daži izplatīti brīdinājumi par SYS failiem ir šādi:

* Šo failu nosaukumus nevajadzētu mainīt, jo šie faili ir atbildīgi par operētājsistēmas pamatfunkcijām un mainīgajiem.
* Šos failus nevajadzētu dzēst, jo to trūkums var izraisīt kļūdas
* .sys failus nevajadzētu lejupielādēt no interneta, kamēr neesat pārliecināts par avota likumību
* Nevajadzētu sajaukt ar šiem failiem, jo to mainīšana vai jaukšanās ar tiem izraisa nopietnas sistēmas kļūdas
* Ja šos failus sabojā kāds vīruss vai ļaunprātīga programmatūra, tie ir jāinstalē atkārtoti

## SYS piemērs ##

Šis ir vienkārša SYS sistēmas konfigurācijas faila piemērs:

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
