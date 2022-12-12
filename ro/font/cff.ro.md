{
  "date" : "2020-08-20",
  "keywords" :[ "fișier cff", "format fișier cff", "ce este un fișier cff", "fișier", "exemplu cff", "extensie fișier cff", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Format compact de fișier de font",
  "description":"Aflați despre formatul fișierului CFF și API-urile pentru a crea și deschide fișiere CFF.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Ce este un fișier CFF?

Un fișier cu extensia .cff este un format de font compact și este cunoscut și ca PostScript Type 1 sau CIDFont. CFF acționează ca un container pentru a stoca mai multe fonturi împreună într-o singură unitate cunoscută sub numele de FontSet. Designul fonturilor CFF permite încorporarea codului de limbaj PostScript care permite flexibilitate și extensibilitate suplimentară a formatului pentru utilizarea cu medii de imprimantă. Fișierele cu fonturi CFF pot fi deschise și convertite folosind API-uri precum [Aspose.Font](https://products.aspose.com/font).

## Format de fișier CFF

Fișierele CFF sunt fișiere binare care conțin un aspect structurat de date, au definite tipuri de date, un antet, organizare de glife și dicționare de tabel. Mai multe detalii despre acestea pot fi găsite în [specificațiile formatului de font compact](https://docs.microsoft.com/en-us/typography/opentype/spec/cff).

### Aspect de date
Aspectul de date al formatului de fișier CFF este prezentat mai jos.

|Intrare|Comentarii|
---|---|
|Antet|–|
|NumeINDEX|–|
|Sup INDEX DICT|–|
|Șir INDEX|–|
|Global Subr INDEX|–|
|Codificări–Seturi de caractere|–|
|FDSelect|Numai CIDFonts|
|CharStrings INDEX|per-font|
|Font DICT INDEX|per-font, numai CIDFonts|
|DICT privat|per-font|
|Local Subr INDEX|per-font sau per-Private DICT pentru CIDFonts|
|Notificări privind drepturile de autor și mărcile comerciale|–|

### Tipuri de date

Tipurile de date CFF sunt cele prezentate în tabelul următor.

|Nume|Gamă|Descriere|
---|---|---|
|Card8|0 –255|număr nesemnat de 1 octet|
|Card16|0 – 65535|număr nesemnat de 2 octeți|
|Offset|variază|offset de 1, 2, 3 sau 4 octeți (specificat de câmpul OffSize)|
|OffSize|1–4|numărul nesemnat de 1 octet specifică dimensiunea unui câmp sau câmpuri Offset|
|SID|0 – 64999|identificator de șir de 2 octeți|

### Antet

Datele binare încep cu un antet având formatul prezentat în tabelul următor.

|Tip|Nume|Descriere|
---|---|---|
|Card8|major|Format versiunea majoră (începând cu 1)|
|Card8|minor|Format versiunea minoră (începând cu 0)|
|Card8|hdrSize| Dimensiunea antetului (octeți)|
|OffSize|offSize|Dimensiunea decalajului absolut (0)|

## Referințe

* [Tabel format compact font](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [Format de fișier CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 Chartset](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

