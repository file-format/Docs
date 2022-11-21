---
date: 2019-10-11
keywords: dart, .dart, รูปแบบไฟล์ dart, ไฟล์ dart, วิธีรันไฟล์ dart, นามสกุล .dart,
ผู้เขียน:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: รูปแบบไฟล์โผ,
linktitle: Dart
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ Dart และ API ที่สามารถสร้างและเปิดไฟล์ Dart"
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## ไฟล์ Dart คืออะไร? ##

ไฟล์ Dart มีซอร์สโค้ดของภาษาโปรแกรม Dart ซึ่งเป็นภาษาโปรแกรมที่ปรับให้เหมาะกับไคลเอ็นต์ที่พัฒนาโดย Google ซึ่งใช้สร้างแอปสำหรับมือถือ เดสก์ท็อป เว็บ Iot (Internet of Things) เป็นต้น Dart เป็นภาษาเชิงวัตถุ ด้วยไวยากรณ์ที่คล้ายกับ C Dart สามารถคอมไพล์เป็น JavaScript หรือโค้ดเนทีฟ คุณสามารถเรียกใช้ไฟล์ Dart ในเว็บเบราว์เซอร์ที่มีชื่อเสียงได้เช่นเดียวกับที่คุณเรียกใช้ไฟล์จาวาสคริปต์ เครื่องมือบรรทัดคำสั่งที่เรียกว่า Dart virtual machine ซึ่งมาพร้อมกับ Dart SDK สามารถใช้เพื่อคอมไพล์และเรียกใช้ไฟล์ Dart

## ประวัติย่อ ##

โครงการ Dart ก่อตั้งโดย Lars Bak และ Kasper Lund และเปิดตัวเวอร์ชันแรกเมื่อวันที่ 14 พฤศจิกายน 2013 ฉันเริ่ม Dart ถูกวิพากษ์วิจารณ์เรื่องการกระจายตัวของเว็บเนื่องจากแผนการรวม Dart VM ใน Google Chrome แผนเหล่านั้นถูกยกเลิกและ Dart มุ่งเน้นไปที่การคอมไพล์เป็น JavaScript ด้วยการเปิดตัวเวอร์ชัน 1.9 ในปี 2558

Dart 2.0 เปิดตัวในเดือนสิงหาคม 2018 โดยมีการเปิดตัวส่วนขยาย dart2native ที่คอมไพล์รหัส Dart ไปยังแพลตฟอร์ม Linux, Windows, macOS ดั้งเดิม ส่วนขยายนี้เปิดใช้โปรแกรมปฏิบัติการที่มีในตัวเอง เนื่องจากไม่จำเป็นต้องใช้ Dart SDK เพื่อเรียกใช้แอป Dart บนแพลตฟอร์มเหล่านั้น ส่วนขยายนี้ยังรวมเข้ากับ Flutter ทำให้สามารถสร้างแอปข้ามแพลตฟอร์มได้

ECMA กำหนดมาตรฐาน Dart โดยพิมพ์ครั้งแรกในเดือนกรกฎาคม 2014 และพิมพ์ครั้งที่ 2 ในเดือนธันวาคม 2014


## วิธีรัน/รันโค้ด Dart ##

รหัส Dart สามารถเรียกใช้ได้ด้วยวิธีต่อไปนี้:

- **รวบรวมเป็น JavaScript**:</br> โค้ด Dart ถูกคอมไพล์เป็น JavaScript โดยใช้คอมไพเลอร์ dart2js โค้ด JavaScript ที่คอมไพล์แล้วเข้ากันได้กับเว็บเบราว์เซอร์หลักๆ ทั้งหมด
- **สแตนด์อโลน**:</br> Dart Software Development Kit (SDK) มาพร้อมกับ Dart VM แบบสแตนด์อโลนที่อนุญาตให้รันโค้ด Dart ในอินเทอร์เฟซบรรทัดคำสั่ง Dart มาพร้อมกับไลบรารีมาตรฐานที่สมบูรณ์ซึ่งช่วยให้ผู้ใช้สามารถเขียนแอปที่ทำงานได้อย่างสมบูรณ์
- **รวบรวมล่วงหน้า (AOT)**:</br> รหัส Dart สามารถคอมไพล์ AOT เป็นรหัสเครื่องที่อนุญาตให้สร้างแอพมือถือด้วย Flutter
- **พื้นเมือง**:</br> ด้วยคอมไพเลอร์ dart2native ทำให้สามารถคอมไพล์โค้ด Dart เป็นไฟล์ปฏิบัติการที่มีในตัวเองซึ่งสามารถทำงานบน Windows, Linux และ macOS

## รูปแบบไฟล์โผ ##

Dart เป็นภาษาเชิงวัตถุสไตล์ C ที่รองรับอินเทอร์เฟซ มิกซ์อิน คลาสนามธรรม รีไฟด์ทั่วไป และอินเทอร์เฟซประเภท

### ไวยากรณ์ ###

ต่อไปนี้เป็นตัวอย่างบางส่วนของไวยากรณ์ Dart

#### พิมพ์ไปที่คอนโซล ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### ลูปและอาร์เรย์ ####

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

#### ฟังก์ชั่น ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### ชั้นเรียน ####

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

#### มิกซ์อิน ####

มิกซ์อินเป็นคลาสปกติที่เราสามารถยืมเมธอด/ตัวแปรได้โดยไม่ต้องสืบทอด สิ่งนี้ทำได้โดยใช้คีย์เวิร์ด *"กับ"*

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

## อ้างอิง ##

- [Dart (ภาษาโปรแกรม) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [โผ](https://dart.dev/)

