{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier MPG",
  "keywords" :[ "MPG", "fișier", "extensie", "format", "format video", "ce este un format de fișier mpg", "format de fișier mpg", "player fișier mpg", "compresie mpeg", "video ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Aflați despre formatul de fișier MPG și despre API-urile care pot crea și arăta cum să deschideți fișierele MPG.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Ce este un format de fișier MPG? ##

Fișierul cu extensia .mpg aparține grupului de extensii de fișiere pentru compresia audio și video MPEG-1 sau MPEG-2. Videoclipul MPEG-1 Partea 2 nu este ușor disponibil, iar această extensie (format de fișier MPG) indică de obicei un flux de programe MPEG care este definit în MPEG-1 și MPEG-2 sau un flux de transport MPEG care este definit în MPEG-2 . Există și alte extensii, cum ar fi .m2ts, care specifică containerul exact, în acest caz, MPEG-2 TS, dar acest lucru are puțină pertinență pentru media MPEG-1. [.mp3](/audio/mp3/) este cea mai comună extensie pentru fișierele care conțin audio MP3. Un fișier MP3 este un flux tipic de audio brut; modalitatea tradițională de etichetare a fișierelor MP3 este prin scrierea datelor de flux în segmentele „gunoi” ale fiecărui cadru, care salvează informațiile media, dar sunt eliminate de **mpg file player**. Aceasta este o tehnică similară folosită pentru a eticheta fișierele AAC, dar mai puțin acceptată în zilele noastre.

## Compresie MPEG ##

Numele MPEG înseamnă Moving Pictures Experts Group. MPEG este un instrument de compresie video, care implică comprimarea imaginilor și sunetelor, precum și sincronizarea celor două.
În prezent, există mai multe standarde MPEG.

- MPEG-1 este propus pentru ratele de date intermediare, de ordinul a 1,5 Mbit/sec.
- MPEG-2 este propus pentru rate mari de date de cel puțin 10 Mbit/sec.
- MPEG-3 a fost propus pentru compresia HDTV, dar sa dovedit a fi redundant și a fost fuzionat cu MPEG-2.
- MPEG-4 este propus pentru rate de date foarte mici, mai mici de 64 Kbit/sec.


## Flux de program în format de fișier MPG ##

Fluxul de program este un container pentru multiplexarea audio digitală, video și multe altele. Formatul Program Stream este specificat în prima parte a MPEG-1 (ISO/IEC 11172-1) și în prima parte a MPEG-2, Sisteme (standard ISO/IEC 13818-1/ITU-T H.222.0). Fluxul de programe MPEG-2 este bazat pe analog și similar cu stratul de sisteme ISO/IEC 11172 și compatibil înainte.

### Detalii de codificare ###

Iată detaliile de codare ale formatului de antet al pachetului de flux de programe MPEG-2 parțial:

| Nume | Numărul de biți | Descriere |
---|---|---|
| octeți de sincronizare | 32 | 0x000001BA |
| biți de marcare | 2 | 01b pentru versiunea MPEG-2. Biții de marcare pentru versiunea MPEG-1 sunt 4 biți cu valoarea 0010b. |
| Ceas sistem [32..30] | 3 | Referința ceasului de sistem (SCR) biți de la 32 la 30 |
| bit marker | 1 | 1 bit întotdeauna setat. |
| Ceas sistem [29..15] | 15 | Biți de ceas de sistem de la 29 la 15 |
| bit marker | 1 | 1 bit întotdeauna setat. |
| Ceas sistem [14..0] | 15 | Biți de ceas de sistem de la 14 la 0 |
| bit marker | 1 | 1 bit întotdeauna setat. |
| Extensie SCR | 9 | |
| bit marker | 1 | 1 bit întotdeauna setat. |
| rata de biți | 22 | În unități de 50 de octeți pe secundă. |
| biți de marcare | 2 | 11 biți întotdeauna setați. |
| rezervat | 5 | rezervat pentru utilizare viitoare |
| lungimea umpluturii | 3 | |
| umplutură octeți | 8*lungimea umpluturii | |
| antet sistem (opțional) | 0 sau mai mult | dacă codul de pornire al antetului sistemului urmează: 0x000001BB |

Următorul tabel arată formatul parțial al antetului sistemului:

| Nume | Număr de octeți | Descriere |
---|---|---|
| octeți de sincronizare | 4 | 0x000001BB |
| lungime antet | 2 | |
| rata legată și biți de marcare | 3 | |
| legat audio și steaguri | 1 | |
| steaguri, bit de marcator și legat video | 1 | |
| Restricția ratei pachetelor și octetul rezervat | 1 | |


## Referințe ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



