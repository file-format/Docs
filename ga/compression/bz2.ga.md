{
  "date": "2019-10-11",
  "keywords": [
"comhad bz2",
"Formáid comhaid bz2",
"Cad is comhad bz2 ann",
"comhad",
"sampla bz2",
"Íosluchtaigh síneadh comhad bz2",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BZ2 - Formáid Chomhaid Chomhbhrúite",
  "description": "Faigh amach cad is comhad BZ2 ann agus APIanna ar féidir comhaid BZ2 a chruthú agus a oscailt.",
  "linktitle": "BZ2",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-bz-ga2"
}
},
  "lastmod": "2020-09-05"
}

## Cad is comhad BZ2 ann?

Is comhaid comhbhrúite iad BZ2 a ghintear trí úsáid a bhaint as an modh comhbhrú foinse oscailte [BZIP2](http://www.bzip.org/), ar chóras UNIX nó Linux den chuid is mó. Úsáidtear é chun comhad amháin a chomhbhrú agus níl sé i gceist chun ilchomhaid a chartlannú. Tá sé seo i gcodarsnacht le formáid comhaid TAR ar na hardáin chéanna a dhéanann ilchomhaid a chartlannú i gcomhad amháin ach gan comhbhrú. Is féidir comhaid atá comhbhrúite mar BZ2 a dhí-chomhbhrú le feidhmchláir ar nós [WinZip](https://www.winzip.com/win/en/). Úsáideann BZIP2 Ionchódú Fad Rith (RLE) nó algartam comhbhrú [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) chun ardleibhéil comhbhrú a bhaint amach.

## Formáid Comhaid BZ2

Níl aon sonraíochtaí foirmiúla ar fáil don fhormáid comhaid seo. Mar sin féin, léiríonn [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) neamhoifigiúil go bhfuil ceanntásc 4-beart i sruth .bz2 a bhfuil nialas nó níos mó bloic chomhbhrúite ina dhiaidh sin. Ina dhiaidh sin láithreach tá marcóir deireadh an tsrutha ina bhfuil CRC 32-giotán don ghnáthsruth iomlán a phróiseáiltear. Níl aon stuáil idir na bloic chomhbhrúite agus tá na bloic go léir ailínithe.

## Dízip/Sliocht Comhad BZ2

Is féidir leat comhad BZ2 a unzip ar Windows agus Mac OS ag baint úsáide as bogearraí ar nós WinZip. Ar linux, an t-ordú seo a leanas sa chríochfort.

```
bzip2 -d filename.bz2
```

## Tagairtí

* [Sonraíochtaí Formáid BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


