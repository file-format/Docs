{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "extensie", "fișier", "format", "eBook", "Format fișier Kindle", "Structură fișier AZW3"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier AZW3 și despre API-urile care pot crea și deschide fișiere AZW3.",
  "title" :"Ce este un fișier AZW3?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Ce este un fișier AZW3?

AZW3, cunoscut și ca Kindle Format 8 (**KF8**), este versiunea modificată a formatului de fișier digital pentru cărți electronice [AZW](/ro/ebook/azw/) dezvoltat pentru dispozitivele Amazon Kindle. Formatul este o îmbunătățire a fișierelor AZW mai vechi și este utilizat pe dispozitivele Kindle Fire numai cu compatibilitate cu versiunea anterioară pentru formatul de fișier strămoș, adică [MOBI](/ro/ebook/mobi/) și AZW. Amazon a introdus formatul KFX (KF versiunea 10) după KF8, care este utilizat pe cele mai recente dispozitive Kindle. Fișierele AZW3 au tip media internet application/vnd.amazon.mobi8-ebook. Fișierele AZW3 pot fi convertite într-un număr de alte formate de fișiere, cum ar fi [PDF](/ro/pdf/), [EPUB](/ro/ebook/epub/), [AZW](/ro/ebook/azw/), [DOCX](/ro/ word-processing/docx/) și [RTF](/ro/word-processing/rtf/).

## Format de fișier AZ3/KF8 ##

Fișierele KF8 sunt de natură binară și păstrează structura unui format de fișier MOBI ca fișier PDB. După cum am menționat mai devreme, un fișier KF8 poate consta atât dintr-un MOBI, cât și dintr-o versiune KF8 mai nouă a EPUB mai târziu. Detaliile interne ale formatului au fost decodificate de [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack), care este un script Python care analizează baza de date compilată finală și extrage fișierele sursă MOBI sau AZW din aceasta. Fișierele AZW3 (KF8) vizează versiunea EPUB3 cu compatibilitate inversă și pentru EPUB. KF8 compilează fișierele EPUB și generează o structură binară bazată pe formatul de fișier PDB.

## Referințe ##

* [KF8 - După Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)

