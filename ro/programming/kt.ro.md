---
date: 2019-10-11
keywords: kt, .kt, format de fișier kotlin, cum să deschideți fișiere kotlin, cum să rulați fișiere kotlin, format de fișier .kt, fișier kt, extensie de fișier kotlin, extensie .kt, kotlin vs java
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier KT
linktitle: KT
description: "Aflați despre formatul de fișier KT și despre API-urile care pot crea și deschide fișiere KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Ce este un fișier KT? ##

Un cod sursă scris în Kotlin este salvat cu extensia .kt, cunoscută în mod obișnuit ca **extensie de fișier Kotlin**. Kotlin este un limbaj de programare multiplatformă de uz general dezvoltat de JetBrains pentru a fi pe deplin interoperabil cu [Java](/ro/programming/java/). Marca Kotlin este protejată de Fundația Kotlin.

Kotlin a fost anunțat ca limbaj de programare preferat pentru dezvoltarea aplicațiilor Android de către Google pe 7 mai 2019. Android Studio 3.0 a început să accepte Kotlin ca alternativă pentru dezvoltarea aplicațiilor Android în octombrie 2017.

## Scurt istoric al formatului de fișier Kotlin KT##

Kotlin a fost dezvăluit de JetBrains în iulie 2011 ca un nou limbaj de programare pentru JVM. Conducătorul JetBrains, Dmitry Jemerov, a spus că în majoritatea limbilor lipsesc caracteristici pe care le căutau, cu excepția Scala, dar compilarea lentă a Scala a fost un dezavantaj. Unul dintre obiectivele principale ale lui Kotlin a fost compilarea la fel de rapid ca Java. Proiectul Kotlin a fost open-source sub licența Apache 2 în februarie 2012.

Versiunea 1.0 a Kotlin a fost lansată pe 15 februarie 2015. Android a anunțat suport de primă clasă pentru Kotlin pe Android la Google I/O 2017. Kotlin 1.2 a fost lansat pe 28 noiembrie 2017 cu posibilitatea de a partaja cod între platformele JVM și JavaScript. Kotlin 1.3 a fost lansat pe 29 octombrie 2018 cu suport pentru programare asincronă. Google a anunțat că Kotlin este limbajul de programare preferat pentru dezvoltarea aplicațiilor Android pe 7 mai 2019. Kotlin 1.4 a fost lansat în august 2020, cu câteva modificări ușoare pentru a sprijini interoperabilitatea cu Swift/Objective-C.

## Sintaxa Kotlin ##

Kotlin a fost conceput pentru a fi mai bun decât Java, dar totuși să fie interoperabil cu codul Java pentru a permite migrarea treptată de la Java la Kotlin.

* Punctele și virgulă sunt opționale în Kotlin. O nouă linie este suficientă pentru a indica sfârșitul declarației.
* Kotlin acceptă două tipuri de variabile, numai pentru citire, definite de cuvântul cheie *val* și mutabile, definite de cuvântul cheie *var*.
* Cursurile sunt private și finale în mod implicit. Pentru a deriva dintr-o clasă, clasa de bază trebuie să fie declarată cu cuvântul cheie *open*.
* Kotlin acceptă și programarea procedurală.
* Punctul de intrare în programul Kotlin este funcția „principală” similară cu Java, C# etc.

### Exemplu de sintaxă ###

Următorul este un exemplu de sintaxă Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

În codul de mai sus, cuvântul cheie **fun** definește funcția numită main. În interiorul funcției, o variabilă numai în citire „audience” este declarată cu cuvântul cheie **val**. Prin utilizarea metodei **println**, „Hello World from Kotlin” este tipărit pe consolă. Valoarea audienței variabile este injectată în șir cu semnul **$**.

## Kotlin vs Java
Kotlin este o limbă oficială pentru a scrie aplicații Android, oferind multe funcții avansate, dar mulți dezvoltatori Java experți încă nu își arată interesul de a trece la Kotlin. Ei cred că pot face totul numai cu Java. Deci, următoarea este comparația dintre două tehnologii care pot convinge dezvoltatorii java să comute:

| Parametru | Java | Kotlin |
|---------------------|------------|----------------- -|
| Singletons Obiecte | √ | √ |
| Tipuri wildcard | √ | Χ |
| Compilare | Bytecodes | Mașină virtuală |
| Expresia Lambda | Χ | √ |
| Matrice invariantă | Χ | √ |
| Câmpuri non-private | √ | Χ |
| Smart Casts | Χ | √ |
| Siguranță nulă | Χ | √ |
| Membri statici | √ | Χ |

## Referințe ##

- [Kotlin (limbaj de programare) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(limbaj_de_programare))

