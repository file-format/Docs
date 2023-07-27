{
  "date" : "2019-10-11",
  "keywords" :[ "fișier tbz", "format fișier tbz", "ce este un fișier tbz", "fișier", "exemplu tbz", "extensie fișier tbz", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Arhiva de gudron comprimat Bzip",
  "description":"Aflați despre formatul de fișier TBZ și despre API-urile care pot crea și deschide fișiere TBZ.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Ce este un fișier TBZ?

Un fișier cu extensia .tbz este o arhivă comprimată care utilizează compresia BZIP pentru a reduce dimensiunea fișierelor de conținut. Fișierele TBZ sunt de fapt fișiere arhivate UNIX [TAR](/ro/compression/tar/) care sunt apoi comprimate cu BZIP. Cea mai recentă compresie de nivel al doilea este [BZIP2](/ro/compression/bz2/) care a înlocuit BZIP. Formatul de fișier TBZ este potrivit pentru transferul de fișiere mari. Fișierele TBZ pot fi deschise/extrase folosind aplicații software precum 7-Zip, PeaZip și jZip. Utilizatorii Linux și macOS pot deschide, de asemenea, un TBZ cu comanda BZIP2 dintr-o fereastră de terminal.

## Format de fișier TBZ

Fișierele TBZ sunt de fapt arhive comprimate create cu compresie BZIP/[BZIP2](/ro/compression/bz2/). Nu există specificații formale disponibile pentru acest format de fișier. Cu toate acestea, o [specificații de inginerie inversă] neoficială (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) arată că un flux .bz2 constă dintr-un antet de 4 octeți care este urmat cu zero sau mai multe blocuri comprimate.

## Referințe ##

* [Specificații format BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

