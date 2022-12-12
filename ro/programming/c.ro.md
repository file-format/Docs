{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c","ce este fișierul ac","cum se deschide fișierul c", "extensie", "fișier", "fișier c","format fișier c", "extensie fișier c"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier de programare limbaj C – C",
  "description":"Aflați despre formatul de fișier C și despre API-urile care pot crea și deschide fișiere C.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Ce este un fișier C?

Un fișier salvat cu extensia de fișier c este un fișier cod sursă scris în limbajul de programare C. **Fișierul C** include toată implementarea funcționalității aplicației sub formă de cod sursă. Declarația codului sursă este scrisă în fișierele de antet care sunt salvate cu extensia [.h](/ro/programming/h/). C++ este forma modernă a limbajului C și este folosită pentru a dezvolta majoritatea software-ului în zilele noastre.

## Scurt istoric

Limbajul C a apărut ca urmare a creării diferitelor utilități pentru sistemul de operare UNIX. Denis Ritchie, omul din spatele creării acestui limbaj de programare, lucrarea a început inițial în anii 1960 și începutul anilor 1970.

## C Format de fișier

Fișierele C sunt scrise în format de fișier text simplu, urmând sintaxa limbajului de programare. Un fișier C tipic va avea:

* declarație de import în partea de sus a fișierului pentru a importa orice fișiere de antet
* una sau mai multe metode de implementare a funcționalității dorite

### Import anteturi

Fișierele antet, cu extensia .h, conțin instrucțiunile include necesare pentru includerea altor fișiere de funcționalități în proiect. În plus, acestea conțin declarațiile metodelor definite în fișierul de implementare. Fișierele antet sunt incluse folosind instrucțiunea include așa cum se arată mai jos.

```
#include <filename.h>
```

### Implementarea codului sursă

Implementarea efectivă a cerințelor funcționale este codificată ca metode în fișierul C. Fiecare metodă dintr-un fișier C are un tip de returnare, un nume de metodă și poate avea câțiva parametri de intrare. Dacă tipul returnat nu este nul, metoda poate returna o anumită valoare.

### Exemplu de cod C
Iată un exemplu de program ac:

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



## **Referințe** ##

* [Implementarea clasei - Prin Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

