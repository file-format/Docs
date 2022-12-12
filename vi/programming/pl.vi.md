{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "tệp", "phần mở rộng", "định dạng", "Perl", "ngôn ngữ Perl", "tệp PL", "lập trình"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp PL và các API có thể tạo và mở tệp PL.",
  "title" :"Tệp PL - Định dạng tệp tập lệnh Perl",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## Tệp PL là gì?

Tệp có phần mở rộng .pl là tệp Perl Script là ngôn ngữ kịch bản. Chúng được biên dịch và chạy bằng phần mềm Phiên dịch Perl. Tệp tập lệnh PL chứa các dòng mã, biến và nhận xét. Ngôn ngữ kịch bản tương đối khó
hiểu các định dạng tệp lập trình khác, chẳng hạn như [PHP](/vi/programming/php/). Các tệp PL có thể được tạo và tương thích với Windows, macOS và Linux.

## Tóm tắt lịch sử ngôn ngữ kịch bản Perl

Ngôn ngữ này lần đầu tiên được sử dụng vào năm 1987, vì vậy những tệp này có nguồn gốc từ năm đó. Năm 1989 Perl 2 được phát hành. Sau đó, nó đã được cập nhật và sửa đổi cho đến phiên bản 5.35 và phiên bản tiếp theo dự kiến sẽ được phát hành vào năm tới.

Trong mọi bản cập nhật, đã có thêm các công cụ về chức năng, hiệu suất và giao diện của ngôn ngữ và tệp. Đã có nhiều sửa đổi về các phiên bản trong những năm này. Ban đầu nó là một ngôn ngữ kịch bản cơ bản nhưng bây giờ nó cũng bao gồm nhiều mô-đun khác. Ban đầu, nó là một ngôn ngữ rất đơn giản, nhưng các chữ viết của ngôn ngữ này khá khó hiểu vì chúng nhỏ gọn.

## Thông số kỹ thuật tiện ích mở rộng định dạng tệp Perl

Có một số thuộc tính hoặc thông số kỹ thuật của các tệp lập trình này, một số thuộc tính như sau:

* Mã có trong các tệp này ở định dạng văn bản thuần túy và được sử dụng để phát triển tập lệnh
* Tập lệnh của máy chủ, phân tích cú pháp văn bản và quản trị máy chủ là những khía cạnh chính mà tập lệnh của ngôn ngữ này bao gồm
* Nhiều chương trình phổ biến được liên kết với ngôn ngữ này là Trạng thái hoạt động Active Perl và Bare Bones BBEdit (tương thích với Mac OS)
* Ngôn ngữ này được coi là ngôn ngữ cấp cao
* Đối với Win32, người dùng có thể phải cài đặt bản phân phối nhị phân gốc của ngôn ngữ
* Nó yêu cầu một số công cụ viết kịch bản để có thể thực thi được trong các Bộ tài nguyên Windows khác nhau
* Visual Studio .NET là một framework nổi tiếng để phát triển các ngôn ngữ lập trình. Công cụ Trạng thái hoạt động được gọi là Visual Perl được sử dụng để thêm Perl vào Visual studio
* Trong các tệp, dòng đầu tiên của mã nguồn mô tả thông tin của trình thông dịch đang được sử dụng. Các tệp PL thường bắt đầu bằng dòng **#!/usr/bin/perl** cho phép máy tính của bạn chạy tập lệnh này bằng trình thông dịch Perl được cài đặt trong máy tính


## Ví dụ về tập lệnh PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

Điều này sẽ in

```
Hello, World
```

### Nhận xét một dòng ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Bình luận nhiều dòng ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Phép gán biến ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Phép gán biến vô hướng ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Các phép toán vô hướng đơn giản ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Người giới thiệu ##

- [Python (ngôn ngữ lập trình) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

