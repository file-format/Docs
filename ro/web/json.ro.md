---
date: 2019-10-11
keywords: json, .json, format de fișier json, cum se deschide fișiere json, notație obiect javascript, format de date json, format de fișier .json
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier JSON - Ce este un fișier JSON?
linktitle: JSON
description: "Aflați despre formatul de fișier JSON și despre API-urile care pot crea și deschide fișiere JSON."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Ce este un fișier JSON?

JSON (JavaScript Object Notation) este un format de fișier standard deschis pentru partajarea datelor care utilizează text care poate fi citit de om pentru a stoca și transmite date. Fișierele JSON sunt stocate cu extensia .json. JSON necesită mai puțină formatare și este o alternativă bună pentru [XML](/ro/web/xml/). JSON este derivat din JavaScript, dar este un format de date independent de limbă. Generarea și analiza JSON este acceptată de multe limbaje de programare moderne. *application/json* este tipul media utilizat pentru JSON.

## Format de fișier JSON - Scurt istoric

Era nevoie de comunicare în timp real de la server la client care să ducă la crearea JSON. Formatul JSON a fost specificat pentru prima dată de Douglas Crockford în martie 2001. JSON s-a bazat pe Standardul ECMA-262 ediția a treia - decembrie 1999, care este un subset de JavaScript.

Prima ediție a standardului JSON ECMA-404 a fost publicată în octombrie 2013 de Ecma International. RFC 7159 a devenit principala referință pentru utilizările Internetului JSON în 2014. În noiembrie 2017, ISO/IEC 21778:2017 a fost publicat ca standard internațional. RFC 8259 a fost publicat pe 13 decembrie 2017 de The Internet Engineering Task Force, care este versiunea actuală a Internet Standard STD 90.

## Structura fișierului JSON

Datele JSON sunt scrise în perechi **cheie/valoare**. Cheia și valoarea sunt separate prin două puncte (:) în mijloc, cu cheia în stânga și valoarea în dreapta. Diferite perechi cheie/valoare sunt separate prin virgulă (,). Cheia este un șir înconjurat de ghilimele duble, de exemplu „nume”. Valorile pot fi de următoarele tipuri.

- „Număr”.
- `Șir`: Secvență de caractere Unicode înconjurate de ghilimele duble.
- `Boolean`: Adevărat sau Fals.
- `Matrice`: O listă de valori înconjurate de paranteze drepte, de exemplu

```json
[ „Mer”, „Banană”, „Portocală”]
```

- „Obiect”: o colecție de perechi cheie/valoare înconjurate de acolade, de exemplu

```json
{"name": "Jack", "age": 30, "favoriteSport": "Fotbal"}
```

Obiectele JSON pot fi, de asemenea, imbricate pentru a reprezenta structura datelor. Mai jos este un exemplu de obiect JSON.

### Exemplu de format JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Care este dimensiunea maximă a fișierului JSON?

Nu există practic nicio limită pentru dimensiunea maximă a unui fișier JSON. Poate fi atât de lung cât spațiul necesar conținutului de stocat.

Când vine vorba de utilizarea formatului de fișier JSON pentru transferul de date pe internet, trebuie să fiți atenți la resursele disponibile ale computerului. Dacă sunt transferate date JSON mari, transferul va fi afectat dacă browserul client are memorie limitată.


Nu există o limită strictă definită de specificații, dar trebuie să aveți grijă să nu epuizați resursele de pe computerele utilizatorilor dvs., deoarece le va degrada rapid experiența utilizatorului și este posibil ca aceștia să vă abandoneze aplicația.

## JSON vs XML

**XML** este un alt format de fișier comun și utilizat pe scară largă pentru schimbul de date pe internet. Când vine vorba de schimbul de date între aplicații, dezvoltatorii au opțiunea de a folosi atât formatele de fișiere XML, cât și JSON. Cu toate acestea, JSON este adoptat ca cea mai convenabilă modalitate de schimb de date între aplicații prin internet din următoarele motive.

1. JSON oferă o vizualizare clară și mai ușor de citit a datelor în comparație cu formatele de fișiere XML
1. JSON reduce suprasarcina transferului de date pe internet, deoarece are un număr mai mic de caractere pentru a defini același set de date în comparație cu XML
1. Limbajele de programare moderne oferă analizoare încorporate pentru a analiza răspunsul JSON pe web.

## Știați?

Puteți deveni colaborator la FileFormat.com pentru a menține comunitatea de format de fișier la curent cu descoperirile dvs. Dacă trebuie să împărtășiți ceva despre formatele de fișiere JSON sau Web, puteți publica rezultatele în secțiunea [Web File Format News](https://news.fileformat.com/t/Web) pentru ca oamenii să afle mai multe din acestea.

## Referințe

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [O introducere în JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

