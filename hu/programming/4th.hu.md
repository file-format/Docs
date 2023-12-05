
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"4. fájl – negyedik nyelvi fájlformátum",
  "description":"Tudjon meg többet arról, hogy mi a .4. fájlformátum, példákkal és API-kkal, amelyek 4. fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Mi az a 4. fájl?

A .4 kiterjesztésű fájl a **Forth programozási nyelvhez** létrehozott programfájl. Forth programozási nyelven írt programok forráskódját tartalmazza, és a program végrehajtásakor generálja a kimenetet. Ez csak egy másik programnyelvi fájl, amely hasonló a [C](/hu/programming/c/) és a [C++](/hu/programing/cpp/) forrásfájlhoz.

## 4. fájlformátum – További információ


### 4. programozási nyelv kód példa

Íme egy példa egy Forth nyelven írt egyszerű programra, amely kiszámolja egy adott szám faktoriálisát:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

Ebben a példában a faktoriális szó egyetlen n argumentumot vesz fel, és annak faktoriálisát adja vissza. A dup szó megkettőzi a verem tetején lévő értéket, a drop eldobja a verem tetején lévő értéket, és a * megszorozza a verem tetején lévő két értéket. Az if és a start/amíg konstrukciók szabályozzák a program menetét.

A program használatához írja be a definíciót a Forth értelmezőbe, majd hívja meg a faktoriális szót azzal a számmal, amelyiknek a faktoriálisát meg szeretné keresni:

```
10 factorial .
```
Ez a 3628800 kimenetet eredményezné, ami a 10 faktoriálisa.

## Hivatkozások

* [Forth programozási nyelv](https://en.wikipedia.org/wiki/Forth_(programming_language))

