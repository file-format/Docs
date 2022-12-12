{
  "date" : "2021-04-08",
  "keywords" :[ "fișier rpm", "format fișier rpm", "ce este un fișier rpm", "fișier", "exemplu rpm", "extensie fișier rpm", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM – fișierul manager de pachete Red Hat",
  "description":"Aflați despre formatul de fișier RPM și despre API-urile care pot crea și deschide fișiere RPM.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Ce este un fișier RPM?

Un fișier cu extensia .rpm este un pachet de sistem de operare Red Hat Linux pentru instalări de programe pe sisteme Linux. Red Hat Package Manager folosește formatul de fișier RPM și este un sistem de gestionare a pachetelor gratuit și open-source. Deși fișierele RPM pot fi folosite așa cum sunt pentru instalarea programelor, acestea pot fi convertite în alte formate de pachete, cum ar fi [DEB](/ro/compression/deb/) folosind programul Debian numit Alien.

## Format de fișier RPM

Un fișier RPM este un binar care poate conține un set de fișiere. De cele mai multe ori, fișierele RPM sunt „RPM-uri binare”, care sunt executabilele compilate ale software-ului. Fișierul RPM poate conține RPM sursă (SRPM) care pot fi folosite pentru a construi pachetul din codul sursă. Formatul de fișier RPM este format din patru secțiuni.

* Lead - Identifică fișierul ca fișier RPM
* Semnătura - Poate fi folosită pentru a asigura integritatea și/sau autenticitatea
* Antet - Conține metadate, inclusiv numele pachetului, versiunea, arhitectura, lista de fișiere etc.
* Arhivă de fișiere - Cunoscută și ca sarcină utilă, care este de obicei în format cpio, comprimată cu [GZIP](/ro/compression/gz/)

## Referințe

* [RPM - Wikipedia](https://rpm.org)
* [Documentația RPM](https://rpm.org/documentation.html)

