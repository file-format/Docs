{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp DDL và các API có thể tạo và mở tệp DDL.",
  "title" :"Định dạng tệp DDL - Tệp ngôn ngữ định nghĩa dữ liệu",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Tập tin DDL là gì?

Tệp có phần mở rộng .ddl là tệp Ngôn ngữ định nghĩa dữ liệu được sử dụng để xác định lược đồ của cơ sở dữ liệu. Nó chứa các câu lệnh/câu lệnh để làm việc với các cấu trúc cơ sở dữ liệu như bảng, cột, bản ghi và các trường khác. Các lệnh trong tệp DDL được viết bằng [SQL](/vi/database/sql/) và có thể thực hiện các thao tác như tạo bảng trong cơ sở dữ liệu, thả và cập nhật. Lược đồ cơ sở dữ liệu được sở hữu bởi lược đồ được tạo và tất cả các thao tác CRUD có thể được thực hiện trên lược đồ đó. Các ứng dụng phổ biến có thể tạo và mở tệp DDL là Windows Text Editor, Jetbrains Intellij Idea và EclipseLink.

## lệnh DDL

Một tệp DDL duy nhất có thể chứa một số lệnh, do đúng cú pháp, sẽ thực thi theo trình tự và thực hiện các thay đổi đối với lược đồ, chẳng hạn như tạo bộ ký tự và bảng, loại bỏ bảng, đổi tên và thay đổi bảng. Các lệnh DDL sau thường được sử dụng khi làm việc với lược đồ cơ sở dữ liệu.

`CREATE` - Được sử dụng để tạo cơ sở dữ liệu hoặc các đối tượng của nó (như bảng, chỉ mục, hàm, dạng xem, thủ tục lưu trữ và trình kích hoạt).

`DROP` – Được sử dụng để xóa các đối tượng khỏi cơ sở dữ liệu.

`ALTER` - Được sử dụng để thay đổi cấu trúc của cơ sở dữ liệu.

`TRUNCATE` – Được sử dụng để xóa tất cả các bản ghi khỏi một bảng, bao gồm tất cả các khoảng trắng được phân bổ cho các bản ghi bị xóa.

`BÌNH LUẬN` – Thêm nhận xét vào từ điển dữ liệu.

`RENAME` – Đổi tên một đối tượng hiện có trong cơ sở dữ liệu.

## Ví dụ DDL

Ví dụ sau đây cho thấy câu lệnh DDL cho lệnh CREATE tạo bảng và xác định các trường của bảng.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Người giới thiệu ##

* [DDL của Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

