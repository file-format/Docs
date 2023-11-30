{
"ngày": "2023-03-07",
  "keywords": [
"tệp reg",
"tệp reg là gì",
"tài liệu",
"phần mở rộng tập tin reg",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp REG - Tệp đăng ký Windows",
  "description":"Tìm hiểu về định dạng REG và các API có thể tạo và mở tệp REG.",
"linktitle":"REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
      "parent": "system"
}
},
"lastmod": "2023-03-07"
}

## Tập tin REG là gì?

Tệp REG là định dạng tệp được sử dụng để nhập hoặc xuất dữ liệu Windows Reg. Windows Sổ đăng ký là cơ sở dữ liệu phân cấp lưu trữ các tùy chọn và cài đặt cấu hình cho hệ điều hành Windows và các ứng dụng đã cài đặt. Sổ đăng ký chứa thông tin như tùy chọn người dùng, cài đặt ứng dụng, dữ liệu cấu hình phần cứng và phần mềm, v.v.

Tệp REG thường có phần mở rộng tệp ".reg" và là tệp văn bản thuần túy chứa một loạt mục nhập và giá trị đăng ký ở định dạng cụ thể. Định dạng này bao gồm phần tiêu đề xác định tệp là tệp đăng ký, theo sau là một loạt các cặp khóa và giá trị đại diện cho các mục đăng ký.

## Định dạng tệp REG - Thông tin thêm

Đây là một ví dụ về định dạng tệp reg:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Dòng đầu tiên của tệp chỉ định phiên bản của trình chỉnh sửa sổ đăng ký. Các dòng sau chứa các mục đăng ký ở định dạng đường dẫn chính, theo sau là tên giá trị và dữ liệu giá trị. Trong ví dụ này, tệp reg chứa hai mục: một mục thêm chương trình có tên "Example.exe" vào danh sách khởi động Windows và một mục khác đặt giá trị "Ẩn" trong cài đặt nâng cao của Windows Explorer thành "true".

Các tệp Reg có thể được tạo và chỉnh sửa bằng trình soạn thảo văn bản như Notepad. Chúng thường được sử dụng cho mục đích sao lưu và khôi phục cũng như để định cấu hình nhiều máy tính có cùng cài đặt đăng ký.

## Nhập hoặc xuất sổ đăng ký Windows

Tệp REG là loại tệp được sử dụng để nhập hoặc xuất dữ liệu từ Windows Register. Windows Sổ đăng ký là cơ sở dữ liệu phân cấp lưu trữ các tùy chọn và cài đặt cấu hình cho hệ điều hành Windows và các ứng dụng đã cài đặt. Sổ đăng ký chứa thông tin như tùy chọn người dùng, cài đặt ứng dụng, dữ liệu cấu hình phần cứng và phần mềm, v.v.

Các tệp Reg có thể được sử dụng để tạo hoặc sửa đổi các mục đăng ký và chúng thường được sử dụng cho mục đích sao lưu và khôi phục cũng như để định cấu hình nhiều máy tính có cùng cài đặt đăng ký. Dưới đây là cách sử dụng tệp reg để thêm mục đăng ký mới vào Sổ đăng ký Windows:

1. Tạo tệp văn bản mới bằng trình soạn thảo văn bản như Notepad.
2. Nhập mục đăng ký theo đúng định dạng. Định dạng này bao gồm phần tiêu đề xác định tệp là tệp đăng ký, theo sau là một loạt các cặp khóa và giá trị đại diện cho các mục đăng ký. Đây là một ví dụ:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Thao tác này sẽ tạo một khóa mới có tên là "Ví dụ" trong khóa "Phần mềm" trong trung tâm đăng ký của người dùng hiện tại và đặt giá trị "Cài đặt1" thành "Giá trị1".

3. Lưu tệp có phần mở rộng tệp .reg.
4. Bấm đúp vào tệp .reg để thêm mục đăng ký mới vào Windows Register.

Bạn sẽ được nhắc xác nhận rằng bạn muốn thêm mục vào sổ đăng ký. Sau khi bạn xác nhận, mục nhập mới sẽ được thêm vào sổ đăng ký và bạn có thể xác minh nó bằng công cụ Trình chỉnh sửa sổ đăng ký.

## Người giới thiệu
* [Windows Sổ đăng ký](https://en.wikipedia.org/wiki/Windows_Registry)

