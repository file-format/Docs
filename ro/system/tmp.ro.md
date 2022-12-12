{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "extensie", "fișier", "format", "sistem", "fișier TMP", "documente TMP", "fișiere TMP", "fișier temporar", "aplicație", "programe"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP – Format de fișier temporar",
  "description":"Aflați despre formatul de fișier TMP și despre API-urile care pot crea și deschide fișiere TMP.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Ce este un fișier TMP? ##

Un fișier TMP se referă la o copie de rezervă tranzitorie, stocare sau alt sistem de fișiere generat de un program software. Este creat ocazional ca un fișier invizibil și este frecvent distrus atunci când programul este oprit. Fișierele TMP pot fi folosite și pentru a stoca temporar informații în timp ce se construiește un fișier nou.

## Format fișier TMP ##

Un fișier TMP este alcătuit de obicei din date brute care sunt utilizate ca o fază în procesul de conversie a materialului de la un stil la altul. Microsoft Word și Apple Safari sunt două aplicații care pot produce și utiliza formatul de fișier TMP.

Documentele TMP generate ar trebui, teoretic, să fie eliminate automat atunci când programul este închis sau mașina este oprită. În practică, acest lucru nu este întotdeauna cazul. Ca rezultat, în timp ce navigați prin documentele programului dvs., puteți întâlni fișiere tranzitorii care nu sunt utilizate în mod activ de sistem sau de orice alt software.

### Memorie auxiliară ###

Memoria virtuală este utilizată în sistemele de operare, cu toate acestea, programele care utilizează volume uriașe de informații ar putea avea nevoie pentru a crea documente temporare.

### Comunicarea intraprocesuala ###

Majoritatea sistemelor de operare oferă primitive pentru transmiterea datelor între programe, cum ar fi conducte, socluri sau memoria principală, dar cea mai simplă metodă este să transferați fișiere într-un fișier temporar și să sfătuiți aplicația care primește locația fișierului temporar.


## Specificatii tehnice ##

Obținerea numelor de documente temporare distinctive este de obicei oferită de sistemele de operare și programele software.
Fișierele temporare pot fi generate în siguranță pe sistemele POSIX folosind funcțiile de bibliotecă mkstemp sau tmpfile. Unele sisteme includ aplicația anterioară POSIX (dispusă) mktemp. Aceste fișiere se găsesc de obicei în directorul temporar obișnuit de pe platformele Unix în /TMP sau %TEMP% (este specific pentru autentificare) pe mașinile Windows.

Când programul se oprește sau documentul este închis, fișierul tranzitoriu generat cu fișierul tmp este eliminat automat. GetTempFileName (Windows) sau tmpnam (POSIX) pot fi folosite pentru a crea un nume de fișier temporar care va dura mai mult decât programul care l-a creat.

## Referință ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
