{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c","co je soubor ac","jak otevřít soubor c", "přípona", "soubor", "soubor c", "formát souboru c", "přípona souboru c"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Programovací soubor jazyka C - C",
  "description":"Další informace o formátu souboru C a rozhraních API, která mohou vytvářet a otevírat soubory C.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Co je soubor C?

Soubor uložený s příponou c je soubor zdrojového kódu napsaný v programovacím jazyce C. Soubor **C** obsahuje veškerou implementaci funkčnosti aplikace ve formě zdrojového kódu. Deklarace zdrojového kódu se zapisuje do hlavičkových souborů, které jsou uloženy s příponou [.h](/cs/programming/h/). C++ je moderní forma jazyka C a dnes se používá k vývoji většiny softwaru.

## Stručná historie

Jazyk C vznikl jako výsledek vytváření různých utilit pro operační systém UNIX. Denis Ritchie, muž stojící za vytvořením tohoto programovacího jazyka, práce původně začala v 60. a na začátku 70. let.

## Formát souboru C

Soubory C jsou psány ve formátu prostého textu podle syntaxe programovacího jazyka. Typický soubor C bude mít:

* příkaz import v horní části souboru pro import libovolné hlavičky Files
* jedna nebo více metod implementace požadované funkce

### Import záhlaví

Hlavičkové soubory s příponou .h obsahují nezbytné příkazy include pro zahrnutí dalších funkčních souborů do projektu. Kromě toho obsahují deklarace metod definovaných v implementačním souboru. Soubory záhlaví jsou zahrnuty pomocí příkazu include, jak je uvedeno níže.

```
#include <filename.h>
```

### Implementace zdrojového kódu

Vlastní implementace funkčních požadavků je kódována jako metody v souboru C. Každá metoda v souboru C má návratový typ, název metody a může mít nějaké vstupní parametry. Pokud návratový typ není neplatný, metoda může vracet nějakou hodnotu.

### Příklad kódu C
Zde je ukázkový program ac:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Reference** ##

* [Implementace třídy – podle Wikipedie](https://en.wikipedia.org/wiki/Class_implementation_file)

