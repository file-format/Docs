{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","tệp jar là gì","cách mở tệp jar", "phần mở rộng", "tệp", "tệp jar","định dạng tệp jar", "phần mở rộng .jar " ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Định dạng tệp lưu trữ Java",
  "description":"Tìm hiểu về định dạng tệp JAR và các API có thể tạo và mở tệp JAR.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Tệp JAR là gì?

Tệp có phần mở rộng .jar là tệp Lưu trữ Java chứa nhiều tệp liên quan đến ứng dụng khác nhau dưới dạng một tệp. Định dạng tệp này được tạo để giảm tốc độ tải Java Applet đã tải xuống trong trình duyệt thông qua giao dịch HTTP, bằng cách tránh tạo nhiều kết nối HTTP. Một tệp JAR duy nhất có thể chứa các tệp lớp Java ([.class](/vi/programming/class/)), [hình ảnh](/vi/image/) và [âm thanh](/vi/audio/). Các mục riêng lẻ bên trong tệp JAR có thể được nhà phát triển ứng dụng ký điện tử để xác thực nguồn gốc của chúng. Các tệp JAR thường được sử dụng để tạo các API chức năng chứa chức năng cụ thể liên quan đến API đó.

## Định dạng tệp JAR

Các tệp JAR dựa trên [định dạng tệp ZIP](/vi/compression/zip/) phổ biến lưu trữ các tệp nội dung riêng lẻ của nó trong một tệp duy nhất. Định dạng tệp JAR hỗ trợ nén, dẫn đến kích thước tệp nhỏ hơn để tải xuống và do đó cải thiện hơn nữa thời gian tải xuống. [Thông số kỹ thuật của tệp JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) của Oracle cung cấp chi tiết đầy đủ về các thông số kỹ thuật bên trong của tệp JAR.

### Tệp kê khai

Khi một tệp JAR được tạo, một tệp kê khai sẽ tự động được tạo bên trong tệp chứa thông tin siêu dữ liệu về nội dung của tệp JAR. Tệp này hiển thị nội dung được đóng gói bên trong tệp JAR. Một tệp Manifest điển hình trông như sau, hiển thị các thư mục và lớp có trong tệp JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Thông số kê khai

Thông số kỹ thuật của tệp kê khai được định nghĩa bởi Oracle như sau.

`tệp kê khai`: dòng mới của phần chính \*phần riêng lẻ

`phần chính`: dòng mới thông tin phiên bản \*thuộc tính chính

`thông tin phiên bản`: Manifest-Version : số phiên bản

`phiên bản-số` : chữ số+{.chữ số+}*

`thuộc tính chính`: (bất kỳ thuộc tính chính hợp pháp nào) dòng mới

`mục cá nhân`: Tên : giá trị dòng mới \*perentry-attribute

`perentry-attribute`: (bất kỳ thuộc tính perentry hợp lệ nào) dòng mới

`dòng mới` : CR LF | LF | CR (không theo sau bởi LF)

`digit`: {0-9}

### JAR thực thi

Các tệp JAR cũng có thể bao gồm một ứng dụng có thể được thực thi bởi Máy ảo Java (JVM) tương tự như bất kỳ ứng dụng nào khác trên Hệ điều hành Microsoft Windows. Trong trường hợp này, JVM cần biết về điểm vào của ứng dụng là bất kỳ lớp nào có phương thức chính public static void. Tệp kê khai xác định một lớp như vậy với tiêu đề `Lớp chính` theo định dạng sau:

```
Main-Class: com.example.MyClassName
```



## Người giới thiệu

* [Tổng quan về tệp JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [Định dạng tệp JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

