---
date: 2019-10-11
keywords: dart, .dart, định dạng file dart, file dart, cách chạy file dart, đuôi .dart
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp phi tiêu
linktitle: Dart
description: "Tìm hiểu về định dạng tệp Dart và các API có thể tạo và mở tệp Dart."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Tệp phi tiêu là gì? ##

Tệp Dart chứa mã nguồn của ngôn ngữ lập trình Dart, ngôn ngữ lập trình được tối ưu hóa cho máy khách do Google phát triển, được sử dụng để xây dựng ứng dụng cho thiết bị di động, máy tính để bàn, web, Iot (Internet vạn vật), v.v. Dart là ngôn ngữ hướng đối tượng với cú pháp tương tự như C. Dart có thể được biên dịch thành JavaScript hoặc mã gốc. Bạn có thể chạy các tệp Dart trong trình duyệt web nổi tiếng giống như bạn có thể chạy tệp javascript. Một công cụ dòng lệnh được gọi là máy ảo Dart đi kèm với SDK Dart cũng có thể được sử dụng để biên dịch và chạy các tệp Dart.

## Lược Sử ##

Dự án Dart được thành lập bởi Lars Bak và Kasper Lund và phiên bản đầu tiên được phát hành vào ngày 14 tháng 11 năm 2013. Lúc đầu, Dart đã bị chỉ trích vì sự phân mảnh web do kế hoạch đưa Dart VM vào Google Chrome. Những kế hoạch đó đã bị hủy bỏ và Dart tập trung vào việc biên dịch thành JavaScript với việc phát hành phiên bản 1.9 vào năm 2015.

Dart 2.0 được phát hành vào tháng 8 năm 2018, trong đó tiện ích mở rộng dart2native được giới thiệu để biên dịch mã Dart cho các nền tảng Linux, Windows, macOS gốc. Tiện ích mở rộng này đã kích hoạt các tệp thực thi độc lập do đó SDK Dart không bắt buộc phải chạy các ứng dụng Dart trên các nền tảng đó. Tiện ích mở rộng này cũng được tích hợp với Flutter để có thể tạo các ứng dụng đa nền tảng.

ECMA chuẩn hóa Dart với phiên bản đầu tiên vào tháng 7 năm 2014 và phiên bản thứ hai vào tháng 12 năm 2014.


## Cách chạy/thực thi mã Dart ##

Mã phi tiêu có thể chạy theo các cách sau:

- **Biên dịch dưới dạng JavaScript**:</br> Mã Dart được biên dịch sang JavaScript bằng cách sử dụng trình biên dịch dart2js. Mã JavaScript được biên dịch tương thích với tất cả các trình duyệt web chính.
- **Độc lập**:</br> Bộ công cụ phát triển phần mềm Dart (SDK) đi kèm với Dart VM độc lập cho phép mã Dart chạy trong giao diện dòng lệnh. Dart cung cấp một thư viện tiêu chuẩn hoàn chỉnh cho phép người dùng viết các ứng dụng đầy đủ chức năng.
- **Trước thời hạn (AOT) được biên dịch**:</br> Mã phi tiêu có thể được biên dịch AOT thành mã máy cho phép xây dựng ứng dụng di động bằng Flutter.
- **Tự nhiên**:</br> Với trình biên dịch dart2native, mã Dart có thể được biên dịch thành các tệp thực thi độc lập có thể chạy trên Windows, Linux và macOS.

## Định dạng tệp phi tiêu ##

Dart là ngôn ngữ hướng đối tượng kiểu C hỗ trợ giao diện, mixin, lớp trừu tượng, tổng quát thống nhất và giao diện kiểu.

### Cú pháp ###

Sau đây là một số ví dụ về cú pháp Dart.

#### In ra Bảng điều khiển ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Vòng lặp và Mảng ####

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

#### Chức năng ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Các lớp học ####

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

#### Hỗn hợp ####

Mixins là các lớp thông thường mà từ đó chúng ta có thể mượn các phương thức/biến mà không cần kế thừa chúng. Điều này được thực hiện bằng cách sử dụng từ khóa *"with"*.

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

## Người giới thiệu ##

- [Phi tiêu (ngôn ngữ lập trình) - Wikipedia](https://vi.wikipedia.org/wiki/Dart_(programming_language))
- [Phi tiêu](https://dart.dev/)

