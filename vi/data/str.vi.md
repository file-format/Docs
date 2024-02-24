{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Tệp STR - Tệp đối tượng danh sách cấu trúc dBASE - Tệp .str là gì và làm cách nào để mở tệp?",
  "description" : "Tìm hiểu về Tệp đối tượng danh sách cấu trúc STR dBASE và cách mở tệp đó.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-vi",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Tập tin STR là gì?

Định dạng tệp STR thường được liên kết với dBASE, một hệ thống quản lý cơ sở dữ liệu. Trong dBASE, tệp .str thường đại diện cho tệp đối tượng danh sách cấu trúc. Tệp này chứa cấu trúc của bảng cơ sở dữ liệu, bao gồm thông tin về các trường (cột) và thuộc tính của chúng.

Tệp đối tượng danh sách cấu trúc (.str) chứa siêu dữ liệu như tên trường, kiểu dữ liệu, độ dài trường và bất kỳ thuộc tính nào khác được liên kết với từng trường trong bảng cơ sở dữ liệu. Nó được sử dụng để xác định cấu trúc của bảng cơ sở dữ liệu mà không chứa các bản ghi dữ liệu thực tế.

Các chương trình như dBASE hoặc các công cụ quản lý cơ sở dữ liệu khác có thể sử dụng tệp này để hiểu cách bố trí bảng cơ sở dữ liệu và thực hiện các thao tác như truy vấn, cập nhật hoặc tạo bản ghi mới dựa trên cấu trúc này.

Đây là một ví dụ cơ bản về nội dung tệp STR có thể chứa:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Ví dụ này mô tả một bảng có bốn trường: ID, Name, Age và DOB, cùng với kiểu dữ liệu và độ dài tương ứng của chúng.

## Làm cách nào để mở tập tin STR?

Cách chính để mở tệp .str là sử dụng chính dBASE, đặc biệt là trên hệ điều hành Windows. dBASE có khả năng đọc và giải thích nội dung của các tệp này, cho phép người dùng xem và làm việc với cấu trúc cơ sở dữ liệu.

Vì tệp .str về cơ bản là các tệp văn bản thuần túy chứa thông tin về cấu trúc cơ sở dữ liệu nên bạn cũng có thể mở chúng bằng trình soạn thảo văn bản. Ví dụ về trình soạn thảo văn bản bao gồm Microsoft Notepad trên Windows và Apple TextEdit trên Mac. Khi mở bằng trình soạn thảo văn bản, bạn sẽ có thể xem nội dung của tệp, bao gồm tên trường, loại dữ liệu và thông tin cấu trúc khác ở định dạng mà con người có thể đọc được.

## Người giới thiệu
* [dBase](https://en.wikipedia.org/wiki/DBase)


