{
  "date": "2019-10-11",
  "keywords": [
"bz2 fails",
"bz2 faila formātā",
"kas ir bz2 fails",
"failu",
"bz2 piemērs",
"bz2 faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BZ2 - saspiesta faila formāts",
  "description": "Uzziniet, kas ir BZ2 fails un API, kas var izveidot un atvērt BZ2 failus.",
  "linktitle": "BZ2",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-bz-lv2"
}
},
  "lastmod": "2020-09-05"
}

## Kas ir BZ2 fails?

BZ2 ir saspiesti faili, kas ģenerēti, izmantojot [BZIP2](http://www.bzip.org/) atvērtā pirmkoda saspiešanas metodi, galvenokārt UNIX vai Linux sistēmā. To izmanto viena faila saspiešanai un nav paredzēts vairāku failu arhivēšanai. Tas ir pretstatā TAR faila formātam tajās pašās platformās, kas arhivē vairākus failus vienā failā, bet bez saspiešanas. Failus, kas saspiesti kā BZ2, var atspiest ar tādām lietojumprogrammām kā [WinZip](https://www.winzip.com/win/en/). BZIP2 izmanto Run-Length Encoding (RLE) vai [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) saspiešanas algoritmu, lai sasniegtu augstu saspiešanas līmeni.

## BZ2 faila formāts

Šim faila formātam nav pieejamas oficiālas specifikācijas. Tomēr neoficiāls [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) liecina, ka .bz2 straume sastāv no 4 baitu galvenes, kurai seko nulle vai vairāk saspiestu bloku. Tūlīt tam seko straumes beigu marķieris, kas satur 32 bitu CRC visai apstrādātajai vienkārša teksta straumei. Starp saspiestajiem blokiem nav polsterējuma, un visi bloki ir izlīdzināti.

## Izpakojiet/izņemiet BZ2 failu

Varat izpakot BZ2 failu operētājsistēmās Windows un Mac OS, izmantojot programmatūru, piemēram, WinZip. Operētājsistēmā Linux terminālā šāda komanda.

```
bzip2 -d filename.bz2
```

## Atsauces

* [BZIP2 formāta specifikācijas](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


