---
date: 2019-10-11
keywords: dart, .dart, dart file format, dart file, how to run dart files, .dart extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dincəsənət fayl formasıat
linktitle: Dart
description: LDart faylı yarada və aça bilən Dart fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Dart faylı nədir? ##

Dart faylı Google tərəfindən hazırlanmış müştəri üçün optimallaşdırılmış proqramlaşdırma dili olan Dart proqramlaşdırma dilinin mənbə kodunu ehtiva edir və mobil, masaüstü, veb, Iot (əşyaların İnterneti) və s. üçün proqramlar yaratmaq üçün istifadə olunur. Dart obyekt yönümlü dildir. C. Dart-a oxşar sintaksis ilə JavaScript və ya yerli koda tərtib edilə bilər. Dart fayllarını javascript faylını işlədə bildiyiniz kimi məşhur veb brauzerdə işlədə bilərsiniz. Dart SDK ilə birlikdə gələn Dart virtual maşını kimi tanınan komanda xətti aləti də Dart fayllarını tərtib etmək və işə salmaq üçün istifadə olunur.

## Qısa tarix ##

The Dart project was founded by Lars Bak and Kasper Lund and the first version was released on 14th November 2013. Mən əvvəldən Dart, Google Chrome-da Dart VM-ni daxil etmək planlarına görə veb parçalanmasına görə tənqid edildi. Bu planlar ləğv edildi və Dart 2015-ci ildə 1.9 versiyasının buraxılması ilə JavaScript-i tərtib etməyə diqqət yetirdi.

Dart 2.0 2018-ci ilin Avqust ayında buraxıldı, burada dart2-native genişləndirilməsi təqdim edildi və Dart kodunu yerli Linux, Windows, macOS platformaları üçün tərtib etdi. Bu genişləndirmə müstəqil icra sənədlərini işə saldı, buna görə Dart SDK-nın bu platformalarda Dart proqramlarını işə salması tələb olunmadı. Bu genişləndirmə həmçinin Flutter ilə inteqrasiya olunub və platformalararası proqramlar yaratmağa imkan verir.

ECMA Dart-ı 2014-cü ilin iyulunda ilk nəşri və 2014-cü ilin dekabrında ikinci nəşri ilə standartlaşdırdı.


## Dart kodunu necə işlətmək/icra etmək olar ##

Dart kodu aşağıdakı yollarla işləyə bilər:

- **JavaScript kimi tərtib edilmişdir**:</br> Dart kodu dart2js kompilyatorundan istifadə etməklə JavaScript-də tərtib edilir. Tərtib edilmiş JavaScript kodu bütün əsas veb brauzerlərə uyğun gəlir.
- **Tək başına**:</br> Dart Software Development Kit (SDK) Dart kodunu komanda xətti interfeysində işlətməyə imkan verən müstəqil Dart VM ilə göndərilir. Dart istifadəçilərə tam funksional proqramlar yazmağa imkan verən tam standart kitabxana ilə təchiz edilir.
- **Vaxtdan əvvəl (AOT) tərtib edilmişdir**:</br> Dart kodu, mobil proqramların Flutter ilə qurulmasına imkan verən maşın koduna AOT tərəfindən tərtib edilə bilər.
- **Doğma**:</br> Dart2native kompilyatoru ilə Dart kodu Windows, Linux və macOS-da işləyə bilən müstəqil icra edilə bilən proqramlara tərtib edilə bilər.

## Dart Fayl Format ##

Dart interfeysləri, miksinləri, abstrakt sinifləri, dəqiqləşdirilmiş generikləri və tip interfeysi dəstəkləyən C üslublu obyekt yönümlü dildir.

### Sintaksis ###

Aşağıda Dart sintaksisinin bəzi nümunələri verilmişdir.

#### Konsola çap edin ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Döngülər və Massivlər ####

```dart
// loops and arrays
var names = {
  'John',
  'James',
  'Rose',
};
main() {
  for (var name in names) {
    print(name);
  }
}
```

#### Funksiyalar ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Dərslər ####

```dart
// classes
abstract class Person {
  detail();
}

class Student implements Person {
  String firstName = "Jack";
  String lastName = "Wick";
  detail() => print("Student: $firstName $lastName");
}

main() {
  // The 'new' keyword is optional.
  Student student = Student();
  student.detail();
}
```

#### Qarışıqlar ####

Miksinlər metodları/dəyişənləri miras almadan götürə biləcəyimiz normal siniflərdir. Bu *with* açar sözündən istifadə etməklə edilir.

```dart
class B {  
  method(){
     ....
  }
}

class A with B {
  ....
     ......
}
void main() {
  A a = A();
  a.method();  //We are able to access the method of B class without inheriting from it.
}
```

## İstinadlar ##

- [Dart (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

