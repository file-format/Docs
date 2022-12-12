{
  "date" : "2021-04-08",
  "keywords" :[ "fișier mst", "format fișier mst", "ce este un fișier mst", "fișier", "exemplu mst", "extensie fișier mst", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - LU Library Archive File Format",
  "description":"Aflați despre formatul de fișier LBR și despre API-urile care pot crea și deschide fișiere LBR.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Ce este un fișier LBR?

Un fișier cu extensia .lbr este un fișier de arhivă creat cu programul LU și utilizat pe sistemele de operare CP/M și DOS în anii 1980. Nu mai este folosit și a fost înlocuit cu formate moderne de fișiere de arhivare. Formatul nu comprimă fișierele membre și acționează ca arhivă container pentru acestea. Caracteristica de arhivare a fost folosită în principal pentru transferul fișierelor arhivate pe internet. Deoarece LBR nu oferea compresie, alte utilitare, cum ar fi SQ sau CRUNCH, au fost folosite pentru a comprima fișierele membre pre-arhivare sau fișierul de arhivă rezultat după arhivare pentru a reduce dimensiunea acestuia.

## Format de fișier LBR

Formatul de fișier LBR a fost conceput de Gary P. Novosielski și nu are detalii tehnice disponibile public. Fișierele LBR încep cu un octet 0x00, urmat de 11 spații (0x20), apoi doi octeți 0x00, apoi doi octeți care nu sunt ambii 0x00. Fiind format de fișier container, acesta poate fi extras folosind LU.COM și NULU.COM.

## Referințe

* [LBR - Wikipedia](https://en.wikipedia.org/wiki/LBR_(format_fișier))

