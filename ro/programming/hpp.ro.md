{
"data": "2023-06-08",
  "keywords": [
"fișier hpp",
"Ce este un fișier hpp",
"ce conține fișierul hpp",
"exemplu de fișier hpp",
"care este formatul fișierului hpp",
"fişier",
"extensie fișier hpp",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "fals",
"toc": true,
"title": "Format fișier HPP - fișier antet C++",
  "description":"Aflați despre formatul HPP și despre API-urile care pot crea și deschide fișiere HPP.",
"linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
}
},
"lastmod": "2023-06-08"
}

## Ce este un fișier HPP?

Formatul de fișier ".hpp" este folosit în mod obișnuit pentru fișierele antet în limbajul de programare C++. Fișierele antet conțin de obicei declarații și definiții ale funcțiilor, claselor, variabilelor și constantelor care sunt utilizate de alte fișiere de cod sursă în proiectul C++.

Scopul utilizării fișierelor de antet este de a oferi o modalitate de a partaja codul comun în mai multe fișiere de cod sursă fără a duplica codul în sine. Când fișierul sursă C++ trebuie să acceseze declarații sau definiții din fișierul antet, acesta include fișierul antet folosind directiva de preprocesor `#include`.

Extensia de fișier ".hpp" este adesea folosită pentru a indica faptul că un fișier este un fișier antet C++. Nu este o cerință să utilizați această extensie specifică pentru fișierele antet și este posibil să întâlniți și fișiere antet cu ".h" sau alte extensii. Alegerea extinderii este în mare măsură o chestiune de convenție și preferințe personale.

Când un fișier sursă C++ include fișierul antet folosind `#include`, compilatorul combină efectiv conținutul fișierului antet cu fișierul sursă înainte de a-l compila ca unitate. Acest lucru permite fișierului sursă să acceseze declarațiile și definițiile din fișierul antet, oferind informațiile necesare compilatorului pentru a efectua verificarea tipului și generarea codului.

## Ce conține fișierul HPP?

Iată câteva conținuturi comune pe care le puteți găsi în fișierul ".hpp":

- **Declarații de funcție:** Fișierele antet includ adesea declarații de funcție fără implementările lor reale. Aceste declarații oferă informații despre numele funcției, tipul de returnare și parametrii, permițând altor fișiere de cod sursă să utilizeze funcția fără a fi nevoie să cunoască detaliile implementării.
- **Declarații de clasă:** Fișierele antet pot conține declarații de clasă, inclusiv numele clasei, variabilele membre, funcțiile membru și specificatorii de acces. Prin includerea declarației de clasă în fișierul antet, alte fișiere de cod sursă pot crea obiecte ale acelei clase și pot accesa membrii acesteia.
- **Declarații constante:** Fișierele antet pot defini constante, cum ar fi variabile globale sau valori de enumerare care sunt menite să fie partajate în mai multe fișiere de cod sursă. Aceste constante pot fi accesate prin includerea fișierului antet în alte fișiere sursă, permițându-le să utilizeze constantele definite.
- **Definiții de tip:** Fișierele antet pot conține definiții de tip folosind cuvântul cheie "typedef" sau aliasuri de tip folosind cuvântul cheie "utilizare". Aceste definiții creează nume noi pentru tipurile existente, făcând codul mai ușor de citit și mai ușor de întreținut.
- **Definiții de funcție în linie:** În unele cazuri, fișierele de antet pot conține definiții de funcție în linie. Funcțiile inline sunt funcții mici care sunt extinse la site-ul de apel, mai degrabă decât să fie apelate ca funcție separată. Includerea definiției funcției în linie în fișierul antet permite compilatorului să înlocuiască apelul funcției cu corpul funcției direct, îmbunătățind potențial performanța.

## Exemplu de fișier HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Care este formatul fișierului HPP?

HPP este un fișier text simplu, dar urmează regulile generale și sintaxa limbajului de programare C++. Iată o detaliere a formatului general și a structurii fișierului ".hpp":

- **Apărători antet:** De obicei, un fișier ".hpp" începe cu protecții antet pentru a preveni includerile multiple ale aceluiași fișier. Acest lucru se realizează folosind directive de preprocesor precum `#ifndef`, `#define` și `#endif`. Protectia antetului se asigură că conținutul fișierului este inclus o singură dată în timpul procesului de compilare.
- **Include declarații:** După protecția antetului, puteți include alte fișiere de antet necesare folosind directiva `#include`. Acestea pot include antete standard de bibliotecă sau alte anteturi personalizate cerute de codul dvs.
- **Declarații și definiții:** Conținutul principal al fișierului ".hpp" este declarațiile și, în unele cazuri, definițiile claselor, funcțiilor, constantelor, alias-urilor de tip și altor elemente. De exemplu, puteți declara clase folosind cuvântul cheie `class`, funcțiile folosind tipul lor returnat, numele și lista de parametri și constantele folosind cuvântul cheie `const` urmat de tipul și numele lor.
- **Definiții de funcție în linie:** În anumite cazuri, puteți include definiții de funcție în linie direct în fișierul ".hpp". Funcțiile inline sunt de obicei definite în corpul clasei, ceea ce înseamnă că definiția funcției este inclusă alături de declarația acesteia. Acest lucru se poate face prin prefixarea definiției funcției cu cuvântul cheie `inline`.
- **Declarații de spații de nume:** Dacă utilizați spații de nume în codul dvs., le puteți declara în fișierul ".hpp". Acest lucru se face folosind cuvântul cheie `namespace` urmat de numele spațiului de nume și includerea codului relevant în blocul namespace.

## Referințe
* [Fișiere antet (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

