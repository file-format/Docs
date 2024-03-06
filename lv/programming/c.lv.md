{
  "date": "2020-01-10",
  "keywords": [
"c",
".c",
"kas ir ac fails",
"kā atvērt c failu",
"pagarinājumu",
"failu",
"c failu",
"c faila formātā",
"c faila paplašinājums"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "C - C valodas programmēšanas fails",
  "description": "Uzziniet par C faila formātu un API, kas var izveidot un atvērt C failus.",
  "linktitle": "C",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--lvc"
}
},
  "lastmod": "2020-01-10"
}

## Kas ir C fails?

Fails, kas saglabāts ar faila paplašinājumu c, ir avota koda fails, kas rakstīts C programmēšanas valodā. **C fails** ietver visu lietojumprogrammas funkcionalitātes ieviešanu avota koda veidā. Avota koda deklarācija ir ierakstīta galvenes failos, kas ir saglabāti ar paplašinājumu [.h](/programming/h/). C++ ir modernā C valodas forma, un mūsdienās to izmanto, lai izstrādātu lielāko daļu programmatūras.

## Īsa vēsture

C valoda radās dažādu UNIX operētājsistēmas utilītu izveides rezultātā. Denis Ritchie, cilvēks aiz šīs programmēšanas valodas izveides, darbs sākotnēji sākās 1960. gados un 1970. gadu sākumā.

## C Faila formāts

C faili ir rakstīti vienkārša teksta faila formātā, ievērojot programmēšanas valodas sintakse. Tipiskā C failā būs:

 * importēšanas paziņojums faila augšdaļā, lai importētu jebkuru galvenes failus
 * viena vai vairākas metodes, lai ieviestu vēlamo funkcionalitāti

### Galvenes importēšana

Galvenes failos ar paplašinājumu .h ir ietverti nepieciešamie iekļaušanas paziņojumi citu funkcionalitātes failu iekļaušanai projektā. Turklāt tie satur ieviešanas failā definēto metožu deklarācijas. Galvenes faili ir iekļauti, izmantojot iekļaušanas paziņojumu, kā parādīts tālāk.

```
#include <filename.h>
```

### Avota koda ieviešana

Funkcionālo prasību faktiskā īstenošana ir kodēta kā metodes C failā. Katrai C faila metodei ir atgriešanas veids, metodes nosaukums un var būt daži ievades parametri. Ja atgriešanas veids nav nederīgs, iespējams, metode atgriež kādu vērtību.

### C koda piemērs
Šeit ir ac programmas piemērs:

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



## **Atsauces** ##

* [Class Implementation — Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)


