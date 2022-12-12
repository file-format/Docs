{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Sổ tay Unix",
  "description":"Tìm hiểu về định dạng tệp FODT và API có thể tạo và mở tệp MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Tệp MAN là gì?

Một tệp có phần mở rộng .man là viết tắt của trang man, đây là hướng dẫn sử dụng lập trình Unix ở dạng tài liệu phần mềm. Nó được sử dụng bởi tiện ích `Man`, có trong Unix, được sử dụng để xem tài liệu. Tài liệu phần mềm chứa thông tin trong các phần và trang có thể được truy xuất bằng tiện ích Man từ thiết bị đầu cuối lệnh bằng cách đưa ra các lệnh. Có sẵn trong máy tính dưới dạng bản mềm của tài liệu, nó không yêu cầu bất kỳ bản in hoặc kết nối internet nào để truy cập nó.

## Hướng dẫn sử dụng Unix Man File Format - Thông tin thêm

Các trang hướng dẫn được lưu trữ ở định dạng văn bản thuần túy và có thể được tạo và mở trong bất kỳ trình soạn thảo văn bản nào để xem hoặc chỉnh sửa. Trong UNIX, thông tin từ các trang Man được lấy ra bằng cách đưa ra các lệnh từ thiết bị đầu cuối bao gồm tham chiếu đến phần và số trang từ sổ tay.

### Mục và Trang

Unix man là hướng dẫn sử dụng của hệ thống trong đó mỗi đối số trang cho lệnh đề cập đến tên của chương trình, tiện ích hoặc chức năng. lệnh, nếu được cung cấp thông tin phần, sẽ tìm kiếm trang trong phần cụ thể đó. Tuy nhiên, hành vi mặc định là tìm kiếm trang trong tất cả các phần và hiển thị trang đầu tiên bất kể trang đó có tồn tại trong nhiều phần hay không.

### Số Phần

Sau đây là thông tin về số phần của sách hướng dẫn, tiếp theo là các loại trang chứa trong đó.

|Số mục|Loại trang|
---|---|
|1|Chương trình thực thi hoặc lệnh shell|
|2|Các lệnh gọi hệ thống (các chức năng do kernel cung cấp)|
|3|Gọi thư viện (chức năng trong thư viện chương trình)|
|4|Các tập tin đặc biệt (thường được tìm thấy trong /dev)|
|5|Định dạng và quy ước tệp, ví dụ /etc/passwd|
|6|Trò chơi|
|7|Khác (bao gồm các gói macro và quy ước), ví dụ: man(7), groff(7)|
|8|Các lệnh quản trị hệ thống (thường chỉ dành cho root)|
|9|Lện trình hạt nhân [Không chuẩn]|

## Ví dụ - Cách đọc trang MAN?

Dưới đây là một ví dụ về cách truy xuất thông tin về lệnh MkDir bằng lệnh Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Người giới thiệu

* [Thông số Kỹ thuật OpenDocument - Theo Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specution)
* [man(1) — Trang hướng dẫn sử dụng Linux](https://man7.org/linux/man-pages/man1/man.1.html)

