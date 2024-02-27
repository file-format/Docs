{
  "date": "2022-06-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GZIP-filformat - GNU Zipped Archive File",
  "description": "Lær om, hvad en GZIP-fil og API'er er, der kan oprette og åbne GZIP-filer.",
  "linktitle": "GZIP",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-gzi-dap"
}
},
  "lastmod": "2022-06-26"
}

## Hvad er en GZIP fil?

En GZIP-fil er et komprimeret arkiv, der er oprettet med standardkompressionsalgoritmen [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Det komprimerede arkiv kan indeholde flere filer inklusive komprimerede filer, mapper og filstubber. De fleste af Unix-systemerne inkluderer open source gzip (GNU Zip) komprimeringsværktøjet til komprimering/dekomprimering af filer. GZIP-filer kan åbnes med programmer såsom [WinZip](https://www.winzip.com/en/).

## GZIP-filformat - flere oplysninger

GZIP bruger [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE)-algoritmen til at komprimere filer til arkiver. To RFC'er, [RFC1952](https://tools.ietf.org/html/rfc1952) og [RFC 1951](https://tools.ietf.org/html/rfc1951), definerer specifikationerne for henholdsvis gzip-indpakningsformatet og deflatere komprimeret dataformat.

GZIP-filer gemmes ofte som [GZ](/compression/gz/) filformat.

## Referencer

* [gzip](http://www.gzip.org/)

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

* [RFC1952: GZIP-filformatspecifikation](https://datatracker.ietf.org/doc/html/rfc1952), af IETF

* [RFC 1951](https://tools.ietf.org/html/rfc1951)


