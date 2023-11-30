
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fjärde filen - Forth Language File Format",
  "description":"Läs mer om vad .4th filformat är med exempel och API:er som kan skapa och öppna 4th filer.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Vad är en fjärde fil?

En fil med filändelsen .4th är en programmeringsfil skapad för **Forth Programming Language**. Den innehåller källkod för program skrivna i Forth programmeringsspråk och genererar utdata när programmet körs. Det är bara en annan programmeringsspråksfil som liknar källfilen [C](/sv/programming/c/) och [C++](/sv/programming/cpp/).

## Fjärde filformatet - Mer information


### Exempel på 4:e programmeringsspråkskoden

Här är ett exempel på ett enkelt program skrivet i Forth som beräknar fakulteten för ett givet tal:

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

I det här exemplet tar faktorordet ett enda argument n och returnerar dess faktor. Dup-ordet duplicerar värdet på toppen av stacken, drop kasserar värdet på toppen av stacken och * multiplicerar de två värdena ovanpå stacken. Konstruktionerna om och börja/tills styr programmets flöde.

För att använda det här programmet skulle du ange definitionen i Forth-tolken och sedan anropa faktorordet med numret du vill hitta faktorvärdet för:

```
10 factorial .
```
Detta skulle resultera i utgången 3628800, vilket är faktorn 10.

## Referenser

* [Forth Programming Language](https://en.wikipedia.org/wiki/Forth_(programming_language))

