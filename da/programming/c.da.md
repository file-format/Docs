{
  "date": "2020-01-10",
  "keywords": [
"c",
".c",
"hvad er ac fil",
"hvordan man åbner filen c",
"udvidelse",
"fil",
"c fil",
"c filformat",
"c filtypenavn"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "C - C sprogprogrammeringsfil",
  "description": "Lær om C-filformat og API'er, der kan oprette og åbne C-filer.",
  "linktitle": "C",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--dac"
}
},
  "lastmod": "2020-01-10"
}

## Hvad er en C fil?

En fil gemt med filtypen c er en kildekodefil skrevet i programmeringssproget C. **C-filen** inkluderer al implementering af applikationens funktionalitet i form af kildekode. Erklæringen af kildekoden er skrevet i header-filerne, der er gemt med udvidelsen [.h](/programming/h/). C++ er den moderne form for C-sprog og bruges til at udvikle det meste af softwaren i dag.

## Kort historie

C-sproget blev til som et resultat af at skabe forskellige værktøjer til UNIX-operativsystemet. Denis Ritchie, manden bag skabelsen af dette programmeringssprog, arbejdet startede oprindeligt i 1960'erne og begyndelsen af 1970'erne.

## C filformat

C-filer er skrevet i almindeligt tekstfilformat efter programmeringssprogets syntaks. En typisk C-fil vil have:

 * import erklæring øverst i filen for at importere eventuelle overskrifter Filer
 * en eller flere metoder til at implementere ønsket funktionalitet

### Import af overskrifter

Header-filerne med filtypenavnet .h indeholder nødvendige inkluderingssætninger for at inkludere andre funktionalitetsfiler i projektet. Derudover indeholder disse de erklæringer om metoder, der er defineret i implementeringsfilen. Header-filer er inkluderet ved hjælp af include-sætningen som vist nedenfor.

```
#include <filename.h>
```

### Kildekodeimplementering

Selve implementeringen af funktionskravene er kodet som metoder i C-filen. Hver metode i en C-fil har en returtype, metodenavn og kan have nogle inputparametre. Hvis returtypen ikke er ugyldig, kan metoden returnere en vis værdi.

### C-kodeeksempel
Her er et eksempel på et program:

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



## **Referencer** ##

* [Klasseimplementering - af Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)


