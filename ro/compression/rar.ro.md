{
  "date" : "2019-10-11",
  "keywords" :[ "fișier rar", "format fișier rar", "ce este un fișier rar", "fișier", "exemplu rar", "extensie fișier rar", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Ce este o extensie de fișier RAR și API-uri care pot crea și deschide fișiere RAR.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier RAR?

Fișierele cu extensia .rar sunt fișiere de arhivă care sunt create pentru stocarea informațiilor în formă comprimată sau normală. RAR, care înseamnă Roshal ARchive file format, este un format de fișier proprietar creat de Eugene Roshal în 1995, care era un inginer rus de software. Formatul este folosit pentru a arhiva fișiere cu diferite metode, inclusiv diferite tehnici de compresie. Există mai multe aplicații software disponibile pentru Windows, Linux și MacOS pentru extragerea fișierelor RAR. Software-ul WinRAR, de la RARlab, este utilitarul de arhivare a fișierelor shareware (gratuit timp de 40 de zile) pentru platforma Microsoft Windows; software-ul a fost portat pe Linux (doar ca extractor) de către același autor, Eugene Roshal.

## Istoricul versiunilor formatului de fișier RAR

* v1.3 (original, nu are semnătura „Rar!”)
* v1.5
* v2.0 - lansat cu WinRAR 2.0 și Rar pentru MS-DOS 2.0
* v2.9 - lansat în WinRAR versiunea 3.00
* v5.0 - acceptat de WinRAR 5.0 și versiuni ulterioare

## Caracteristici cheie ale formatului RAR

RAR a fost în domeniu de destul de mult timp și a fost unul dintre formatele de fișiere de arhivare preferate. Caracteristicile cheie ale formatului RAR sunt:

**`Raport de compresie ridicat:`** Superior în comparație cu [ZIP](/ro/compression/zip/), comparabil cu formatul 7z și zipx.

**`Criptare puternică a fișierelor prin design:`** Arhivele RAR4 criptate se bazează pe criptarea bazată pe AES-128, în timp ce arhivele RAR5 criptate se bazează pe criptarea AES-256 cu programare îmbunătățită a cheilor

**`Capacități avansate de corecție a erorilor și de recuperare a datelor:`** înregistrări opționale de recuperare în timpul creării arhivei

**`Dimensiunea fișierului:`** Minim 20 de octeți și maxim 2^63 de octeți (8 exaocteți din dimensiunea totală a arhivei)

**`Arhive RAR cu mai multe volume:`** Posibilitatea de a împărți arhivele mari în mai multe fișiere mai mici pentru a facilita transferul în rețea. În acest caz, extensiile de fișiere sunt incrementate cu 1 pentru a reprezenta volumele împărțite

## Format de fișier RAR

Specificațiile complete ale formatului RAR nu sunt disponibile public și de aceea detaliile despre format nu pot fi formulate într-o manieră concisă.

### Aspect general al arhivei

Aspectul general al unui format de fișier RAR introdus în versiunea 5.0 este următorul:

|Format de fișier
---|
|Modul autoextractabil (opțional)
|RAR 5.0 Semnătura
| Antet de criptare arhivă (opțional)
| Antetul principal al arhivei
|Arhivați antetul serviciului de comentarii (opțional)
Antetul fișierului 1
| Anteturi de serviciu (NTFS ACL, fluxuri etc.) pentru fișierul precedent (opțional)
|...
| Antetul fișierului N
| Anteturi de serviciu (NTFS ACL, fluxuri etc.) pentru fișierul precedent (opțional)
|Înregistrare de recuperare (opțional)
|Sfârșitul antetului arhivei

Informații despre fiecare secțiune a fișierului RAR menționată mai sus pot fi găsite în documentul [Specificații format fișier RAR 5.0](https://www.rarlab.com/technote.htm#arcstruct).

#### Arhive RAR cu autoextractie

Dacă fișierul RAR în sine se extrage automat, informațiile care se extrag automat sunt conținute la începutul fișierului care precede semnătura arhivei. Mărimea și conținutul acestuia nu sunt definite.

#### Semnătura RAR 5.0

Semnătura RAR este un antet de 8 octeți care constă din următorul număr magic:

0x 52 61 72 21 1A 07 00

Unde

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Referințe

* [Format de arhivă RAR 5.0](https://www.rarlab.com/technote.htm)
* [RAR - După Wikipedia](https://en.wikipedia.org/wiki/RAR_(format_fișier))

