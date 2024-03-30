{
  "date" : "2021-04-08",
  "keywords" :[ "fișier lzma", "format fișier lzma", "ce este un fișier lzma", "fișier", "exemplu lzma", "extensie fișier lzma", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - Format de fișier comprimat LZMA",
  "description":"Ce este un fișier LZMA și API-urile care pot crea și deschide fișiere LZMA.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Ce este un fișier LZMA?

Un fișier cu extensia .lzma este un fișier de arhivă comprimat creat folosind metoda de compresie LZMA (Lempel-Ziv-Markov chain Algorithm). Acestea sunt găsite/utilizate în principal pe sistemul de operare Unix și sunt similare cu alți algoritmi de compresie, cum ar fi [ZIP](/ro/compression/zip/) pentru a minimiza dimensiunea fișierului. LZMA este un format de fișier vechi, care este sau a fost înlocuit cu formatul .xz. Tipul MIME al formatului .lzma este \`application/x-lzma'. Acest format de fișier a fost conceput de Igor Pavlov pentru a fi utilizat în LZMA SDK.

## Format de fișier LZMA

Fișierul LZMA este format din două părți principale:

1. Antet
1. Date comprimate


### Antet LZMA

Fișierele LZMA au un antet de 13 octeți care este urmat de datele comprimate LZMA. Antetul LZMA este format din:

* Proprietăți
* Dimensiunea dicționarului
* Dimensiune necomprimată

#### Proprietăți antet LZMA

Câmpul Proprietăți conține trei proprietăți. O abreviere este dată în paranteze, urmată de intervalul de valori al proprietății. Domeniul este format din

1) numărul de biți de context literal (lc, [0, 8]);
2) numărul de biți de poziție literală (lp, [0, 4]); și
3) numărul de biți de poziție (pb, [0, 4]).

#### Dicţionar LZMA Size

Acesta este stocat ca un întreg mic endian pe 32 de biți fără semn, cu valori cuprinse între 2^n și 2^n + 2^(n-1). LZMA Utils poate decomprima fișiere cu orice dimensiune de dicționar.

#### Dimensiune necomprimată
Dimensiunea necomprimată este stocată ca un întreg mic endian nesemnat pe 64 de biți. O valoare specială de 0xFFFF_FFFF_FFFF_FFFF indică faptul că dimensiunea necomprimată este necunoscută. Valoarea este reprezentată de marcatorul de sfârșit de sarcină utilă (\*) dacă și numai dacă dimensiunea necomprimată este necunoscută.

## Referințe
* [Algoritmul lanțului Lempel–Ziv–Markov](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
