{
  "date": "2019-12-10",
  "keywords": [
"CSV",
"failu",
"pagarinājumu",
"faila formātā",
"Ar komatu atdalītas vērtības",
"Izklājlapa"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par CSV faila formātu un API, kas var izveidot un atvērt CSV failus.",
  "title": "CSV faila formāts",
  "linktitle": "CSV",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-cs-lvv"
}
},
  "lastmod": "2019-12-10"
}

## Kas ir CSV fails?

Faili ar paplašinājumu .csv (komatatdalītās vērtības) ir vienkārša teksta faili, kas satur datu ierakstus ar komatatdalītām vērtībām. Katra CSV faila rinda ir jauns ieraksts no failā ietvertās ierakstu kopas. Šādi faili tiek ģenerēti, ja ir paredzēta datu pārsūtīšana no vienas uzglabāšanas sistēmas uz citu. Tā kā visas programmas spēj atpazīt ierakstus, kas atdalīti ar komatu, šādu datu failu importēšana datu bāzē tiek veikta ļoti ērti. Gandrīz visas izklājlapu lietojumprogrammas, piemēram, Microsoft Excel vai OpenOffice Calc, var importēt CSV bez īpašas piepūles. No šādiem failiem importētie dati tiek sakārtoti izklājlapas šūnās, lai tos attēlotu lietotājam.

## Īsa vēsture ##

Tālāk ir sniegti daži ātri fakti par CSV faila formāta izcelsmi un vēsturi.

* 1972. gads — IBM Fortran (paplašināts H līmeņa) kompilators tos atbalstīja operētājsistēmā OS/360


* 1978. gads — uz sarakstu vērstu ievadi/izvadi atbalstīja FORTRAN 77, kas atdalītājiem izmantoja komatus un atstarpes


* 2005. gads — CSV tika standartizēts ar [RFC4180](https://tools.ietf.org/html/rfc4180) kā MIME satura veidu.


* 2013. gads — RFC4180 trūkumi tika novērsti, izmantojot W3C ieteikumu


* 2015. gads — W3C izstrādāja pirmos ieteikumu projektus CSV metadatu standartiem, kas sākās kā ieteikums 2015. gada decembrī.


## Konvertēt CSV failus ##

CSV failus var pārvērst vairākos dažādos failu formātos, izmantojot lietojumprogrammas, kas var atvērt šos failus. Piemēram, Microsoft Excel var importēt datus no CSV faila formāta un saglabāt tos XLS, [XLSX](/spreadsheet/xlsx/), [PDF](/pdf/), [TXT](/word-processing/txt/), XML un [HTML](/web/html/) failu formātos. Līdzīgi citi darbvirsmas, kā arī tiešsaistes pakalpojumi nodrošina iespēju eksportēt CSV failus uz HTML, ODS un [RTF](/word-processing/rtf/).

## CSV faila formāts ##

Ir zināms, ka CSV faila formāts ir norādīts sadaļā [RFC4180](https://tools.ietf.org/html/rfc4180). Tas nosaka, ka jebkurš fails ir saderīgs ar CSV, ja:

* Katrs ieraksts atrodas atsevišķā rindā, ko norobežo līnijas pārtraukums (CRLF). Piemēram:

  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx CRLF
* Pēdējam ierakstam failā var būt un var nebūt beigu rindiņas pārtraukuma. Piemēram:

  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx
* Var būt papildu galvenes rinda, kas parādās kā faila pirmā rindiņa ar tādu pašu formātu kā parastajām ierakstu rindām. Šajā galvenē būs nosaukumi, kas atbilst faila laukiem, un tajā ir jābūt tādam pašam lauku skaitam kā ierakstiem pārējā failā (galvenes rindas esamība vai neesamība jānorāda, izmantojot šī faila izvēles parametru "header" MIME veids). Piemēram:

  * lauka_nosaukums, lauka_nosaukums, lauka_nosaukums CRLF
  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx CRLF
* ﻿Galvenē un katrā ierakstā var būt viens vai vairāki lauki, kas atdalīti ar komatiem. Katrā rindiņā ir jābūt vienādam lauku skaitam visā failā. Atstarpes tiek uzskatītas par lauka daļu, un tās nedrīkst ignorēt. Aiz pēdējā ieraksta lauka nedrīkst būt komats. Piemēram:

  * aaa,bbb,ccc
* Katrs lauks var būt vai nevar būt ievietots dubultpēdiņās (tomēr dažas programmas, piemēram, Microsoft Excel, vispār neizmanto dubultpēdas). Ja lauki nav ietverti dubultpēdiņās, dubultpēdiņas var neparādīties laukos. Piemēram:\

  * aaa,bbb,ccc CRLF
  * zzz,yyy,xxx
* Lauki, kas satur rindiņu pārtraukumus (CRLF), dubultpēdas un komatus, jāiekļauj dubultpēdiņās. Piemēram:

  * aaa,b CRLF
  * bb,ccc CRLF
  * zzz,yyy,xxx
* Ja lauku ievietošanai tiek izmantotas dubultpēdas, tad laukā redzamās dubultās pēdiņas ir jāaizpilda, pirms tās ievietojot citu dubultpēdiņu. Piemēram:

  * aaa,bbb,ccc

Tomēr, ņemot vērā mūsdienu lietojumu, norobežotājs neaprobežojas tikai ar komatu, un tas var būt arī semikols, tabulēšana vai atstarpes. Programmas, piemēram, Microsoft Excel, nodrošina iespēju norādīt norobežotāja rakstzīmi ierakstu importēšanai no CSV faila.

## Atsauces

* [RFC 4180](https://tools.ietf.org/html/rfc4180)

* [RFC 2048](https://tools.ietf.org/html/rfc2048)

* [CSV — Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)


