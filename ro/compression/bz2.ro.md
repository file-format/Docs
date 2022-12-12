{
  "date" : "2019-10-11",
  "keywords" :[ "fișier bz2", "format fișier bz2", "ce este un fișier bz2", "fișier", "exemplu bz2", "extensie fișier bz2", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Format de fișier comprimat",
  "description":"Aflați să știți ce este un fișier BZ2 și API-urile care pot crea și deschide fișiere BZ2.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Ce este un fișier BZ2?

BZ2 sunt fișiere comprimate generate folosind metoda de compresie open source [BZIP2](http://www.bzip.org/), mai ales pe sisteme UNIX sau Linux. Este folosit pentru comprimarea unui singur fișier și nu este destinat arhivării mai multor fișiere. Acest lucru este în contrast cu formatul de fișier TAR de pe aceleași platforme care arhivează mai multe fișiere într-un singur fișier, dar fără compresie. Fișierele comprimate ca BZ2 pot fi decomprimate cu aplicații precum [WinZip](https://www.winzip.com/win/en/). BZIP2 utilizează algoritmul de compresie Run-Length Encoding (RLE) sau [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) pentru a atinge niveluri ridicate de compresie.

## Format de fișier BZ2

Nu există specificații formale disponibile pentru acest format de fișier. Cu toate acestea, o [specificații de inginerie inversă] neoficială (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) arată că un flux .bz2 constă dintr-un antet de 4 octeți care este urmat cu zero sau mai multe blocuri comprimate. Este urmat imediat de un marcator de sfârșit de flux care conține un CRC pe 32 de biți pentru întregul flux de text simplu procesat. Nu există nicio umplutură între blocurile comprimate și toate blocurile sunt aliniate la biți.

## Dezarhivați/Extrageți fișierul BZ2

Puteți dezarhiva un fișier BZ2 pe Windows și Mac OS folosind software precum WinZip. Pe Linux, următoarea comandă în terminal.

```
bzip2 -d filename.bz2
```

## Referințe

* [Specificații format BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

