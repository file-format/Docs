---
date: 2019-10-11
keywords: dart, .dart, dart file format, dart file, how to run dart files, .dart extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dفرم فایل هنریat
linktitle: Dart
description: Lدر مورد فرمت فایل Dart و APIهایی که می توانند فایل Dart را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## فایل دارت چیست؟ ##

یک فایل دارت حاوی کد منبع زبان برنامه نویسی دارت است که یک زبان برنامه نویسی بهینه شده برای کلاینت است که توسط گوگل توسعه یافته و برای ساخت برنامه های موبایل، دسکتاپ، وب، آیوت (اینترنت اشیا) و غیره استفاده می شود. دارت یک زبان شی گرا است. با نحوی شبیه به C. Dart را می توان به کد جاوا اسکریپت یا کد بومی کامپایل کرد. می‌توانید فایل‌های Dart را در مرورگر وب معروف اجرا کنید، همانطور که می‌توانید یک فایل جاوا اسکریپت را اجرا کنید. یک ابزار خط فرمان معروف به ماشین مجازی Dart که با Dart SDK می‌آید نیز برای کامپایل و اجرای فایل‌های Dart استفاده می‌شود.

## تاریخچه مختصر ##

The Dart project was founded by Lars Bak and Kasper Lund and the first version was released on 14th November 2013. من در ابتدا Dart به دلیل چندپارگی وب به دلیل برنامه ریزی برای گنجاندن Dart VM در Google Chrome مورد انتقاد قرار گرفت. این برنامه ها کنار گذاشته شدند و دارت با انتشار نسخه 1.9 در سال 2015 بر روی کامپایل کردن به جاوا اسکریپت تمرکز کرد.

Dart 2.0 در آگوست 2018 منتشر شد که در آن پسوند dart2native معرفی شد که کد Dart را برای پلتفرم های بومی لینوکس، ویندوز و macOS کامپایل می کرد. این افزونه فایل‌های اجرایی مستقل را فعال می‌کند، به همین دلیل Dart SDK برای اجرای برنامه‌های Dart در آن پلتفرم‌ها مورد نیاز نبود. این افزونه همچنین با Flutter ادغام شده و امکان ایجاد برنامه های چند پلتفرمی را فراهم می کند.

ECMA دارت را با اولین نسخه در جولای 2014 و نسخه دوم در دسامبر 2014 استاندارد کرد.


## نحوه اجرا/اجرا کردن کد دارت ##

کد دارت می تواند به روش های زیر اجرا شود:

- **کامپایل شده به صورت جاوا اسکریپت**:</br> کد Dart با استفاده از کامپایلر dart2js به جاوا اسکریپت کامپایل می شود. کد جاوا اسکریپت کامپایل شده با تمام مرورگرهای وب اصلی سازگار است.
- **مستقل **:</br> کیت توسعه نرم‌افزار دارت (SDK) با یک Dart VM مستقل عرضه می‌شود که به کد دارت اجازه می‌دهد در رابط خط فرمان اجرا شود. دارت با یک کتابخانه استاندارد کامل عرضه می شود که به کاربران امکان می دهد برنامه های کاملاً کاربردی بنویسند.
- **پیش از زمان (AOT) گردآوری شده**:</br> کد دارت را می توان با AOT در کد ماشین کامپایل کرد که به برنامه های تلفن همراه اجازه می دهد با فلاتر ساخته شوند.
- **بومی**:</br> با کامپایلر dart2native، کد Dart را می توان به فایل های اجرایی مستقلی که می توانند روی ویندوز، لینوکس و macOS اجرا شوند، کامپایل کرد.

## فرمت فایل دارت ##

دارت یک زبان شی گرا به سبک C است که از رابط ها، میکسین ها، کلاس های انتزاعی، ژنریک های اصلاح شده و رابط نوع پشتیبانی می کند.

### نحو ###

در زیر چند نمونه از نحو دارت آورده شده است.

#### چاپ در کنسول ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### حلقه ها و آرایه ها ####

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

#### کارکرد ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### کلاس ها ####

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

#### ترکیبات ####

Mixinها کلاس‌های عادی هستند که می‌توانیم متدها/متغیرها را بدون به ارث بردن آنها قرض کنیم. این کار با استفاده از کلمه کلیدی *با* انجام می شود.

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

## منابع ##

- [Dart (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

