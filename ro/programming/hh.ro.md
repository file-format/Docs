{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh","ce este un fișier .hh","cum se deschide fișierul .hh", "extensie", "fișier", "fișier .hh","format fișier .hh", " Extensie fișier .hh","Exemplu de fișier .HH"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - Format de fișier antet C++",
  "description":"Aflați despre formatul de fișier HH și despre API-urile care pot crea și deschide fișierul HH.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Ce este un fișier HH?

Un fișier cu extensia .hh este un fișier antet C++ care include declararea variabilelor, constantelor și funcțiilor. Aceste declarații sunt utilizate de fișierele de implementare C++ corespunzătoare, de obicei salvate ca fișiere [.cpp](/ro/programming/cpp/) care conțin implementarea efectivă a logicii utilizatorului. Fișierele antet .hh sunt menționate în fișierele CPP de implementare folosind directiva `#include`. Puteți adăuga cât mai multe fișiere antet în proiectul dvs. C++ pentru a include declarații la nivel de proiect.

## Format fișier .HH

Un fișier .hh este un fișier text simplu care este creat ținând cont de regulile de definire a fișierului antet. Cele mai comune informații declarate într-un fișier .hh includ următoarele.

**`Variabile`** - În cazul programării orientate pe obiecte (OOP), un fișier antet de clasă conține definiții ale tuturor variabilelor la nivel de clasă care sunt accesibile prin fișierele codului sursă de implementare
**`Declarația metodelor`** - Toate declarațiile metodelor sunt incluse în fișierele antet .h pentru a fi accesibile în mai multe fișiere de implementare.
**`Non-Inline Function Definitions`** - Fișierele antet pot conține, de asemenea, definiții ale unei metode non-inline.
**`Hărți de mesaje`** - Un fișier antet poate conține, de asemenea, hărți de mesaje în cazul implementării unui cod sursă MFC. În acest caz, hărțile de mesaje sunt legate de implementarea funcționalității care este legată de elementele UI, cum ar fi butonul, caseta de selectare, butoanele radio etc.

## Diferența dintre fișierele .H și .HH

Aparent, nu există o astfel de diferență între fișierele de antet .h și .hh, în afară de modul recomandat de utilizare a acestora pentru limbajele respective, adică [C](/ro/programming/c/) sau C++. Numirea fișierelor de antet în funcție de aceste limbi vă ajută să faceți distincția între acestea într-un proiect mare care poate fi un amestec de implementări C și C++.

În plus, dacă anteturile sunt separate prin extensie, editorul dvs. poate aplica automat formatarea corespunzătoare, respectiv.

În general, diferențierea acestor două formate de fișiere nu va face niciun rău, dar va fi avantajoasă și este încurajată să urmeze pentru distincția C și C++.

### Gărzi de antet

Fișierele antet pot duce la erori complexe în cazul în care mai multe declarații sunt incluse în același fișier ca urmare a adăugării altor fișiere antet. Aceste definiții duplicat generează erori ale compilatorului. Această situație problematică poate fi evitată printr-un mecanism numit header guard care sunt directive de compilare condiționată, așa cum se arată mai jos.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Cu acest antet, preprocesorul verifică dacă `ANY_UNIQUE_NAME_HERE_HPP` a fost deja definit. Dacă antetul este inclus în mod repetat în același fișier, conținutul antetului va fi ignorat.

## Referințe

* [Filere antet - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Diferența dintre formatele de fișiere .h și .hh](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

