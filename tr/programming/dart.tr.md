---
date: 2019-10-11
keywords: dart, .dart, dart dosya formatı, dart dosyası, dart dosyalarının nasıl çalıştırılacağı, .dart uzantısı
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dart Dosya Biçimi
linktitle: Dart
description: "Dart dosya formatı ve Dart dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Dart dosyası nedir? ##

Bir Dart dosyası, Google tarafından geliştirilen ve mobil, masaüstü, web, IoT (nesnelerin İnterneti) vb. İçin uygulamalar oluşturmak için kullanılan, istemci tarafından optimize edilmiş bir programlama dili olan Dart programlama dilinin kaynak kodunu içerir. Dart, nesne yönelimli bir dildir C'ye benzer bir sözdizimi ile Dart, JavaScript veya yerel koda derlenebilir. Dart dosyalarını tıpkı bir javascript dosyasını çalıştırabildiğiniz gibi ünlü web tarayıcısında çalıştırabilirsiniz. Dart SDK ile birlikte gelen ve Dart sanal makinesi olarak bilinen bir komut satırı aracı da Dart dosyalarını derlemek ve çalıştırmak için kullanılır.

## Kısa Tarih ##

Dart projesi Lars Bak ve Kasper Lund tarafından kuruldu ve ilk sürüm 14 Kasım 2013'te piyasaya sürüldü. Başlarda Dart, Google Chrome'a bir Dart VM dahil etme planları nedeniyle web parçalanması nedeniyle eleştirildi. Bu planlar iptal edildi ve Dart, 2015'te 1.9 sürümünün piyasaya sürülmesiyle JavaScript'te derlemeye odaklandı.

Dart 2.0, Ağustos 2018'de yayınlandı ve burada Dart kodunu yerel Linux, Windows, macOS platformlarına derleyen dart2native uzantısı tanıtıldı. Bu uzantı, bağımsız yürütülebilir dosyaları etkinleştirdi, bu nedenle bu platformlarda Dart uygulamalarını çalıştırmak için Dart SDK'sı gerekli değildi. Bu uzantı ayrıca Flutter ile entegre edilerek platformlar arası uygulamalar oluşturmayı mümkün kılar.

ECMA, Dart'ı ilk baskısı Temmuz 2014'te ve ikinci baskısı Aralık 2014'te standartlaştırdı.


## Dart kodunu çalıştırma/yürütme ##

Dart kodu aşağıdaki şekillerde çalışabilir:

- **JavaScript olarak derlenmiştir**:</br> Dart kodu, dart2js derleyicisi kullanılarak JavaScript'te derlenir. Derlenmiş JavaScript kodu, tüm büyük web tarayıcılarıyla uyumludur.
- **Bağımsız**:</br> Dart Yazılım Geliştirme Kiti (SDK), Dart kodunun komut satırı arabiriminde çalışmasına izin veren bağımsız bir Dart VM ile birlikte gelir. Dart, kullanıcıların tamamen işlevsel uygulamalar yazmasına izin veren eksiksiz bir standart kitaplıkla birlikte gelir.
- **Önceden derlenmiş (AOT)**:</br> Dart kodu, mobil uygulamaların Flutter ile oluşturulmasına izin veren makine koduna AOT derlenebilir.
- **Yerli**:</br> Dart2native derleyici ile Dart kodu, Windows, Linux ve macOS üzerinde çalışabilen bağımsız yürütülebilir dosyalara derlenebilir.

## Dart Dosya Biçimi ##

Dart, arabirimleri, karışımları, soyut sınıfları, birleştirilmiş jenerikleri ve tür arabirimini destekleyen C stili nesne yönelimli bir dildir.

### Sözdizimi ###

Aşağıda, Dart sözdiziminin bazı örnekleri verilmiştir.

#### Konsola Yazdır ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Döngüler ve Diziler ####

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

#### İşlevler ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Sınıflar ####

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

#### Karışımlar ####

Karışımlar, yöntemleri/değişkenleri miras almadan ödünç alabildiğimiz normal sınıflardır. Bu, *"with"* anahtar sözcüğü kullanılarak yapılır.

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

## Referanslar ##

- [Dart (programlama dili) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

