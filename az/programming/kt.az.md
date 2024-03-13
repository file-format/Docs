---
date: 2019-10-11
keywords: kt, .kt, kotlin file format, how to open kotlin files, how to run kotlin files, .kt file format, kt file , kotlin file extension, .kt extention, kotlin vs java
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT Fayl Formasıat
linktitle: KT
description: LKT faylı yarada və aça bilən KT fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## KT faylı nədir? ##

Kotlin dilində yazılmış mənbə kodu adətən **Kotlin fayl uzantısı** kimi tanınan .kt uzantısı ilə saxlanılır. Kotlin, [Java](/programming/java/) ilə tam qarşılıqlı işləmək üçün JetBrains tərəfindən hazırlanmış ümumi məqsədli çarpaz platforma proqramlaşdırma dilidir. Kotlin ticarət nişanı Kotlin Fondu tərəfindən qorunur.

Kotlin was announced as the preferred programming language for Android App development by Google on 7th May 2019. Android Studio 3.0 2017-ci ilin oktyabrında Android Tətbiqinin inkişafı üçün alternativ olaraq Kotlin-i dəstəkləməyə başladı.

## Kotlin KT Fayl Formatının Qısa Tarixi##

Kotlin 2011-ci ilin iyul ayında JetBrains tərəfindən JVM üçün yeni proqramlaşdırma dili kimi təqdim edildi. JetBrains-in rəhbəri Dmitri Jemerov dillərin əksəriyyətində Scala istisna olmaqla, axtardıqları funksiyaların çatışmadığını, lakin Scala-nın yavaş tərtib edilməsinin çatışmazlıq olduğunu söylədi. Kotlin-in əsas məqsədlərindən biri Java kimi tez tərtib etmək idi. Kotlin layihəsi 2012-ci ilin fevralında Apache 2 Lisenziyası altında açıq mənbəli idi.

Version 1.0 of Kotlin was released on 15 February 2015. Android Google I/O 2017-də Android-də Kotlin üçün birinci dərəcəli dəstəyi elan etdi. Kotlin 1.2 JVM və JavaScript platformaları arasında kodu paylaşmaq imkanı ilə 28 noyabr 2017-ci ildə buraxıldı. Kotlin 1.3 asinxron proqramlaşdırma dəstəyi ilə 29 oktyabr 2018-ci ildə buraxıldı. Google 7 may 2019-cu ildə Android Tətbiqinin inkişafı üçün Kotlin-in üstünlük verilən proqramlaşdırma dili olduğunu elan etdi. Kotlin 1.4 Swift/Objective-C ilə qarşılıqlı əlaqəni dəstəkləmək üçün bəzi cüzi dəyişikliklərlə 2020-ci ilin avqustunda buraxıldı.

## Kotlin Sintaksisi ##

Kotlin Java-dan daha yaxşı olmaq üçün hazırlanmışdır, lakin Java-dan Kotlin-ə tədricən miqrasiyaya imkan vermək üçün Java kodu ilə işləyə bilər.

 * Kotlin dilində nöqtəli vergüllər isteğe bağlıdır. Bəyanatın sonunu göstərmək üçün yeni sətir kifayətdir.
 * Kotlin, *val* açar sözü ilə təyin olunan yalnız oxuna bilən və *var* açar sözü ilə təyin olunan dəyişkən iki növ dəyişəni dəstəkləyir.
 * Dərslər özəldir və standart olaraq yekundur. Sinifdən əldə etmək üçün əsas sinif *açıq* açar sözü ilə elan edilməlidir.
 * Kotlin həmçinin prosedur proqramlaşdırmanı dəstəkləyir.
 * Kotlin proqramına giriş nöqtəsi Java, C# və s.-ə bənzər əsas funksiyadır.

### Sintaksis Nümunəsi ###

Aşağıda Kotlin sintaksisinin nümunəsi verilmişdir.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Yuxarıdakı kodda **fun** açar sözü main adlı funksiyanı müəyyən edir. Funksiya daxilində **val** açar sözü ilə yalnız oxunan dəyişən 'auditoriya' elan edilir. **println** metodundan istifadə edərək, konsolda Kotlindən Salam Dünya çap olunur. Dəyişən auditoriyanın dəyəri **$** işarəsi ilə sətirə daxil edilir.

## Kotlin Javaya qarşı
Kotlin, bir çox qabaqcıl xüsusiyyətləri təklif edən Android proqramları yazmaq üçün rəsmi dildir, lakin bir çox ekspert Java tərtibatçıları hələ də Kotlin-ə keçməyə maraq göstərmirlər. Onlar hər şeyi yalnız Java ilə edə biləcəklərini düşünürlər. Beləliklə, java tərtibatçılarını keçid etməyə inandıra biləcək iki texnologiya arasında müqayisə:

| Parametr | Java | Kotlin |
|--------------------|-----------|---------------- -|
| Singletons Objects | √ | √ |
| Wildcard növləri | √ | Χ |
| Tərtib | Bayt kodları | Virtual Maşın |
| Lambda ifadəsi | Χ | √ |
| İnvariant massiv | Χ | √ |
| Qeyri-özəl Sahələr | √ | Χ |
| Ağıllı Yayım | Χ | √ |
| Null Təhlükəsizlik | Χ | √ |
| Statik Üzvlər | √ | Χ |

## İstinadlar ##

- [Kotlin (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

