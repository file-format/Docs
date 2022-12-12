{
  "date" : "2022-01-23",
  "keywords" :[ "fișier xz", "format fișier", "ce este un fișier xz", "fișier", "exemplu xz", "extensie fișier xz", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier XZ - Arhivă comprimată XZ",
  "description":"Aflați despre formatul de fișier XZ și despre API-urile care pot crea și deschide fișiere XZ.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Ce este un fișier XZ?

XZ este un format de fișier comprimat care utilizează algoritmul de compresie LZMA2. A fost conceput ca un înlocuitor pentru formatele populare gzip și bzip2 și oferă o serie de avantaje față de aceste standarde mai vechi. Fișierele XZ sunt bine acceptate pe multe platforme și pot fi decomprimate rapid și ușor. Deși nu sunt la fel de comune ca fișierele [ZIP](/ro/compression/zip/) sau [RAR](/ro/compression/rar/), arhivele XZ pot fi folosite pentru a stoca cantități mari de date fără a sacrifica calitatea compresiei. Dacă trebuie să comprimați sau să decomprimați fișiere mari, extensia de fișier XZ merită luată în considerare.

## Format de fișier XZ

Fișierele XZ sunt generate și salvate ca fișiere binare pe disc. Utilizează algoritmul LZMA pentru a comprima datele și poate atinge un raport de compresie de până la 50%. Fișierele XZ sunt utilizate de obicei pentru distribuțiile de software și arhivele de rezervă. Ele pot fi decomprimate folosind utilitarul XZ, care este inclus în majoritatea distribuțiilor Linux.

## Dezarhivați fișierele XZ pe Linux/Unix

Pentru a dezarhiva fișierele XZ, instalați mai întâi pachetul `xz-utils`:
```
$ sudo apt-get install xz-utils
```

Utilizați comanda `unxz` pentru a extrage fișierele .xz:
```
$ unxz compressed_xz_file.xz
```

sau folosind opțiunea --decompress a XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Referințe

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)

