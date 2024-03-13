---
date: 2019-10-11
keywords: java, .java, java file format, how to open java files, how to run java files, java file, java sample code
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java fayl formasıat
linktitle: Java
description: LJava fayl formatı və Java faylını yarada və aça bilən API-lər haqqında məlumat əldə edins.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Java faylı nədir? ##
Java mənbə kodu olan və .java fayl uzantısı ilə saxlanılan fayl Java faylı kimi tanınır. Java oyunları, mobil, veb və masaüstü proqramların inkişafı üçün ən çox istifadə edilən texnologiyalardan biridir. Java platformadan müstəqil olduğundan, Windows, Mac, Linux, Raspberry Pi və s.-də qüsursuz işləyir. Java C# və C++ dillərinə çox bənzəyir, ona görə də bu dillər arasında keçid etmək daha asandır.

## Qısa tarix ##

Java layihəsi 1991-ci ilin iyununda James Gosling, Mike Sheridan və Patrick Naughton tərəfindən başladılmışdır. Java əvvəlcə Oak adlandırıldı. Daha sonra onun adı Yaşıl və nəhayət Java olaraq dəyişdirildi. James Gosling Java-nı C/C++ ilə oxşar sintaksislə dizayn etmişdir. Java-nın ilk ictimai versiyası 1996-cı ildə Sun Microsystems tərəfindən buraxılmışdır. Java-nın sürətlə populyarlaşmasına səbəb olan bütün populyar sistemlərdə işləyə bilər. 1998-ci ilin dekabrında Java 2-nin buraxılması ilə müxtəlif növ platformalar üçün çoxlu konfiqurasiyalar quruldu. Versiyaları aşağıdakı kimi idi

- J2EE (Java EE): Korporativ həllər üçün
- J2ME (Java ME): Mobil proqramlar üçün
- J2SE (Java SE): Masaüstü proqramlar üçün

19 noyabr 2006-cı ildə Java Virtual Machine (JVM) Sun tərəfindən pulsuz və açıq mənbəli proqram təminatı olaraq buraxıldı. Oracle Corporation 2009-2010-cu illərdə Sun Microsystems-i əldə etdikdən sonra Ceyms Qoslinq 2 aprel 2010-cu ildə Oracle-dan istefa verdi.

## Java kodunu necə işlətmək/icra etmək olar ##

Java kodunu icra etmək üçün əvvəlcə onu tərtib etmək lazımdır. Bunun üçün Java SDK tələb olunur. Java SDK Java kodunu bayt kodu sinif faylına tərtib edir. Eclipse və IntelliJ Idea kimi IDE-lər var ki, onlar Java kodunu tərtib etmək və icra etmək üçün kodu tamamlamaq və istifadəsi asan interfeys təmin etməklə Java faylları ilə işləməyi asanlaşdırır.

## Java fayl formatı ##

Java dilinin sintaksisi C və C++ dillərindən çox təsirlənmişdi, lakin C++-dan fərqli olaraq, Java demək olar ki, yalnız obyekt yönümlü dil kimi qurulmuşdur. Java-da bütün kodlar siniflər daxilində yazılır və hər bir məlumat elementi bir obyektdir. C++-dan fərqli olaraq, Java operatorun həddən artıq yüklənməsini və ya çoxlu varisliyi dəstəkləmir.

### Java nümunə kodu ###

Aşağıda Java sintaksisinin bir nümunəsidir.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
Yuxarıdakı kodda **public** açar sözü giriş dəyişdiricisini bildirir. Bu, bu sinfə sinif iyerarxiyasından kənar siniflər tərəfindən daxil ola biləcəyini bildirir. Giriş modifikatoru həmçinin **mühafizəli** (eyni paketdə daxil olmaq olar) və ya **özəl** (metodlara yalnız eyni sinif tərəfindən daxil ola bilər) ola bilər. Metodun qarşısındakı **statik**, metodun sinfin xüsusi nümunəsi olmadan çağırıla biləcəyini göstərir. **Void** metodun heç nə qaytarmayacağını göstərir. Sətri konsola çap etmək üçün. System.out.println əmrindən istifadə olunur. Bu əmrdə *Sistem* sinfinin *println* metodunu ehtiva edən *PrintStream* sinfinin nümunəsi olan *out* statik sahəsi var.

Java fayllarının fayl adı sinif adı ilə eyni olmalıdır. Beləliklə, nümunə kodu üçün Java faylı *ExampleApp.java* adlandırılacaq.

## İstinadlar ##

- [Java (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

