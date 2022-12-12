{
  "date" : "2019-10-11",
  "keywords" :[ "wmz fájl", "wmz fájl formátum", "mi az a wmz fájl", "fájl", "wmz példa", "wmz fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMZ fájlformátum – tömörített Windows metafájl",
  "description":"További információ a WMZ fájlformátumról és az API-król, amelyek WMZ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "WMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Mi az a WMZ fájl?

A .wmz kiterjesztésű fájl a [WMF](/hu/image/wmf/) tömörített változata, és metafájlok tárolására szolgál. Ez egy közepes szintű fájl, amelyet a Microsoft Office alkalmazások régebbi verziói generálnak, és nem túl népszerű. A WMZ-fájlok a dokumentumok [HTML](/hu/web/html/) formátumba mentésekor jönnek létre. Ezek a beágyazott clip art-okat, egyenleteket stb. tartalmazó dokumentumok e-mailben történő küldésekor is előállíthatók. A WMZ-fájlokat megnyitni képes alkalmazások közé tartozik (de nem kizárólagosan) a Corel Winzip és az Apple Archive Utility.

## WMZ fájlformátum

A WMZ-fájlok [Gzip](/hu/compression/gz/) tömörítettek, és tartalmazzák a [WMF](/hu/image/WMF/) fájlt. A Gzip a DEFLATE algoritmust használja az archívum tömörítésére. A GZIP eltér a [ZIP](/hu/compression/zip/) archívumformátumtól, mivel tömörítési algoritmust alkalmaz a teljes archívumra, nem pedig az egyes fájlokra. A fájlformátum a következőkből áll:

* Fájl fejléc
* Opcionális fejlécek
* Tömörített adatok
* Fájllábléc

Az Internet Engineering Task Force (IETF) által közzétett GZIP fájlformátum [specifikációs verzió 4.3] (http://tools.ietf.org/html/rfc1952) részletes információkat tartalmaz a fájlformátumról.

## Hivatkozások

* [RFC1952: GZIP fájlformátum specifikáció](http://tools.ietf.org/html/rfc1952), készítette: [IETF](https://ietf.org)
* [Windows MetaFile – Wikipédia](https://en.wikipedia.org/wiki/Windows_Metafile)

