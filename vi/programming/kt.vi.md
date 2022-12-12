---
date: 2019-10-11
keywords: kt, .kt, định dạng file kotlin, cách mở file kotlin, cách chạy file kotlin, định dạng file .kt, file kt , đuôi file kotlin, phần mở rộng .kt, kotlin vs java
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp KT
linktitle: KT
description: "Tìm hiểu về định dạng tệp KT và các API có thể tạo và mở tệp KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Tệp KT là gì? ##

Mã nguồn được viết bằng Kotlin được lưu với phần mở rộng .kt thường được gọi là **phần mở rộng tệp Kotlin**. Kotlin là ngôn ngữ lập trình đa nền tảng có mục đích chung do JetBrains phát triển để có thể tương thích hoàn toàn với [Java](/vi/programming/java/). Thương hiệu Kotlin được bảo vệ bởi Kotlin Foundation.

Kotlin đã được Google công bố là ngôn ngữ lập trình ưa thích để phát triển Ứng dụng Android vào ngày 7 tháng 5 năm 2019. Android Studio 3.0 bắt đầu hỗ trợ Kotlin như một giải pháp thay thế cho phát triển Ứng dụng Android vào tháng 10 năm 2017.

## Sơ lược về lịch sử định dạng tệp Kotlin KT##

Kotlin đã được JetBrains tiết lộ vào tháng 7 năm 2011 như một ngôn ngữ lập trình mới cho JVM. Trưởng nhóm JetBrains Dmitry Jemerov nói rằng hầu hết các ngôn ngữ đều thiếu các tính năng mà họ đang tìm kiếm ngoại trừ Scala nhưng việc biên dịch Scala chậm là một nhược điểm. Một trong những mục tiêu chính của Kotlin là biên dịch nhanh như Java. Dự án Kotlin có mã nguồn mở theo Giấy phép Apache 2 vào tháng 2 năm 2012.

Phiên bản 1.0 của Kotlin được phát hành vào ngày 15 tháng 2 năm 2015. Android đã công bố hỗ trợ hạng nhất cho Kotlin trên Android tại Google I/O 2017. Kotlin 1.2 được phát hành vào ngày 28 tháng 11 năm 2017 với khả năng chia sẻ mã giữa các nền tảng JVM và JavaScript. Kotlin 1.3 được phát hành vào ngày 29 tháng 10 năm 2018 với sự hỗ trợ cho lập trình không đồng bộ. Google đã công bố Kotlin là ngôn ngữ lập trình ưa thích để phát triển Ứng dụng Android vào ngày 7 tháng 5 năm 2019. Kotlin 1.4 được phát hành vào tháng 8 năm 2020 với một số thay đổi nhỏ để hỗ trợ khả năng tương tác với Swift/Objective-C.

## Cú pháp Kotlin ##

Kotlin được thiết kế để trở nên tốt hơn Java nhưng vẫn có thể tương thích với mã Java để cho phép di chuyển dần dần từ Java sang Kotlin.

* Dấu chấm phẩy là tùy chọn trong Kotlin. Một dòng mới là đủ để chỉ ra phần cuối của câu lệnh.
* Kotlin hỗ trợ hai loại biến, chỉ đọc, được xác định bởi từ khóa *val* và có thể thay đổi, được xác định bởi từ khóa *var*.
* Các lớp học là riêng tư và cuối cùng theo mặc định. Để dẫn xuất từ một lớp, lớp cơ sở phải được khai báo bằng từ khóa *open*.
* Kotlin cũng hỗ trợ lập trình thủ tục.
* Điểm vào chương trình Kotlin là chức năng "chính" tương tự như Java, C#, v.v.

### Ví dụ cú pháp ###

Sau đây là một ví dụ về cú pháp Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Trong đoạn mã trên, từ khóa **fun** xác định hàm có tên main. Bên trong hàm, một biến chỉ đọc 'khán giả' được khai báo bằng từ khóa **val**. Bằng cách sử dụng phương pháp **println**, "Xin chào thế giới từ Kotlin" được in trên bảng điều khiển. Giá trị của biến đối tượng được thêm vào chuỗi bằng dấu **$**.

## Kotlin so với Java
Kotlin là ngôn ngữ chính thức để viết các ứng dụng Android với nhiều tính năng nâng cao, nhưng nhiều nhà phát triển Java chuyên nghiệp vẫn không thể hiện sự quan tâm của họ để chuyển sang Kotlin. Họ nghĩ rằng họ có thể làm tất cả chỉ với Java. Vì vậy, sau đây là sự so sánh giữa hai công nghệ có thể thuyết phục các nhà phát triển java chuyển đổi:

| Thông số | Java | Kotlin |
|---------|------|---------------- -|
| Đối tượng Singletons | √ | √ |
| Các loại ký tự đại diện | √ | Χ |
| Biên soạn | Mã byte | Máy ảo |
| Biểu thức Lambda | Χ | √ |
| Mảng bất biến | Χ | √ |
| Ruộng Non | √ | Χ |
| Diễn viên thông minh | Χ | √ |
| Không an toàn | Χ | √ |
| Thành viên tĩnh | √ | Χ |

## Người giới thiệu ##

- [Kotlin (ngôn ngữ lập trình) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

