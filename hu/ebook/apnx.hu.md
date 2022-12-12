{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Amazon oldalszám index", "kiterjesztés", "fájl", "formátum", "eBook", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az Amazon APNX fájlformátumról és az API-król, amelyek APNX fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"APNX – Amazon oldalszám index",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Mi az APNX fájl? ##

Az Amazon oldalszámindex fájl, amely az .apnx kiterjesztést használja, egy eBook fájltípus; az Amazon Kindle használja. Ezeket a fájlokat valójában lapozási fájlokként ismerik, amelyeket a Kindle eszközök használnak. Tehát az APNX-fájlokat általában a Kindle e-könyvek oldalainak megjelölésére hozzák létre. Az oldalszámozási funkciót az Amazon Kindle eszközökön a 3.1-es firmware óta elindították. Belenéz az APNX fájlba az oldalindexekért, majd leképezi az eredeti nyomtatott könyv oldalszámaival. Ezeket a fájlokat a Kindle eszközökre menti az Amazon eBooks fájljaival együtt. Az APNX-fájlokat nem lehet megnyitni vagy szerkeszteni.

## APNX fájlformátum specifikációi ##

### Elrendezés

|byte| tartalom| megjegyzések|
---|---|---|
|4 |00010001 | Formátumazonosító. 65537 kis-endián értéke.|
|4 |következő kezdete | Az eltolás az első fejléc véghelye után. Elindítja a fejléc info| új sorozatát
|4 |hossza| Az első fejléc hossza|
|N |első fejléc | Tartalomfejlécet tartalmazó karakterlánc. Elindítja a következő sorozatot|
|2 |ismeretlen | Mindig 1|
|2 |hossz | Második fejléc hossza|
|2 |oldalszám | Az oldalakat képviselő második fejléc utáni bájtok teljes száma. Ez az összeg tartalmazza azokat a bájtokat, amelyeket a pageMap figyelmen kívül hagy.|
|2 |ismeretlen | Mindig 32|
|N |második fejléc | Az oldalleképezés fejlécét tartalmazó karakterlánc|
|4*N |párna | Az oldalleképezés fejlécében megadott első szám a 0 bájt számát jelzi.|
|4*N |oldallista ||

### Tartalomfejléc

A tartalomfejléc egy {}-ba zárt karakterláncból áll, amely kulcs-érték párokat tartalmaz:

|tartalom| megjegyzések|
---|---|
|contentGuid| Útmutató.|
|asin | Amazon-azonosító a könyv Kindle verziójához.|
|cdeType | MOBI cdeType. Az e-könyveknél mindig EBOK-nak kell lennie.|
|fileRevisionId | A fájl átdolgozása.|

#### Példa
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Oldalleképezés fejléce
Az oldalleképezés fejléce egy {}-ba zárt karakterláncból áll, amely kulcs-érték párokat tartalmaz.

|tartalom | megjegyzések|
---|---|
|asin | Az ISBN 10 annak a papírkönyvnek, amelynek oldalai megfelelnek|
|oldaltérkép| Három értékű sor. Így néz ki: "(N,N,N)\
1) Az oldalszámozási sorozatot elindító fejléc utáni bájtok száma\
2) ismeretlen\
3) ismeretlen\|
#### Példa
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Oldallista

Az oldallista eltolások sorozata a nyers HTML-ben. Minden egyes
érték egy új oldal eleje. Minden bejegyzés egy 4 bájtos big endian
int.



## Hivatkozások

* [Amazon APNX fájlformátum](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX – MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

