{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh","co je soubor .hh","jak otevřít soubor .hh", "přípona", "soubor", "soubor .hh", "formát souboru .hh", " přípona souboru .hh",".HH File Example"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - Formát souboru záhlaví C++",
  "description":"Další informace o formátu souboru HH a rozhraních API, která mohou vytvořit a otevřít soubor HH.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Co je soubor HH?

Soubor s příponou .hh je hlavičkový soubor C++, který obsahuje deklaraci proměnných, konstant a funkcí. Tyto deklarace jsou používány odpovídajícími implementačními soubory C++, obvykle uloženými jako soubory [.cpp](/cs/programming/cpp/), které obsahují skutečnou implementaci uživatelské logiky. Na hlavičkové soubory .hh se v implementačních souborech CPP odkazuje pomocí direktivy `#include`. Do projektu C++ můžete přidat co nejvíce hlavičkových souborů, aby obsahovaly deklarace úrovně projektu.

## Formát souboru .HH

Soubor .hh je prostý textový soubor, který je vytvořen s ohledem na pravidla definice souboru záhlaví. Mezi nejběžnější informace deklarované v souboru .hh patří následující.

**`Proměnné`** – V případě objektově orientovaného programování (OOP) obsahuje soubor záhlaví třídy definice všech proměnných na úrovni třídy, které jsou přístupné napříč soubory zdrojového kódu implementace.
**`Deklarace metod`** - Všechny deklarace metod jsou zahrnuty v hlavičkových souborech .h, aby byly přístupné ve více souborech implementace.
**`Definice neinline funkcí`** - Soubory záhlaví mohou také obsahovat definice neinline metod.
**`Mapy zpráv`** - Soubor záhlaví může také obsahovat mapy zpráv v případě implementace zdrojového kódu MFC. V takovém případě jsou mapy zpráv propojeny s implementací funkčnosti, která je propojena s prvky uživatelského rozhraní, jako je tlačítko, zaškrtávací políčko, přepínače atd.

## Rozdíl mezi soubory .H a .HH

Mezi hlavičkovými soubory .h a .hh zjevně není žádný takový rozdíl, než je doporučený způsob jejich použití pro příslušné jazyky, tj. [C](/cs/programming/c/) nebo C++. Pojmenování hlavičkových souborů podle těchto jazyků vám pomůže rozlišit mezi nimi ve velkém projektu, který může být kombinací implementací C a C++.

Kromě toho, pokud jsou záhlaví oddělena příponou, váš editor může použít příslušné formátování automaticky pro jednotlivě.

Celkově diferenciace těchto dvou formátů souborů neuškodí, ale bude výhodná a doporučuje se ji dodržovat pro rozlišení C a C++.

### Chrániče hlavy

Soubory záhlaví mohou způsobit složité chyby, pokud je do stejného souboru zahrnuto více deklarací v důsledku přidání jiných souborů záhlaví. Tyto duplicitní definice způsobují chyby kompilátoru. Této problematické situaci lze předejít pomocí mechanismu zvaného header guard, což jsou direktivy podmíněné kompilace, jak je ukázáno níže.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Pomocí této hlavičky preprocesor zkontroluje, zda již nebyl definován `ANY_UNIQUE_NAME_HERE_HPP`. Pokud je záhlaví opakovaně zahrnuto do stejného souboru, obsah záhlaví bude ignorován.

## Reference

* [Filery záhlaví – Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Rozdíl mezi formáty souborů .h a .hh](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

