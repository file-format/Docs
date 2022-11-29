{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c","vad är ac-fil","hur man öppnar c-fil", "tillägg", "fil", "c-fil","c-filformat", "c-filtillägg"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"C - C Språkprogrammeringsfil",
  "description":"Läs mer om C-filformat och API:er som kan skapa och öppna C-filer.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Vad är en C-fil?

En fil sparad med filändelsen c är en källkodsfil skriven i programmeringsspråket C. **C-filen** inkluderar all implementering av applikationens funktionalitet i form av källkod. Deklarationen av källkoden skrivs i rubrikfilerna som sparas med tillägget [.h](/sv/programming/h/). C++ är den moderna formen av C-språk och används för att utveckla det mesta av mjukvaran nuförtiden.

## Kortfattad bakgrund

C-språket kom till som ett resultat av att skapa olika verktyg för UNIX-operativsystemet. Denis Ritchie, mannen bakom skapandet av detta programmeringsspråk, arbetet startade ursprungligen på 1960-talet och början av 1970-talet.

## C filformat

C-filer skrivs i vanlig textfilformat enligt programmeringsspråkets syntax. En typisk C-fil kommer att ha:

* import uttalande högst upp i filen för att importera alla rubrikfiler
* en eller flera metoder för att implementera önskad funktionalitet

### Importera rubriker

Rubrikfilerna, med tillägget .h, innehåller nödvändiga inkluderingssatser för att inkludera andra funktionsfiler i projektet. Dessutom innehåller dessa deklarationer av metoder som definieras i implementeringsfilen. Rubrikfiler inkluderas med hjälp av include-satsen som visas nedan.

```
#include <filename.h>
```

### Implementering av källkod

Själva implementeringen av funktionskraven kodas som metoder i C-filen. Varje metod i en C-fil har en returtyp, metodnamn och kan ha några indataparametrar. Om returtypen inte är ogiltig kan metoden returnera något värde.

### C-kodexempel
Här är ett exempel på ett program:

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



## **Referenser** ##

* [Klassimplementering - av Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

