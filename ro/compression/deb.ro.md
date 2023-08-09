{
  "date" : "2021-04-08",
  "keywords" :[ "fișier deb", "format fișier deb", "ce este un fișier deb", "fișier", "exemplu deb", "extensie fișier deb", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Arhiva de gudron comprimată Bzip",
  "description":"Aflați despre formatul fișierului DEB și despre API-urile care pot crea și deschide fișiere DEB.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Ce este un fișier DEB?

Un fișier cu extensia .deb este un format de fișier de pachet binar Debian disponibil pentru distribuirea pachetelor software pe sistemul de operare Linux. Este format din două fișiere de arhivă [TAR](/ro/compression/tar/). DPKG oferă mecanismul de citire și instalare a pachetelor DEB. Pachetele DEB pot fi instalate folosind interfața de gestionare a software-ului pachetului APT. Fișierele DEB au Internet Media Type ca „application/vnd.debian.binary-package”.

## Format de fișier DEB

Un fișier DEB este format din două fișiere de arhivă [TAR](/ro/compression/tar/). O arhivă deține informațiile de control, iar alta conține datele instalabile.

### Organizarea pachetelor

Fișierul DEB este un fișier de arhivă **ar** care are o valoare magică de `!<arch> `. Începând cu Debian 0.93, mecanismul de arhivare a fișierelor DEB conține trei fișiere într-o anumită ordine.

1. `Debian Binary` - Este destinat să aibă o serie de linii, separate prin linii noi. În prezent, este prezentă doar o singură linie care descrie numărul versiunii. Numărul actual al versiunii este 2.0.
1. `Arhiva de control` - Conține o arhivă control.tar care are scripturi de întreținere și meta-informații despre pachet, cum ar fi numele pachetului, versiunea, dependențele și întreținătorul.
1. `Arhiva de date` - Este o arhivă tar numită data.tar și conține fișierele media instalabile efectiv. Arhiva poate fi comprimată cu gz, bz2, lzma sau xz, iar extensia de fișier a arhivei de date se modifică în consecință.

### Arhiva de control

Arhiva de control poate include conținut după cum urmează.

* `control` - Conține o scurtă descriere a pachetului, precum și alte informații, cum ar fi dependențele acestuia.
* `md5sums` - Conține sume de control MD5 ale tuturor fișierelor din pachet pentru a detecta fișierele corupte sau incomplete.
* `conffiles` - Listează fișierele pachetului care ar trebui tratate ca fișiere de configurare. Fișierele de configurare nu sunt suprascrise în timpul unei actualizări decât dacă este specificat.
* `preinst`, postinst, prerm și postrm - scripturi opționale care sunt executate înainte sau după instalarea sau eliminarea pachetului
* `config` este un script opțional care acceptă mecanismul de configurare debconf.
* `shlibs` - Este o listă de dependențe de bibliotecă partajată.

## Referințe

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Format pachet binar Debian](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

