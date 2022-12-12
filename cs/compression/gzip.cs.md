{
  "date" : "2022-06-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru GZIP - archivní soubor GNU ZIP",
  "description":"Zjistěte, co je soubor GZIP a rozhraní API, která mohou vytvářet a otevírat soubory GZIP.",
  "linktitle" : "GZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-26"
}

## Co je soubor GZIP?

Soubor GZIP je komprimovaný archiv, který je vytvořen pomocí standardního kompresního algoritmu [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Komprimovaný archiv může obsahovat více souborů včetně komprimovaných souborů, adresářů a útržků souborů. Většina unixových systémů obsahuje open source gzip (GNU Zip) kompresorový nástroj pro kompresi/dekompresi souborů. Soubory GZIP lze otevřít pomocí aplikací, jako je [WinZip] (https://www.winzip.com/en/).

## Formát souboru GZIP – Další informace

GZIP používá ke kompresi souborů do archivů algoritmus [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE). Dvě RFC, [RFC1952](https://tools.ietf.org/html/rfc1952) a [RFC 1951](https://tools.ietf.org/html/rfc1951), definují specifikace formátu gzip wrapper a deflovat komprimovaný datový formát, resp.

Soubory GZIP se často ukládají ve formátu souboru [GZ](/cs/compression/gz/).

## Reference

* [gzip](http://www.gzip.org/)
* [gzip – Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: Specifikace formátu souboru GZIP] (http://tools.ietf.org/html/rfc1952), od IETF
* [RFC 1951](https://tools.ietf.org/html/rfc1951)

