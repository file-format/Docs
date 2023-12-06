{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPIO File - Unix CPIO Archive File Format",
  "description":"Aflați să știți ce este un fișier CPIO și API-urile care pot crea și deschide fișiere CPIO.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Ce este un fișier CPIO?

Un fișier CPIO este un fișier de arhivă creat în formatul Unix Copy In Copy Out (CPIO). Este similar cu formatul de fișier TAR, în afară de faptul că este necomprimat. Fișierele CPIO pot stoca fișiere dispozitiv, legături simbolice și atribute extinse ale fișierului.

## Format de fișier CPIO

O arhivă CPIO este creată ca fișier binar care nu poate fi citit de om. Stochează colecția de fișiere și directoare. Conținutul unei arhive CPIO este identificat cu informații despre metadate, cum ar fi numele fișierelor, permisiunile, proprietatea și marcajele de timp. Aceste informații despre metadate sunt stocate și în fișierul de arhivă pentru acces lateral de către sistem.

## Formatul arhivei CPIO

Un fișier CPIO cuprinde unul sau mai multe fișiere membre concatenate. Fiecare fișier din arhivă constă dintr-un antet urmat opțional de conținutul fișierului, așa cum este menționat în antet. Arhiva conține un alt antet la sfârșit, care este descris de un fișier gol numit TRAILER!!.

### Tipuri de arhive CPIO

Există două tipuri de arhive CPIO. Acestea diferă doar în stilul antetului.

* Arhive ASCII - Aceste arhive CPIO au un antet imprimabil care devine parte din arhiva CPIO dacă arhiva în sine constă din fișiere ASCII
* Arhive binare - Aceste arhive CPIO au anteturi binare.

## Lucrul cu Arhiva CPIO

### Cum se creează arhive CPIO?

Puteți crea un CPIO pe sisteme asemănătoare Unix folosind comanda **cpio**. Următoarea comandă va găsi toate fișierele și directoarele din directorul curent și subdirectoarele acestuia. Această ieșire este apoi direcționată către comanda cpio care va genera o nouă arhivă CPIO numită archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Cum se extrage fișiere din arhivele CPIO?

Următoarea comandă extrage fișierele dintr-o arhivă existentă.

```
cpio -id < archive_cpio.cpio
```
Acesta va citi fișierul archive.cpio de la intrarea standard și va extrage fișierele în directorul curent.


## Referințe

* [CPIO - De Wikipedia](https://en.wikipedia.org/wiki/Cpio)
* [Format de fișier CPIO](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

