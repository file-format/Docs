{
  "date" : "2019-10-11",
  "keywords" :[ "emz fájl", "emz fájl formátum", "mi az emz fájl", "fájl", "emz példa", "emz fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMZ fájlformátum - Windows tömörített továbbfejlesztett metafájl",
  "description":"További információ az EMZ fájlformátumról és az API-król, amelyek EMZ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-10-24"
}

## Mi az EMZ fájl?

Az .emz kiterjesztésű fájl az Enhanced Metafile ([EMF](/hu/image/emf/) fájl) tömörített tárolója. Ezeket a [GZIP](/hu/compression/gz/) tömörítési technikával tömörítik, amely a UNIX és LINUX operációs rendszereken általánosan használt tömörítési módszer. A ZIP leválasztása (/hu/compression/zip/), a GZIP az archívumot egészben tömöríti az egyes fájlok tömörítése helyett. Az EMZ fájlok kisebb méretűek az EMF fájlokhoz képest, és elősegítik a gyors átvitelt az online fájlmegosztás során. Az EMZ fájlokat megnyitni képes alkalmazások közé tartozik a Microsoft Visio 2019, a Microsoft Office 2019, az XnView MP és a File Viewer Plus.

## EMZ fájlformátum

Az EMZ fájlok [Gzip](/hu/compression/gz/) tömörítettek, és [EMF](/hu/image/emf/) fájlt tartalmaznak. A Gzip a DEFLATE algoritmust használja az archívum tömörítésére, és másként alkalmazza a tömörítést. Egy EMZ fájl kicsomagolható GZip tömörítő segédprogramok, például a GNU Zip segítségével. A fájlformátum a következőkből áll:

* Fájl fejléc
* Opcionális fejlécek
* Tömörített adatok
* Fájllábléc

Az Internet Engineering Task Force (IETF) által közzétett GZIP fájlformátum [specifikációs verzió 4.3](https://datatracker.ietf.org/doc/html/rfc1952) részletes információkat tartalmaz a fájlformátumról.

## Hivatkozások

* [RFC1952: GZIP fájlformátum specifikáció](https://datatracker.ietf.org/doc/html/rfc1952), készítette: [IETF](https://www.ietf.org/)
* [Windows MetaFile – Wikipédia](https://en.wikipedia.org/wiki/Windows_Metafile)

