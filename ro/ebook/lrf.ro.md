{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "fișier", "extensie", "format", "Carte electronică", "Carte digitală"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier LRF și despre API-urile care pot crea și deschide fișiere LRF.",
  "title" :"Format de fișier LRF - Un fișier Sony Portable Reader",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Ce este un fișier LRF?

Un fișier cu extensia .lrf este un fișier electronic Broad Band (BBeB) care conține date pentru un Sony BBeB, inclusiv text, imagini și date de paginare. Fișierul este salvat într-un format binar comprimat care conține un antet, un număr specificat de obiecte și un index de obiecte. Fișierele LRF și LRX includ cele două formate de carte BBeB disponibile. Fișierele LRF nu sunt criptate și pot fi compilate din fișierele [LRX](/ro/ebook/lrf/). Fișierele LRF pot fi convertite din mai multe tipuri de fișiere, inclusiv PDF și HTML. Dacă computerul nu poate deschide fișierul LRF, atunci probabil că nu aveți software-ul instalat pentru a deschide sau edita fișierele LRF. Programele care pot deschide fișiere LRF sunt Caliber, BookDesigner, Makelrf și Canon Book Creator pentru Windows, Caliber pentru Linux, Caliber și Sony Reader pentru Macintosh.

## Scurt istoric

Tipul de fișier LRF este asociat în primul rând cu Line Rider de către [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Line Rider este o jucărie de fizică pe internet și a fost inventată în septembrie 2006 de un student universitar sloven, Boštjan Čadež. Cititoarele electronice de cărți electronice marca Sony (cum ar fi cititoarele Sony PRS-500 și Sony Librie) utilizează extensia de fișier LRF pentru documentele și textele lor. Acest tip de fișier proprietar este acum învechit, precum și fișierele LRS și LRX aferente. Aceste trei tipuri de fișiere au alcătuit BroadBand eBook (BBeB), care a fost întreruptă în 2010, când Sony a început să-și vândă cărțile electronice în format EPUB.

## Format de fișier LRF

Specificațiile detaliate ale formatului de fișier LRF sunt disponibile la [arhivă web](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Un fișier LRF este format din:
* un antet
* un număr de obiecte
* un index de obiecte.

Toate aceste valori sunt în ordinea Intel (LSB primul).

### Antet LRF

|Offset (hex) |Dimensiune (octeți) |Nume/semnificație| Exemplu de valoare|
---|---|---|---|
|0 |8| Semnătura LRF| 4C 00 52 00 46 00 00 00 = „LRF” în Unicode|
|8 |2| versiune?| 999 în majoritatea fișierelor|
|A |2| „Psuedo-Encryption” |byte cheie 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| NumberOfObjects |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| necunoscut| 0|
|24 |1| Steaguri| (16 - spate în față, 1 = față în spate) 16|
|25 |1| necunoscut |(padding?) 0|
|26 |2| necunoscut| 1600|
|28 |2| necunoscut| (umplutură?) 0|
|2A |2| Înălțime?| 600|
|2C |2| Latime?| 800|
|2E |1| necunoscut| 24|
|2F |1| necunoscut |(padding?) 0|
|30 |0x14| necunoscut| zerouri|
|44 |4| ID-ul obiectului numai al obiectului PlaneStream (0x1E). 0x0042|
|48 |4| necunoscut |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Referințe

* [Format de fișier LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - După Wikipedia](https://en.wikipedia.org/wiki/BBeB)

