---
date: 2019-10-11
keywords: java, .java, định dạng file java, cách mở file java, cách chạy file java, file java, java sample
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp Java
linktitle: Java
description: "Tìm hiểu về định dạng tệp Java và các API có thể tạo và mở tệp Java."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Tệp Java là gì? ##
Một tệp chứa mã nguồn Java và được lưu với phần mở rộng tệp .java được gọi là tệp Java. Java là một trong những công nghệ được sử dụng rộng rãi nhất để phát triển trò chơi, ứng dụng di động, web và máy tính để bàn. Vì Java là nền tảng độc lập nên nó hoạt động hoàn hảo trên Windows, Mac, Linux, Raspberry Pi, v.v. Java rất giống với C# và C++ nên việc chuyển đổi giữa các ngôn ngữ này sẽ dễ dàng hơn.

## Lược Sử ##

Dự án Java được khởi xướng vào tháng 6 năm 1991 bởi James Gosling, Mike Sheridan và Patrick Naughton. Java ban đầu được đặt tên là Oak. Sau đó nó được đổi tên thành Green và cuối cùng là Java. James Gosling đã thiết kế Java với cú pháp tương tự như C/C++. Phiên bản công khai đầu tiên của Java được phát hành vào năm 1996 bởi Sun Microsystems. Nó có thể chạy trên tất cả các hệ thống phổ biến khiến Java trở nên phổ biến nhanh chóng. Với việc phát hành Java 2 vào tháng 12 năm 1998, nhiều cấu hình cho các loại nền tảng khác nhau đã được xây dựng. Các phiên bản như sau

- J2EE (Java EE): Dành cho giải pháp doanh nghiệp
- J2ME (Java ME): Dành cho ứng dụng di động
- J2SE (Java SE): Dành cho ứng dụng máy tính để bàn

Vào ngày 19 tháng 11 năm 2006, Máy ảo Java (JVM) được Sun phát hành dưới dạng phần mềm mã nguồn mở và miễn phí. Sau khi Tập đoàn Oracle mua lại Sun Microsystems vào năm 2009–2010, James Gosling đã từ chức khỏi Oracle vào ngày 2 tháng 4 năm 2010.

## Cách chạy/thực thi mã Java ##

Để thực thi mã Java, nó cần được biên dịch trước. Đối với điều đó, SDK Java là bắt buộc. SDK Java biên dịch mã Java thành tệp lớp bytecode. Có các IDE như Eclipse và IntelliJ Idea giúp làm việc với các tệp Java dễ dàng hơn bằng cách cung cấp khả năng hoàn thành mã và giao diện dễ sử dụng để biên dịch và thực thi mã Java.

## Định dạng tệp Java ##

Cú pháp của Java bị ảnh hưởng nhiều bởi C và C++ nhưng không giống như C++, Java hầu như chỉ được xây dựng như một ngôn ngữ hướng đối tượng. Trong Java, tất cả mã được viết bên trong các lớp và mọi mục dữ liệu là một đối tượng. Ngược lại với C++, Java không hỗ trợ nạp chồng toán tử hoặc đa kế thừa.

### Mã mẫu Java ###

Sau đây là một ví dụ về cú pháp Java.

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
Trong đoạn mã trên, từ khóa **public** biểu thị công cụ sửa đổi quyền truy cập. Nó nói rằng lớp này có thể được truy cập bởi các lớp bên ngoài hệ thống phân cấp lớp. Công cụ sửa đổi truy cập cũng có thể là **protected** (có thể được truy cập trong cùng một gói) hoặc **private** (các phương thức chỉ có thể được truy cập bởi cùng một lớp). **static** phía trước phương thức chỉ ra rằng phương thức có thể được gọi mà không cần một thể hiện cụ thể của lớp. **void** chỉ ra rằng phương thức sẽ không trả về gì cả. Để in chuỗi ra bàn điều khiển. Lệnh system.out.println được sử dụng. Trong lệnh này, lớp *System* có một trường tĩnh *out* là một thể hiện của lớp *PrintStream* chứa phương thức *println*.

Tên tệp của các tệp Java phải giống với tên lớp. Vì vậy, tệp Java cho mã ví dụ sẽ được đặt tên là *ExampleApp.java*.

## Người giới thiệu ##

- [Java (ngôn ngữ lập trình) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

