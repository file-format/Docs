{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier TGZ - Fișier Gzipped Tar",
  "description":"Aflați despre formatul de fișier TGZ și despre API-urile care pot crea și deschide fișiere TGZ.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## Ce este un fișier TGZ?

Un fișier cu extensia .tgz este un fișier de arhivă TAR, care cuprinde mai multe fișiere și foldere, care a fost comprimat folosind software-ul de compresie Gnu Zip (gzip). Un fișier [TAR](/ro/compression/tar/) combină de obicei mai multe fișiere într-un singur fișier pentru backup sau distribuire pe internet. Este un fișier de decomprimare până când este comprimat folosind software-ul gzip, după care devine fișierul TGZ. Fișierele TGZ, fiind fișiere comprimate, ocupă mai puțin spațiu pe disc și sunt ușor de transferat folosind internetul prin e-mail. Unele aplicații care pot deschide fișiere TGZ includ WinZip, Apple Archive Utility, 7-Zip și WinRAR. Fișierele TGZ sunt utilizate mai ales în sistemele UNIX și Linux.

## Format de fișier TGZ

Fișierele TGZ sunt salvate ca fișiere binare comprimate folosind algoritmul de compresie [GZ](/ro/compression/gz/).

## Cum să despachetezi fișierul .tgz pe Linux

Pe sistemul de operare Linux/Unix, următoarea comandă poate fi utilizată pentru a despacheta fișierele TGZ din linia de comandă.

```
tar zxvf tgzCompressedFile.tgz
```

Comanda de mai sus decomprimă fișierul TGZ comprimat și extrage fișierele acestuia din arhiva TAR pe disc.
## Referințe ##

* [TGS](https://core.telegram.org/animated_stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

