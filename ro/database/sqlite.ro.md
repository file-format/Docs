{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier SQLITE și despre API-urile care pot crea și deschide fișiere SQLITE.",
  "title" :"Format fișier SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Ce este un fișier SQLite?

Un fișier cu extensia .sqlite este un fișier de bază de date SQL ușor creat cu software-ul [SQLite](https://www.sqlite.org/index.html). Este o bază de date într-un fișier propriu-zis și implementează un motor de bază de date autonome, cu funcții complete și de mare încredere [SQL](/ro/database/sql/). Fișierele bazei de date SQLite pot fi folosite pentru a partaja conținut bogat între sisteme prin simpla schimbare a acestor fișiere prin rețea. Aproape toate telefoanele mobile și computerele folosesc SQLite pentru stocarea și partajarea datelor și este alegerea formatului de fișier pentru aplicațiile multiplatforme. Datorită utilizării sale compacte și utilizării ușoare, vine la pachet în alte aplicații. Legăturile SQLite există pentru limbaje de programare precum C, [C#](/ro/programming/cs/), [C++](/ro/programming/cpp), [Java](/ro/programming/java/), [PHP](/ro/programming/php/ ), și multe altele.

## Format de fișier SQLite

SQLite în realitate este o bibliotecă C-Language care implementează RDBMS SQLite folosind formatul de fișier SQLite. Odată cu evoluția noilor dispozitive în fiecare zi, formatul său de fișier a fost păstrat compatibil înapoi pentru a găzdui dispozitive mai vechi. Formatul de fișier SQLite este văzut ca format de arhivare pe termen lung pentru date.

### Fișierul bazei de date

O bază de date SQLite este întreținută complet prin două fișiere.
* Fișier bază de date principală - Conține starea completă a bazei de date SQLite
* Rollback Journal - Stochează informații suplimentare într-un al doilea fișier și este utilizat în timpul efectuării tranzacțiilor. În cazul în care SQLite este în modul WAL, este menținut un fișier jurnal al capului de scriere.

#### Fișier Jurnal

Acest fișier este menit să păstreze toate informațiile păstrate în cazul în care ultima tranzacție nu a putut fi finalizată în cazuri precum o defecțiune a computerului. Acest fișier este utilizat pentru a restabili fișierul bazei de date la o stare consecventă.

#### Pagini

Fișierul principal al bazei de date SQLite cuprinde una sau mai multe pagini. În orice moment, fiecare pagină din baza de date principală are o singură utilizare, care este una dintre următoarele:

* Pagina lock-byte
* O pagină freelist
* O pagină trunk listă gratuită
* O pagină de frunză cu listă gratuită
* O pagină b-tree
* O pagină interioară a tabelului b-tree
* O pagină cu frunze de tabel b-tree
* O pagină interioară cu index b-tree
* O pagină cu index b-tree
* O pagină de depășire a încărcăturii utile
* O pagină de hartă cu indicator

Dimensiunea fișierelor bazei de date SQLite poate varia de la câțiva kilobytes la câțiva gigabytes.

### Antet SQLite

Antetul bazei de date SQLite este localizat în primii 100 de octeți ai fișierului bazei de date. Fiecare fișier valid al bazei de date SQLite începe cu 16 octeți (în hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Detaliile câmpurilor de antet sunt ca în tabelul următor.

|Offset|Dimensiune|Descriere|
---|---|---|
|0|16|Șirul de antet: „SQLite format 3\000”|
|16|2|Dimensiunea paginii bazei de date în octeți. Trebuie să fie o putere de doi între 512 și 32768 inclusiv, sau valoarea 1 reprezentând o dimensiune de pagină de 65536.|
|18|1|Versiunea de scriere a formatului de fișier. 1 pentru moștenire; 2 pentru WAL.|
|19|1|Versiune citită în format de fișier. 1 pentru moștenire; 2 pentru WAL.|
|20|1|Bytes de spațiu „rezervat” neutilizat la sfârșitul fiecărei pagini. De obicei 0.|
|21|1|Fracția maximă a sarcinii utile încorporate. Trebuie să aibă 64.|
|22|1|Fracția de sarcină utilă încorporată minimă. Trebuie să fie 32.|
|23|1|Fracția de sarcină utilă a frunzei. Trebuie să fie 32.|
|24|4|Contor modificări fișiere.|
|28|4|Dimensiunea fișierului bazei de date în pagini. „Dimensiunea bazei de date din antet”.|
|32|4|Numărul paginii primei pagini trunk freelist.|
|36|4|Numărul total de pagini freelist.|
|40|4|Cookie-ul schema.|
|44|4|Numărul formatului schemei. Formatele de schemă acceptate sunt 1, 2, 3 și 4.|
|48|4|Dimensiunea implicită a memoriei cache a paginii.|
|52|4|Numărul paginii celei mai mari pagini rădăcină b-tree atunci când sunteți în modurile auto-vacuum sau incremental-vacuum sau zero în caz contrar.|
|56|4|Codificarea textului bazei de date. O valoare de 1 înseamnă UTF-8. O valoare de 2 înseamnă UTF-16le. O valoare de 3 înseamnă UTF-16be.|
|60|4|„Versiunea utilizatorului” citită și setată de pragma versiunea_utilizator.|
|64|4|Adevărat (diferit de zero) pentru modul de vid incremental. Fals (zero) altfel.|
|68|4|„ID-ul aplicației” setat de PRAGMA application_id.|
|72|20|Rezervat pentru extindere. Trebuie să fie zero.|
|92|4|Numărul de versiune-valid-pentru.|
|96|4|SQLITE_VERSION_NUMBER|

## Referințe ##

* [Format de fișier SQLite - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - Specificații limbaj C](https://www.sqlite.org/c3ref/intro.html)

