
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "4. fails — ceturtās valodas faila formāts",
  "description":"Uzziniet par 4. faila formātu, izmantojot piemēru un API, kas var izveidot un atvērt 4. failus.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th-lv",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Kas ir ceturtais fails?

Fails ar .4 paplašinājumu ir programmēšanas fails, kas izveidots **Forth Programming Language**. Tas satur avota kodu programmām, kas rakstītas Forth programmēšanas valodā, un ģenerē izvadi, kad programma tiek izpildīta. Tas ir tikai vēl viens programmēšanas valodas fails, kas līdzīgs [C](/programming/c/) un [C++](/programming/cpp/) avota failam.

## 4. faila formāts — vairāk informācijas


### 4. programmēšanas valodas koda piemērs

Šeit ir piemērs vienkāršai programmai, kas rakstīta Forth un kas aprēķina noteiktā skaitļa faktoriālu:

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

In this example, the factorial word takes a single argument n and returns its factorial. The dup word duplicates the value on top of the stack, drop discards the value on top of the stack, and * reizina divas vērtības, kas atrodas kaudzes augšpusē. Ja un sākuma/līdz konstrukcijas kontrolē programmas plūsmu.

Lai izmantotu šo programmu, jums ir jāievada definīcija Forth tulkā un pēc tam jāizsauc faktoriālais vārds ar numuru, kuram vēlaties atrast faktoriālu:

```
10 factorial .
```
Tā rezultātā tiktu iegūta izvade 3628800, kas ir koeficients 10.

## Atsauces

 * [Forth programmēšanas valoda](https://en.wikipedia.org/wiki/Forth_(programming_language))

