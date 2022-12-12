{
  "date" : "2019-10-11",
  "keywords" :[ "fișier tar", "format fișier tar", "ce este un fișier tar", "fișier", "exemplu tar", "extensie fișier tar", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Format de fișier arhivă Unix",
  "description":"Aflați despre ce este un fișier Tar și API-urile care pot crea și deschide fișiere TAR.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier TAR?

Fișierele cu extensia .tar sunt arhive create cu un utilitar bazat pe Unix pentru a colecta unul sau mai multe fișiere. Mai multe fișiere sunt stocate într-un format necomprimat, cu suport pentru adăugarea de fișiere, precum și de foldere la arhivă. Utilitarul TAR pe Unix se bazează pe comandă, dar fișierele create prin urmare sunt acceptate de majoritatea sistemelor de arhivare a fișierelor pe aproape toate sistemele de operare. A fost creat pentru prima dată în 1979 de către AT&T Bell Laboratories, iar versiunile ulterioare au fost publicate odată cu trecerea timpului.

## Format de fișier TAR

TAR este un format de fișier deschis cu specificații complete disponibile pentru referința dezvoltatorului. Structura sa de fișiere a fost standardizată în POSIX.1-1988 și mai târziu în POSIX.1-2001. Seturile de date create de tar rețin informații despre parametrii sistemului de fișiere, cum ar fi:

* Nume
* Marcaje de timp
* Proprietate
* Permisiuni de acces la fișiere
* Organizare director

Un fișier Tar nu are niciun număr magic. Conține o serie de blocuri în care fiecare bloc este de BLOCKSIZE octeți.

Fiecare fișier arhivat este reprezentat de un bloc antet care descrie fișierul, urmat de zero sau mai multe blocuri care oferă conținutul fișierului. La sfârșitul fișierului arhivă există două blocuri de 512 de octeți umplute cu zerouri binare ca marcator de sfârșit de fișier. Un sistem rezonabil ar trebui să scrie un astfel de marcator de sfârșit de fișier la sfârșitul unei arhive, dar nu trebuie să presupună că un astfel de bloc există atunci când citește o arhivă. În special, GNU tar emite întotdeauna un avertisment dacă nu îl întâlnește.

Blocurile pot fi blocate pentru operațiuni fizice I/O. Fiecare înregistrare de n blocuri (unde n este setat de factorul de blocare = opțiunea 512-size la tar) este scrisă cu o singură operație „write()”. Pe benzile magnetice, rezultatul unei astfel de scrieri este o singură înregistrare. Când scrieți o arhivă, ultima înregistrare a blocurilor ar trebui să fie scrisă la dimensiunea completă, blocurile după blocul zero conținând toate zerourile. Când citește o arhivă, un sistem rezonabil ar trebui să gestioneze în mod corespunzător o arhivă a cărei ultima înregistrare este mai scurtă decât restul sau care conține înregistrări deșeuri după un bloc zero.

### Antet gudron

Ca orice alt antet de fișier, înregistrarea antetului fișierului tar conține metadate despre un fișier și este prezentată în tabelul următor.


|Decalaj câmp|Dimensiunea câmpului (octeți)|Câmp
---|---|---|
|0|100|Numele fișierului
|100|8|Modul fișier
|108|8|ID utilizator numeric al proprietarului
|116|8|ID-ul de utilizator numeric al grupului
|124|12|Dimensiunea fișierului în octeți (bază octală)
|136|12|Ora ultimei modificări în format numeric de timp Unix (octal)
|148|8|Suma de control pentru înregistrarea antetului
|156|1|Indicator link (tip fișier)
|157|100|Numele fișierului legat

Câmpurile neutilizate sunt completate cu octeți NUL. Un antet constă din 257 de octeți, care este umplut cu octeți NUL pentru a se umple până la înregistrarea de 512 de octeți.

## Referințe ##

* [TAR - După Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))
* [Format de bază TAR](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

