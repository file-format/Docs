{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "fișier", "extensie", "format", "ce este formatul fișierului m4b", "muzică", "formatul fișierului m4b", "M4b vs MP3", "specificația formatului fișierului m4b "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier M4B și despre API-urile care pot crea, converti și deschide fișiere M4B.",
  "title" :"M4B - Format de fișier audio MPEG-4",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Ce este un fișier M4B?

Fișierul cu extensia .m4b este o carte audio folosită în general de cărțile Apple și iTunes. Audio folosit în acest format este stocat în MPEG-4 și comprimat folosind codificarea AAC. Un fișier M4B este foarte asemănător cu M4A, dar are suport pentru caracteristicile legate de cărți audio, cum ar fi marcajele și pauzele de capitol. Fișierele M4B sunt disponibile atât în versiunea DRM activată, cât și în versiunea fără DRM. Cărțile audio criptate DRM sunt de obicei cărți audio plătite din iTunes Store. În timp ce, DRM free poate fi găsit cu ușurință pe internet.

## Format de fișier M4B

Fișierele audiobook care conțin metadate, imagini, marcaje și hyperlink-uri pot fi salvate cu extensia .m4a, dar, în general, extensia .m4b este folosită în timpul salvării, doar pentru a specifica că fișierul are un format de fișier audiobook. Fairplay DRM (Digital Rights Management) este folosit de aplicați pentru a-și proteja fișierele M4B. Deci fișierele descărcate de pe iTunes pot fi redate doar pe dispozitive sau computere autorizate.


## M4B vs M4A

Atât M4B, cât și [MP3](/audio/mp3/) sunt formate de fișiere doar audio.

**M4B**: Câștigă în comparație cu MP3 în ceea ce privește calitatea dacă se codifică ambele la aceeași rată de biți. M4B este un fișier de carte audio care este comprimat folosind codificarea AAC. Practic este asociat cu „MPEG-4 Audio Layer”, fișierele cu extensia .m4b sunt stratul audio al filmelor MPEG-4, dar cu caracteristici suplimentare legate de audiobook. Scopul său este să depășească MP3-ul și să devină noul standard în compresia audio. Este foarte aproape de MP3 în multe privințe, dar a fost dezvoltat pentru a avea o calitate mai bună la aceeași dimensiune sau chiar mai mică. Formatul M4B a fost introdus pentru prima dată de Apple. Tipul de format este, de asemenea, realizat ca Apple Lossless Encoder (ALE).

Prin urmare, în prezent, M4B nu a putut obține succesul popular al MP3-ului, deoarece formatul audio nu este încă redabil în mod obișnuit.

**Mp3**: un format audio digital care este bine familiar pentru toată lumea. Un prim format de compresie pe scena și a devenit foarte faimos printre ascultătorii de muzică. Succesul său general este atât de rapid încât tipul de fișier poate fi redat universal și compatibil cu aproape orice, hardware sau software. Într-un sens general, M4A va produce o calitate mai bună a sunetului, dar mulți ar susține că, indiferent dacă este adevărat sau nu, diferența de sunet nu este comparabilă și ar fi o pierdere de timp să încerci să convertești fișiere MP3 în fișiere M4A. În cele din urmă, conversia vă va face să pierdeți calitatea originală a sunetului.

## Specificația formatului fișierului M4B

Similar cu [M4A](/ro/audio/m4a/), fișierele M4B constau, de asemenea, din bucăți consecutive. Fiecare bucată are antet de 8 octeți și este subdivizată astfel:
- Dimensiunea fragmentului de 4 octeți (big-endian, octetul înalt mai întâi)
- tip de bucată de 4 octeți - una dintre semnăturile predefinite: „ftyp”, „mdat”, „moov”, „pnot”, „moof”, „udta”, „uuid”, „free”, „ctab”, „skip”, „jP2”, „wide”, „load”, „imap”, „matt”, „chap”, „kmat”, „clip”, „crgn”, „sync”, „tmcd”, „PICT ", "scpt", "ssrc".

Similar cu M4A, prima bucată din M4B va fi de tip „ftype” și are un subtip la offset 8. M4B este definit de subtip care trebuie să fie „M4B_”.

Repetând bucăți, până când este detectată o bucată de tip necunoscut, va compune fișierul M4B (MPEG-4 Audio).

## Referințe

* [MPEG-4 Partea 14 - De Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Exemplu de format și recuperare audio MPEG-4 Partea 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

