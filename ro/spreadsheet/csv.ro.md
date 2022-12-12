{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "fișier", "extensie", "format fișier", "Valori separate prin virgulă", "Foaie de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier CSV și despre API-urile care pot crea și deschide fișiere CSV.",
  "title" :"Format fișier CSV",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Ce este un fișier CSV?

Fișierele cu extensia .csv (Valori separate prin virgulă) reprezintă fișiere text simplu care conțin înregistrări de date cu valori separate prin virgulă. Fiecare linie dintr-un fișier CSV este o înregistrare nouă din setul de înregistrări conținut în fișier. Astfel de fișiere sunt generate atunci când se intenționează transferul de date de la un sistem de stocare la altul. Deoarece toate aplicațiile pot recunoaște înregistrările separate prin virgulă, importul unor astfel de fișiere de date în baza de date se face foarte convenabil. Aproape toate aplicațiile pentru foi de calcul precum Microsoft Excel sau OpenOffice Calc pot importa CSV fără prea mult efort. Datele importate din astfel de fișiere sunt aranjate în celulele unei foi de calcul pentru a fi reprezentate pentru utilizator.

## Scurt istoric ##

Următoarele sunt câteva fapte rapide despre originea și istoria formatului de fișier CSV.

* 1972 - Compilatorul IBM Fortran (nivel H extins) le-a suportat sub OS/360

* 1978 - Intrarea/ieșirea direcționată pe listă a fost acceptată de FORTRAN 77 care folosea virgule și spații pentru delimitatori

* 2005 - CSV a fost standardizat cu [RFC4180](https://tools.ietf.org/html/rfc4180) ca tip de conținut MIME.

* 2013 - deficiențele RFC4180 au fost tratate printr-o recomandare W3C

* 2015 - W3C a făcut primele schițe de recomandări pentru standardele CSV-metadate, care au început ca recomandare în decembrie 2015

## Convertiți fișiere CSV ##

Fișierele CSV pot fi convertite în mai multe formate de fișiere diferite folosind aplicațiile care pot deschide aceste fișiere. De exemplu, Microsoft Excel poate importa date din formatul de fișier CSV și le poate salva în XLS, [XLSX](/ro/spreadsheet/xlsx/), [PDF](/ro/pdf/), [TXT](/ro/word-processing/txt/) , XML și [HTML](/ro/web/html/) formate de fișiere. În mod similar, alte servicii desktop, precum și online oferă capacitatea de a exporta fișiere CSV în HTML, ODS și [RTF](/ro/word-processing/rtf/).

## Format fișier CSV ##

Se știe că formatul de fișier CSV este specificat în [RFC4180](https://tools.ietf.org/html/rfc4180). Acesta definește ca orice fișier să fie compatibil CSV dacă:

* Fiecare înregistrare este situată pe o linie separată, delimitată de o întrerupere de linie (CRLF). De exemplu:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* Ultima înregistrare din fișier poate avea sau nu o întrerupere de linie finală. De exemplu:
* aaa,bbb,ccc CRLF
*zzz,aaaa,xxx
* Este posibil să apară o linie de antet opțională ca prima linie a fișierului cu același format ca liniile de înregistrare normale. Acest antet va conține nume corespunzătoare câmpurilor din fișier și ar trebui să conțină același număr de câmpuri ca și înregistrările din restul fișierului (prezența sau absența liniei de antet ar trebui să fie indicată prin intermediul parametrului opțional „header” al acestui tip MIME). De exemplu:
* field_name,field_name,field_name CRLF
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* ﻿În antet și în fiecare înregistrare, pot exista unul sau mai multe câmpuri, separate prin virgulă. Fiecare linie trebuie să conțină același număr de câmpuri în întregul fișier. Spațiile sunt considerate parte a unui câmp și nu trebuie ignorate. Ultimul câmp din înregistrare nu trebuie să fie urmat de virgulă. De exemplu:
* aaa,bbb,ccc
* Fiecare câmp poate fi sau nu cuprins între ghilimele duble (cu toate acestea, unele programe, cum ar fi Microsoft Excel, nu folosesc deloc ghilimele duble). Dacă câmpurile nu sunt închise cu ghilimele duble, atunci ghilimelele duble pot să nu apară în interiorul câmpurilor. De exemplu:\
* "aaa","bbb","ccc" CRLF
*zzz,aaaa,xxx
* Câmpurile care conțin întreruperi de linie (CRLF), ghilimele duble și virgule ar trebui să fie cuprinse între ghilimele duble. De exemplu:
* "aaa","b CRLF
* bb","ccc" CRLF
*zzz,aaaa,xxx
* Dacă sunt folosite ghilimele duble pentru a include câmpuri, atunci ghilimelele duble care apar în interiorul unui câmp trebuie să fie eliminate precedându-l cu alte ghilimele duble. De exemplu:
* "aaa","b""bb","ccc"

Cu toate acestea, în lumina utilizării moderne, delimitatorul nu se limitează doar la virgulă și poate fi și punct și virgulă, tab sau spații. Aplicații precum Microsoft Excel oferă opțiunea de a specifica caracterul delimitator pentru importarea înregistrărilor dintr-un fișier CSV.

## Referințe

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

