{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "extensie", "fișier", "format", "Cărți de benzi desenate", "Format fișier de benzi desenate", "Carte electronică"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier CBC și despre API-urile care pot crea și deschide fișiere CBC.",
  "title" :"CBC - Format de fișier al colecției de benzi desenate",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Ce este un fișier CBC?

Un fișier cu extensia .cbc este o colecție comprimată de fișiere cu benzi desenate pentru cărți electronice și conține fișiere [CBZ](/ro/ebook/cbz/) și [CBR](/ro/ebook/cbr/). Este folosit de [Calibre](https://calibre-ebook.com/), o aplicație de conversie a cărților electronice, care este un manager de cărți electronice open source multiplatformă și vă permite să vă gestionați cărțile electronice și să le convertiți în diferite formate . Un fișier CBC conține un fișier .txt, comics.txt, care listează alte fișiere care fac parte din arhivă. Sunt disponibile online mai multe aplicații care pot converti fișierele CBC în [AZW3](/ro/ebook/azw3/), [EPUB](/ro/ebook/epub/), [FB2](/ro/ebook/fb2/), [MOBI](/ro/ebook/mobi/), [TXT](/ro/word-processing/txt/), [PDF](/ro/pdf/) și alte formate de fișiere populare.

## Format de fișier CBC

Fișierele CBC sunt arhive comprimate care conțin CBZ, CBR și un fișier text pentru listarea conținutului. Fișierul text, comics.txt este codificat UTF8 și conține o listă a fișierelor CBC care vor fi folosite de cititori pentru organizarea colecțiilor lor. Un fișier CBC are de obicei mai multe atribute care permit organizarea acestei colecții, cum ar fi Comic, Categorie, Publisher, Series, Edition și Artist.

Conținutul unui exemplu de fișier CBC este listat după cum urmează:

* comics.txt - Fișier text care conține o listă de fișiere CBR și CBZ
* 1.cbz
* 2.cbz
* 3.cbz
* Fișier(e) CBZ

unde fișierul comics.txt listează conținutul după cum urmează:

* 1.cbz: primul capitol
* 2.cbz: al doilea capitol
* 3.cbz: al treilea capitol

Cititorii procesează fișierul comics.txt și generează cuprinsul pe baza datelor furnizate.

## Referințe

* [Calibre](https://calibre-ebook.com/)

