{
  "date": "2021-07-12",
  "keywords": [
"cmd failu",
"kas ir cmd fails",
"failu",
"cmd piemērs",
"cmd faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par CMD failu formātu un API, kas var izveidot un atvērt CMD failus.",
  "title": "CMD - Windows komandu faila formāts",
  "linktitle": "CMD",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cm-lvd"
}
},
  "lastmod": "2021-07-12"
}

## Kas ir CMD fails?
CMD fails sastāv no skripta, kas satur vienu vai vairākas komandas vienkārša teksta veidā, kuras tiek palaists dažādu uzdevumu izpildei. Tas ir līdzīgs failam [BAT](/executable/bat/), ko parasti izmanto arī izpildāmo komandu partijas glabāšanai. CMD faili tiek plaši izmantoti Microsoft Windows operētājsistēmā. Šie faili tika ieviesti gandrīz 90. gados, bet joprojām tika izmantoti jaunākajā Windows operētājsistēmā. Šie faili parasti ir rakstīti, lai pēc kārtas izpildītu vairāk nekā vienu komandu.

## CMD faila formāts
CMD ir faila formāts, ko izmanto CP/M stila izpildāmās programmas. Parasti tas ir salīdzināms ar [COM](/executable/com/) CP/M-80 un [EXE](/executable/exe/) DOS. CMD fails satur 1–8 koda vai datu grupas un 128 baitu galveni. Katras grupas izmērs var būt līdz 1 MB. CMD faili var saturēt arī pārvietošanas informāciju un pastāvīgo sistēmu paplašinājumus (RSX) to jaunākajās versijās. CMD ir jaunpienācējs, salīdzinot ar failu [BAT](/executable/bat/); izmantots MS-DOS pirms Windows izlaišanas MS-DOS. Lai gan šodien joprojām varat saglabāt failus ar paplašinājumu .bat, daudzi lietotāji izpildāmo skriptu saglabāšanai izmanto paplašinājumu .cmd.

### CMD formāta specifikācija

Galvenes sākumā ir failā esošo grupu saraksts un to veidi. Katru veidu var izmantot ne vairāk kā vienu reizi. Šie veidi ir:

- Kods
- Dati
- Papildus
- Kaudze
- 1. lietotājs
- 2. lietotājs
- 3. lietotājs
- 4. lietotājs
- Koplietotais kods

Tāpat programmas segmenta prefikss DOS, pirmie 256 datu grupas baiti ir nulle. Tie tiks aizpildīti ar CP/M-86 ar nulles lapu. Ja datu grupas nav, tā vietā tiks izmantoti pirmie 256 koda grupas baiti.
## CMD faila piemērs
Tālāk ir sniegts CMD skripta piemērs sistēmas informācijas parādīšanai.
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



## Atsauces 

* [Kā uzrakstīt CMD skriptu](https://smallbusiness.chron.com/write-cmd-script-53226.html)

* [CMD fails (CP/M) — Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))


