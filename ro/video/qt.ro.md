{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier QT - Fișier film rapid",
  "keywords" :[ "QT", "Video QuickTime", "format qt", "cum se redă fișierele qt", "Fișier film rapid", "QTFF", "video", "Apple"],
  "description":"Aflați despre formatul de fișier QT și despre API-urile care pot crea și deschide fișiere QT.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Ce este un fișier QT?

Un fișier cu extensia .qt este un fișier container multimedia care este utilizat de cadrul QuickTime pentru a stoca conținutul fișierelor multimedia. Dezvoltat de Apple Inc., QuickTime File Format (QTFF) este un fișier container multimedia care conține conținut audio, video sau text pentru redare ulterioară. Este formatul ales pentru schimbul de medii digitale între dispozitive, aplicații și sisteme de operare. Fișierele QT sunt salvate și în format [MOV](/ro/video/mov/), care a fost dezvoltat și de Apple Inc. Unele dintre aplicațiile care pot deschide fișiere QT includ Apple QuickTime player, VLC media player și Media Player Classic cu K- Lite Codec Pack.

## Format de fișier QT

QTFF este orientat pe obiecte care expune o colecție flexibilă de obiecte pentru ușurință de analizare și extindere. Fiecare piesă dintr-un fișier QT conține un flux media codificat digital sau o referință de date la fluxul media aflat într-un alt fișier. Structura de date ierarhică constând din obiecte numite atomi acționează ca containere de urme. Specificațiile de format de fișier pentru [formatul de fișier QT](https://developer.apple.com/documentation/quicktime-file-format) sunt disponibile oficial de Apple Inc pentru referința dezvoltatorului.

### Descriere media

Descrierea media a unui fișier QuickTime este stocată separat de datele media. Informații precum numărul de melodii, formatul de compresie video și informațiile de sincronizare sunt stocate în descrierea media (cunoscută și ca resursă de film, atom de film sau pur și simplu film). Datele media sunt referite printr-un index în această structură media. Datele media sunt date efective de eșantion, cum ar fi cadre video și mostre audio, utilizate în film.

### Atomi

Atom este unitatea de bază a fișierului QuickTime. Există două câmpuri majore în orice atom înaintea oricărui alt câmp: câmpurile dimensiune și tip. Câmpul de dimensiune arată dimensiunea atomului, în timp ce câmpul de tip indică tipul de date stocate în atom. Prin natură, atomii sunt ierarhici, ceea ce înseamnă că un atom poate conține alți atomi care încă pot conține alții. Dispunerea unui atom de probă este prezentată în imaginea următoare.

Fiecare atom are două părți, antet și date. Antetul conține câmpurile de dimensiune și tip, iar partea de date conține datele reale. În plus, fiecare câmp este explicat mai jos:

#### Dimensiunea atomului

Antetul atomului și conținutul sunt indicate printr-un număr întreg de 32 de biți cunoscut sub numele de dimensiunea atomului. Câmpul dimensiune conține dimensiunea atomului în octeți, exprimată într-un număr întreg fără semn pe 32 de biți.

#### Tip de atom

Tipul atomului este, de asemenea, afișat printr-un număr întreg de 32 de biți, care este tratat în mare parte ca un câmp de patru caractere cu valoare knemonică, cum ar fi „moov” (0x6D6F6F76) pentru un atom de film sau „trak” (0x7472616B) pentru un atom de urmărire. Odată ce tipul de atom este cunoscut, acesta permite interpretarea datelor acestuia.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Structura fișierului ##

Fișierele QT/MOV constau din bucăți consecutive. Fiecare bucată are un antet de 8 octeți: dimensiunea bucății de 4 octeți (big-endian, octetul mare mai întâi) și tipul de bucată de 4 octeți - una dintre semnăturile predefinite: „ftyp”, „mdat”, „moov”, „pnot „, „udta”, „uuid”, „moof”, „free”, „skip”, „jP2”, „wide”, „load”, „ctab”, „imap”, „matt”, „kmat”, „clip”, „crgn”, „sync”, „chap”, „tmcd”, „scpt”, „ssrc”, „PICT”. Prima bucată este de tip „ftype” și are un subtip la offset 8. MOV definit de subtip care trebuie să fie „qt”. Pentru a compune fișierul MOV, sunt necesare bucăți repetate până când este detectat tipul necunoscut.

Iată un exemplu de exemplu: Inspectând datele binare ale unui fișier MOV eșantion, este evident că acesta începe cu o semnătură **ftyp** (hex: 66 74 79 70) la offset 4, care definește QuickTime Container File Type. Subtipul de fișier este **qt~_~_** (hex: 71 74 20 20) care indică tipul de fișier MOV. Dimensiunea primului bloc este 32 (hex: 00 00 00 20, big-endian, high byte primul), dimensiunea situată la offset 0. La offset 32 (hex: 20) se află a doua bucată, care are dimensiunea de 8 și tip **mdat** (hex: 6D 64 61 74).

Următoarea bucată este situată la offset 32+8#40 (hex: 28) și are o dimensiune 3.263.028 (hex: 00 31 CA 34) și tip **mdat** (hex: 6D 64 61 74) la offset 44 (hex : 2C). Următoarea bucată este situată la offset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) și are dimensiunea 21,189 (hex: 00 00 52 C5) și tip **moov** (hex: 6D 6F 6F) la offset 76 1.836.019.574 (hex: 00 31 CA 60). Aceasta este ultima bucată, deci dimensiunea totală a fișierului este de 3.263.068+21.189#3.284.257 de octeți.

## Referințe ##

* [Format de fișier QT - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [Format de fișier QuickTime - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

