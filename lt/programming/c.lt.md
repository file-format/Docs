{
  "date": "2020-01-10",
  "keywords": [
"c",
".c",
"kas yra ac failas",
"Kaip atidaryti c failą",
"pratęsimas",
"failą",
"c failą",
"c failo formatu",
"c failo plėtinį"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "C - C kalbos programavimo failas",
  "description": "Sužinokite apie C failo formatą ir API, kurios gali kurti ir atidaryti C failus.",
  "linktitle": "C",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--ltc"
}
},
  "lastmod": "2020-01-10"
}

## Kas yra C failas?

Failas, įrašytas su c failo plėtiniu, yra šaltinio kodo failas, parašytas C programavimo kalba. **C failas** apima visas programos funkcijų įgyvendinimas šaltinio kodo forma. Šaltinio kodo deklaracija įrašoma antraštės failuose, kurie išsaugoti su plėtiniu [.h](/programming/h/). C++ yra moderni C kalbos forma, kuri šiais laikais naudojama kuriant didžiąją dalį programinės įrangos.

## Trumpa istorija

C kalba atsirado sukūrus skirtingas UNIX operacinei sistemai skirtas priemones. Denisas Ritchie, šios programavimo kalbos kūrėjas, darbas iš pradžių prasidėjo septintajame ir aštuntojo dešimtmečio pradžioje.

## C failo formatas

C failai parašyti paprasto teksto failo formatu pagal programavimo kalbos sintaksę. Įprastame C faile bus:

 * importavimo teiginį failo viršuje, kad importuotumėte bet kokias antraštes Failai
 * vienas ar daugiau metodų norimai funkcijai įgyvendinti

### Antraštės importavimas

Antraštės failuose, kurių plėtinys yra .h, yra būtini įtraukimo teiginiai, norint įtraukti kitus funkcionalumo failus į projektą. Be to, juose yra metodų, apibrėžtų diegimo faile, deklaracijos. Antraštės failai įtraukiami naudojant teiginį įtraukti, kaip parodyta toliau.

```
#include <filename.h>
```

### Šaltinio kodo diegimas

Faktinis funkcinių reikalavimų įgyvendinimas yra užkoduotas kaip metodai C faile. Kiekvienas C failo metodas turi grąžinimo tipą, metodo pavadinimą ir gali turėti kai kuriuos įvesties parametrus. Jei grąžinimo tipas nėra tuščias, metodas gali grąžinti tam tikrą reikšmę.

### C kodo pavyzdys
Čia yra AC programos pavyzdys:

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



## **Nuorodos** ##

* [Klasės įgyvendinimas – pagal Vikipediją](https://en.wikipedia.org/wiki/Class_implementation_file)


