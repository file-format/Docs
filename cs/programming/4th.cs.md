
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"4th File - Forth Language File Format",
  "description":"Zjistěte, co je formát souboru .4th s příklady a rozhraními API, která mohou vytvářet a otevírat soubory 4.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Co je 4. soubor?

Soubor s příponou .4th je programovací soubor vytvořený pro **Forth Programming Language**. Obsahuje zdrojový kód pro programy napsané v programovacím jazyce Forth a generuje výstup při spuštění programu. Je to jen další soubor programovacího jazyka podobný zdrojovému souboru [C](/cs/programming/c/) a [C++](/cs/programming/cpp/).

## 4. formát souboru – další informace


### Příklad kódu 4. programovacího jazyka

Zde je příklad jednoduchého programu napsaného ve Forth, který vypočítá faktoriál daného čísla:

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

V tomto příkladu slovo faktoriál přebírá jeden argument n a vrací svůj faktoriál. Slovo dup duplikuje hodnotu na vrcholu zásobníku, drop zahodí hodnotu na vrcholu zásobníku a * vynásobí dvě hodnoty na vrcholu zásobníku. Konstrukce if a begin/until řídí tok programu.

Chcete-li použít tento program, zadejte definici do Forth interpretu a potom zavolejte faktoriál slovo s číslem, jehož faktoriál chcete najít:

```
10 factorial .
```
Výsledkem by byl výstup 3628800, což je faktoriál 10.

## Reference

* [Čtvrtý programovací jazyk](https://en.wikipedia.org/wiki/Forth_(programming_language))

