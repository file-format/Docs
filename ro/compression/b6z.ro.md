{
  "date" : "2019-10-11",
  "keywords" :[ "fișier b6z", "format fișier b6z", "ce este un fișier b6z", "fișier", "exemplu b6z", "extensie fișier b6z", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - Format de fișier arhivă B6ZIP",
  "description":"Aflați despre formatul de fișier B6Z și despre API-urile care pot crea și deschide fișiere B6Z.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Ce este un fișier B6Z?

Un fișier cu extensia .b6z este un fișier de arhivă comprimat creat de aplicația software macOS [B6Zip](http://b6zip.com) care este utilizat pentru comprimarea și decomprimarea fișierelor. Este un format de arhivă relativ nou, care permite o rată de compresie mai mare. B6Z are arhitectură deschisă și acceptă dimensiuni de fișiere de până la 900000 PB. Acceptă compresia datelor, recuperarea erorilor și extinderea fișierelor. Software-ul utilitar B6Zip este disponibil gratuit pe MacOS pentru a deschide diferite tipuri de fișiere comprimate, inclusiv B6Z.

## Format de fișier B6Z

Formatul de fișier B6Z se bazează pe arhitectură deschisă și oferă o compresie solidă cu algoritmul de criptare AES-256. Folosește LZMA2 ca metodă de compresie implicită, dar acceptă și alte metode de compresie, după cum urmează.

|Metodă|Descriere|
---|---|
|LZMA |Versiune optimizată a algoritmului LZ77|
|LZMA2| Versiune îmbunătățită a LZMA|
|Dezumflare| Algoritm LZ77 obișnuit|
|BZip2| Algoritm BWT standard|
|PPMD| PPMdH a lui Dmitri Shkarin|

Utilitarul B6Zip acceptă toate aceste standarde de compresie și este extrem de optimizat, rezultând viteză mare. Acceptă lucrul cu formatele de fișier [ZIP](/ro/compression/zip/), [TAR](/ro/compression/tar/) și [RAR](/ro/compression/rar/). Fișierele B6Z au tip MIME application/x-b6z-compressed.

## Referințe

* [B6Zip](http://b6zip.com)

