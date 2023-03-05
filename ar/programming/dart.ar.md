---
date: 2019-10-11
keywords: dart, .dart, dart file format, dart file, how to run dart files, dart extension
مؤلف:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: تنسيق ملف دارت
linktitle: Dart
description: "تعرف على تنسيق ملف Dart وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات Dart وفتحها."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## ما هو ملف دارت؟ ##

يحتوي ملف Dart على الكود المصدري للغة برمجة Dart وهي لغة برمجة محسّنة للعميل تم تطويرها بواسطة Google وتستخدم لإنشاء تطبيقات للجوال وسطح المكتب والويب و Iot (إنترنت الأشياء) وما إلى ذلك. Dart هي لغة موجهة للكائنات مع بناء جملة مشابه لـ C. Dart يمكن تجميعها إما إلى JavaScript أو إلى كود أصلي. يمكنك تشغيل ملفات Dart في متصفح الويب الشهير تمامًا كما يمكنك تشغيل ملف javascript. يمكن أيضًا استخدام أداة سطر الأوامر المعروفة باسم Dart virtual machine التي تأتي مع Dart SDK لتجميع ملفات Dart وتشغيلها.

## نبذة تاريخية ##

تم تأسيس مشروع Dart بواسطة Lars Bak و Kasper Lund وتم إصدار الإصدار الأول في 14 نوفمبر 2013. تم انتقاد I the Begining the Dart بسبب تجزئة الويب بسبب خطط تضمين Dart VM في Google Chrome. تم إسقاط هذه الخطط وركز Dart على التحويل البرمجي إلى JavaScript مع إصدار الإصدار 1.9 في عام 2015.

تم إصدار Dart 2.0 في أغسطس 2018 حيث تم تقديم ملحق dart2native الذي قام بتجميع كود Dart لأنظمة Linux و Windows و macOS الأصلية. مكّن هذا الامتداد الملفات التنفيذية المستقلة التي لم تكن Dart SDK مطلوبة بسببها لتشغيل تطبيقات Dart في تلك الأنظمة الأساسية. تم دمج هذا الامتداد أيضًا مع Flutter مما يجعل من الممكن إنشاء تطبيقات عبر الأنظمة الأساسية.

قامت ECMA بتوحيد Dart مع الإصدار الأول في يوليو 2014 والطبعة الثانية في ديسمبر 2014.


## كيفية تشغيل / تنفيذ كود Dart ##

يمكن تشغيل كود Dart بالطرق التالية:

- ** تم تجميعه على هيئة JavaScript **:</br> يتم تجميع كود Dart إلى JavaScript باستخدام مترجم dart2js. كود JavaScript المترجم متوافق مع جميع متصفحات الويب الرئيسية.
- ** قائمة بذاتها **:</br> يتم شحن Dart Software Development Kit (SDK) مع Dart VM مستقل يسمح بتشغيل رمز Dart في واجهة سطر الأوامر. يأتي Dart مزودًا بمكتبة قياسية كاملة تتيح للمستخدمين كتابة تطبيقات تعمل بكامل طاقتها.
- ** تم تجميع قبل الوقت (AOT) **:</br> يمكن تجميع كود Dart AOT إلى كود الآلة الذي يسمح ببناء تطبيقات الأجهزة المحمولة باستخدام Flutter.
- **محلي**:</br> باستخدام المترجم dart2native ، يمكن تجميع كود Dart إلى ملفات تنفيذية قائمة بذاتها يمكن تشغيلها على أنظمة تشغيل Windows و Linux و macOS.

## تنسيق ملف dart ##

Dart هي لغة موجهة للكائنات من نمط C تدعم الواجهات ، والمزج ، والفئات المجردة ، والأدوية الموحدة ، وواجهة الكتابة.

### بناء الجملة ###

فيما يلي بعض الأمثلة على بناء جملة Dart.

#### الطباعة إلى وحدة التحكم ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### الحلقات والمصفوفات ####

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

#### المهام ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### الطبقات ####

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

#### الخلطات ####

Mixins هي فئات عادية يمكننا من خلالها استعارة الطرق / المتغيرات دون أن نرثها. يتم ذلك باستخدام الكلمة الأساسية * "مع" *.

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

## مراجع ##

- [Dart (لغة برمجة) - ويكيبيديا](https://en.wikipedia.org/wiki/Dart_ (architecture_language))
- [دارت](https://dart.dev/)

