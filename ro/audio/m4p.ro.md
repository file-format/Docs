{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "fișier", "extensie", "format", "ce este formatul fișierului m4p", "muzică", "formatul fișierului m4p", "M4b vs MP3", "specificația formatului fișierului m4p "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier M4P și despre API-urile care pot crea, converti și deschide fișiere M4P.",
  "title" :"M4P - Format de fișier audio MPEG-4",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Ce este un fișier M4P?
Fișierul cu extensia .m4p este un fișier audio care este de obicei disponibil în magazinul Apple iTunes pentru descărcare. Cu alte cuvinte, putem spune că M4P este un fișier AAC, dar protejat la copiere prin utilizarea unui Digital Rights Management (DRM). Înseamnă că fișierele M4P pot fi redate numai pe sisteme sau dispozitive autorizate. De obicei, fișierele M4P sunt specifice dispozitivelor multimedia Apple. Deci, aceste fișiere pot fi redate numai pe macbook-uri Apple, podcasturi, telefoane inteligente precum iPhone 6 sau iPhone 7.

## Format de fișier M4P
M4P înseamnă MPEG 4 Protected (audio) și codifică audio cu codec audio avansat (AAC) și protejează fișierul împotriva utilizării neautorizate a fișierului. Acest format de fișier este de obicei considerat ca format de fișier audio al iTunes Music Store. Apple folosește sistemul său FairPlay Digital Rights Management (DRM) pentru a proteja fișierele M4P. FairPlay DRM se bazează pe tehnologia dezvoltată de Veridisc. Mecanismul său de protecție funcționează prin criptarea fluxului audio AAC folosind criptarea AES. Utilizatorul primește o cheie principală care este atribuită contului său pentru decriptare. Acest format de fișier a fost introdus ca înlocuitor al formatului de fișier MP3, deoarece MP3 nu a fost conceput inițial ca fișier audio, ci ca strat III într-un fișier video MPEG 1 sau 2.


## Specificații pentru formatul fișierului M4P

Similar cu [M4A](/ro/audio/m4a/), fișierele M4P constau, de asemenea, din bucăți consecutive. Fiecare bucată are antet de 8 octeți și este subdivizată astfel:
- Dimensiunea fragmentului de 4 octeți (big-endian, octetul înalt mai întâi)
- tip de bucată de 4 octeți - una dintre semnăturile predefinite: „mdat”, „moov”, „pnot”, „moof”, „udta”, „uuid”, „free”, „skip”, „ftyp”, „jP2”, „wide”, „load”, „imap”, „matt”, „chap”, „kmat”, „clip”, „crgn”, „sync”, „tmcd”, „PICT”, „scpt ", "ctab", "ssrc".

Similar cu M4A, prima bucată din M4P va fi de tip „ftype” și are un subtip la offset 8. M4P este definit de subtip care trebuie să fie „M4P_”.

Repetând bucăți, până când este detectată o bucată de tip necunoscut, va compune fișierul M4P (MPEG-4 Audio).

## Referințe ##

* [MPEG-4 Partea 14 - De Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Exemplu de format și recuperare audio MPEG-4 Partea 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

