
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "4-asis failas – ketvirtosios kalbos failo formatas",
  "description":"Sužinokite, kas yra .4 failo formatas, naudodamiesi pavyzdžiu ir API, kuriomis galima kurti ir atidaryti 4-uosius failus.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th-lt",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Kas yra 4-asis failas?

Failas su .4 plėtiniu yra programavimo failas, sukurtas **Forth Programming Language**. Jame yra programų, parašytų Forth programavimo kalba, šaltinio kodas ir generuojamas išėjimas, kai programa vykdoma. Tai tik dar vienas programavimo kalbos failas, panašus į [C](/programming/c/) ir [C++](/programming/cpp/) šaltinio failą.

## 4-asis failo formatas – daugiau informacijos


### 4-osios programavimo kalbos kodo pavyzdys

Štai paprastos programos, parašytos Forth, pavyzdys, apskaičiuojantis tam tikro skaičiaus faktorialą:

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

In this example, the factorial word takes a single argument n and returns its factorial. The dup word duplicates the value on top of the stack, drop discards the value on top of the stack, and * padaugina dvi vertes, esančias krūvos viršuje. Konstrukcijos if ir start/iki valdo programos eigą.

Norėdami naudoti šią programą, įveskite apibrėžimą į Forth interpretatorių ir iškvieskite faktorialinį žodį su numeriu, kurį norite rasti faktorialą:

```
10 factorial .
```
Taip būtų gauta išvestis 3628800, kuri yra 10 koeficientas.

## Nuorodos

 * [Forth programavimo kalba](https://en.wikipedia.org/wiki/Forth_(programming_language))

