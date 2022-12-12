{
  "date" : "2019-10-11",
  "keywords" :[ "fișier mov", "format fișier mov", "ce este un fișier mov", "fișier", "exemplu mov", "extensie fișier mov", "extensie", "format", "QuickTime", "MPEG- 4" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier MOV - Format fișier Apple QuickTime Movie",
  "description":"Aflați despre formatul de fișier MOV și despre API-urile care pot crea și deschide fișiere MOV.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Ce este un fișier MOV?

Un fișier MOV este un tip de fișier video, dezvoltat de Apple Inc., care conține una sau mai multe piese. Fiecare piesă stochează un film, sunet, clipuri video și subtitrări. Este un container multimedia care poate stoca diferite tipuri de elemente media. Formatul video MOV este compatibil atât cu sistemele Windows, cât și cu Macintosh. Folosește MPEG-4 codificat pentru compresie și pistele sunt menținute în obiecte numite atomi care sunt plasate într-o structură de date ierarhică.

## Scurt istoric al formatului de fișier MOV

Formatul de fișier MPEG-4 a evoluat din specificația QuickTime File Format (**QTFF**) în 2001. Organizația Internațională de Standardizare a aprobat formatul, iar specificațiile sistemelor MPEG-4 Partea 1 au fost publicate în 1999. În 2001, un fișier de revizuire formatul [MP4](/ro/video/mp4/) a fost publicat.

Prima versiune a lui MP4 a fost revizuită în 2003 ca MPEG-4 Part 14 (ISO/IEC 14496-14:2003). În 2004, MP4 a fost generalizat pentru a defini o structură generală pentru toate fișierele media bazate pe timp. Prin urmare, acum este folosit ca bază pentru diferite alte formate de fișiere multimedia.

## Format de fișier QuickTime (QTFF) - Mai multe informații

Pentru a lucra cu multimedia digitală, QTFF poate deține multe tipuri de date. Este un format de idee pentru schimbul de medii digitale, deoarece formatul definește standardele pentru descrierea oricărui tip de structuri media. Formatul de fișier constă dintr-o colecție flexibilă de obiecte orientate pe obiecte. Pentru stocarea filmelor pe discuri, QuickTime folosește două structuri și anume `atomi` și `atomi QT`.

### Atomi

Atom este unitatea de bază a fișierului QuickTime. Există două câmpuri majore în orice atom înaintea oricărui alt câmp: câmpurile dimensiune și tip. Câmpul de dimensiune arată dimensiunea atomului, în timp ce câmpul de tip indică tipul de date stocate în atom. Prin natură, atomii sunt ierarhici, ceea ce înseamnă că un atom poate conține alți atomi care încă pot conține alții. Dispunerea unui atom de probă este prezentată în imaginea următoare.

Fiecare atom are două părți, „header” și „date”. Antetul conține câmpurile de dimensiune și tip, iar partea de date conține datele reale. În plus, fiecare câmp este explicat mai jos:

### Dimensiunea atomului

Antetul atomului și conținutul sunt indicate printr-un număr întreg de 32 de biți cunoscut sub numele de dimensiunea atomului. Câmpul dimensiune conține dimensiunea atomului în octeți, exprimată într-un număr întreg fără semn pe 32 de biți.

### Tip de atom

Tipul atomului este, de asemenea, afișat printr-un număr întreg de 32 de biți, care este tratat în mare parte ca un câmp de patru caractere cu valoare knemonică, cum ar fi „moov” (0x6D6F6F76) pentru un atom de film sau „trak” (0x7472616B) pentru un atom de urmărire. Odată ce tipul de atom este cunoscut, acesta permite interpretarea datelor acestuia.

### QT Atomi și containere de atomi

Atomii QT oferă un format de stocare de uz general și au un antet extins format din câmpuri Dimensiune, Tip, ID atom și Număr de atomi copii. Atomii QT sunt înfășurați într-un container de atomi, o structură de date unică având un antet cu un număr de blocare. Există un atom rădăcină în fiecare recipient de atom, care este atomul QT. Dispunerea atomului QT este prezentată în figura de mai jos.

Antetul containerului QT atom are următoarele date:

Rezervat: un element de 10 octeți cu o valoare de 0.

Blocare număr: întreg de 16 biți cu o valoare de 0.

Antetele QT atom au următoarele date:

**Dimensiunea -** Antetul atomului QT și conținutul sunt indicate în octeți printr-un număr întreg de 32 de biți. În cazul unui atom de frunză, atunci acest câmp conține dimensiunea unui singur atom.

**Tip -** Tipul atomului este indicat printr-un număr întreg de 32 de biți. În cazul în care este atomul rădăcină, atunci valoarea este setată la „sean”.

**Atom ID -** Este un număr întreg de 32 de biți care arată ID-ul atomului și trebuie să fie unic pentru toți frații. Atom rădăcină întotdeauna valoarea ID-ului atomului este 1.

**Rezervat -** Un număr întreg de 16 biți care trebuie setat la 0.

**Număr de copii -** Un număr întreg de 16 biți care indică numărul de atomi copii ai unui atom.

**Rezervat -** Un întreg pe 32 de biți care trebuie setat la 0.

## Structura fișierelor MOV

Fișierele MOV constau din bucăți consecutive. Fiecare bucată are un antet de 8 octeți: dimensiunea bucății de 4 octeți (big-endian, octetul mare mai întâi) și tipul de bucată de 4 octeți - una dintre semnăturile predefinite: „ftyp”, „mdat”, „moov”, „pnot „, „udta”, „uuid”, „moof”, „free”, „skip”, „jP2”, „wide”, „load”, „ctab”, „imap”, „matt”, „kmat”, „clip”, „crgn”, „sync”, „chap”, „tmcd”, „scpt”, „ssrc”, „PICT”. Prima bucată este de tip „ftype” și are un subtip la offset 8. MOV definit de subtip care trebuie să fie „qt”. Pentru a compune fișierul MOV, sunt necesare bucăți repetate până când este detectat tipul necunoscut.

Iată un „exemplu de exemplu”: Inspectând datele binare ale unui fișier MOV eșantion, este evident că acesta începe cu o semnătură **ftyp** (hex: 66 74 79 70) la offset 4, care definește QuickTime Container File Type. Subtipul de fișier este **qt~_~_** (hex: 71 74 20 20) care indică tipul de fișier MOV. Dimensiunea primului bloc este 32 (hex: 00 00 00 20, big-endian, high byte primul), dimensiunea situată la offset 0. La offset 32 (hex: 20) se află a doua bucată, care are dimensiunea de 8 și tip **mdat** (hex: 6D 64 61 74).

Următoarea bucată este situată la offset 32+8#40 (hex: 28) și are o dimensiune 3.263.028 (hex: 00 31 CA 34) și tip **mdat** (hex: 6D 64 61 74) la offset 44 (hex : 2C). Următoarea bucată este situată la offset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) și are dimensiunea 21,189 (hex: 00 00 52 C5) și tip **moov** (hex: 6D 6F 6F) la offset 76 1.836.019.574 (hex: 00 31 CA 60). Aceasta este ultima bucată, deci dimensiunea totală a fișierului este de 3.263.068+21.189#3.284.257 de octeți.

## Cum se convertesc fișierul MOV?

Există o mulțime de playere media și editoare video software disponibile pentru a converti fișiere MOV în alte formate de fișiere video populare. Unele dintre playerele media care pot converti fișiere MOV în alte formate includ:

* Player media VideoLAN VLC
* Eltima Elmedia Player

Mai multe playere media și editoare video, inclusiv VideoLAN VLC media player și Eltima Elmedia Player, pot converti fișiere MOV în alte formate. Acest software poate converti fișiere MOV în următoarele formate video.

* Video MPEG-4 - [MP4](/ro/video/mp4/)
* WebM Video - [WEBM](/ro/video/webm/)
* Flux de transport video - [TS](/ro/video/ts/)
* Format de sisteme avansate - [ASF](/ro/video/ts/)
* Ogg Vorbis Audio - [OGG](/ro/audio/ogg/)
* Audio MP3 - [MP3](/ro/audio/mp3/)
* Codec audio gratuit fără pierderi - [FLAC](/ro/audio/flac/)
* WAVE Audio - [WAV](/ro/audio/wav/)

## Open Source API pentru fișiere MOV

* [React Native API pentru a converti MOV în MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [API-ul Python pentru a repara fișierele MOV](https://github.com/nrosenstein-stuff/movrepair)
* [API Ruby pentru a converti MOV în GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Referințe

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

