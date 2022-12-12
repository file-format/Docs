{
  "date" : "2022-06-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier GZIP - fișier arhivă GNU Zipped",
  "description":"Aflați despre ce este un fișier GZIP și API-urile care pot crea și deschide fișiere GZIP.",
  "linktitle" : "GZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-26"
}

## Ce este un fișier GZIP?

Un fișier GZIP este o arhivă comprimată care este creată cu algoritmul de compresie standard [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Arhiva comprimată poate conține mai multe fișiere, inclusiv fișiere comprimate, directoare și stub-uri de fișiere. Majoritatea sistemelor Unix includ utilitarul de compresor open source gzip (GNU Zip) pentru compresia/decomprimarea fișierelor. Fișierele GZIP pot fi deschise cu aplicații precum [WinZip](https://www.winzip.com/en/).

## Format de fișier GZIP - Mai multe informații

GZIP folosește algoritmul [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) pentru a comprima fișierele în arhive. Două RFC, [RFC1952](https://tools.ietf.org/html/rfc1952) și [RFC 1951](https://tools.ietf.org/html/rfc1951), definesc specificațiile formatului de wrapper gzip și, respectiv, dezumflați formatul de date comprimate.

Fișierele GZIP sunt adesea salvate ca format de fișier [GZ](/ro/compression/gz/).

## Referințe

* [gzip](http://www.gzip.org/)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: specificația formatului fișierului GZIP](http://tools.ietf.org/html/rfc1952), de la IETF
* [RFC 1951](https://tools.ietf.org/html/rfc1951)

