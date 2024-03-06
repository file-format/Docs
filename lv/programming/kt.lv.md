---
date: 2019-10-11
keywords: kt, .kt, kotlin file format, how to open kotlin files, how to run kotlin files, .kt file format, kt file , kotlin file extension, .kt extention, kotlin vs java
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT faila formaat
linktitle: KT
description: Lnopelniet par KT faila formātu un API, kas var izveidot un atvērt KT failus.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Kas ir KT fails? ##

Kotlin rakstītais pirmkods tiek saglabāts ar paplašinājumu .kt, kas parasti ir pazīstams kā **Kotlin faila paplašinājums**. Kotlin ir vispārējas nozīmes starpplatformu programmēšanas valoda, ko izstrādājis JetBrains, lai tā būtu pilnībā sadarbspējīga ar [Java](/programming/java/). Kotlinas preču zīmi aizsargā Kotlinas fonds.

Kotlin was announced as the preferred programming language for Android App development by Google on 7th May 2019. Android Studio 3.0 sāka atbalstīt Kotlin kā alternatīvu Android lietotņu izstrādei 2017. gada oktobrī.

## Īsa Kotlin KT faila formāta vēsture ##

JetBrains 2011. gada jūlijā atklāja Kotlinu kā jaunu JVM programmēšanas valodu. JetBrains vadītājs Dmitrijs Jemerovs sacīja, ka lielākajā daļā valodu trūkst funkciju, kuras viņi meklēja, izņemot Scala, taču Scala lēnā kompilācija bija trūkums. Viens no galvenajiem Kotlin mērķiem bija apkopot tikpat ātri kā Java. 2012. gada februārī Kotlin projekts tika atvērts ar Apache 2 licenci.

Version 1.0 of Kotlin was released on 15 February 2015. Android paziņoja par pirmās klases atbalstu Kotlin operētājsistēmā Android Google I/O 2017. Kotlin 1.2 tika izlaists 2017. gada 28. novembrī ar iespēju koplietot kodu starp JVM un JavaScript platformām. Kotlin 1.3 tika izlaists 2018. gada 29. oktobrī ar asinhronās programmēšanas atbalstu. 2019. gada 7. maijā Google paziņoja, ka Kotlin ir vēlamā programmēšanas valoda Android lietotņu izstrādei. Kotlin 1.4 tika izlaista 2020. gada augustā ar nelielām izmaiņām, lai atbalstītu sadarbspēju ar Swift/Objective-C.

## Kotlina sintakse ##

Kotlin tika izstrādāts tā, lai tas būtu labāks par Java, taču joprojām būtu savietojams ar Java kodu, lai nodrošinātu pakāpenisku migrāciju no Java uz Kotlin.

 * Kotlinā semikoli nav obligāti. Pietiek ar jaunu rindiņu, lai norādītu paziņojuma beigas.
 * Kotlin atbalsta divu veidu mainīgos, tikai lasāmos, ko definē atslēgvārds *val*, un mainīgos, ko definē atslēgvārds *var*.
 * Nodarbības pēc noklusējuma ir privātas un galīgas. Lai iegūtu no klases, bāzes klase ir jādeklarē ar *open* atslēgvārdu.
 * Kotlins atbalsta arī procesuālo programmēšanu.
 * Ieejas punkts Kotlin programmā ir galvenā funkcija, kas līdzīga Java, C# utt.

### Sintakses piemērs ###

Tālāk ir sniegts Kotlin sintakses piemērs.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Iepriekš minētajā kodā atslēgvārds **fun** definē funkciju ar nosaukumu main. Funkcijā ar atslēgvārdu **val** tiek deklarēts tikai lasāms mainīgais auditorija. Izmantojot **println** metodi, uz konsoles tiek izdrukāts Hello World from Kotlin. Mainīgās auditorijas vērtība tiek ievadīta virknē ar zīmi **$**.

## Kotlin pret Java
Kotlin ir oficiālā valoda Android lietotņu rakstīšanai un piedāvā daudzas uzlabotas funkcijas, taču daudzi pieredzējuši Java izstrādātāji joprojām neizrāda interesi pāriet uz Kotlin. Viņi domā, ka visu var izdarīt tikai ar Java. Tālāk ir sniegts divu tehnoloģiju salīdzinājums, kas var pārliecināt Java izstrādātājus pārslēgties:

| Parametrs | Java | Kotlins |
|--------------------|------------|----------------- -|
| Singletons objekti | √ | √ |
| Aizstājējzīmju veidi | √ | Χ |
| Kompilācija | baitu kodi | Virtuālā mašīna |
| Lambda izteiksme | Χ | √ |
| Nemainīgais masīvs | Χ | √ |
| Neprivāti lauki | √ | Χ |
| Smart Casts | Χ | √ |
| Null Drošība | Χ | √ |
| Statiskie locekļi | √ | Χ |

## Atsauces Nr.

- {{HIPERSAITE1}})

