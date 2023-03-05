{
  "date" : "2021-08-02",
  "keywords" :[ "tệp reg", "định dạng tệp reg", "tệp reg là gì", "tệp", "ví dụ reg", "phần mở rộng tệp reg","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp REG và API có thể tạo và mở tệp REG.",
  "title" :"REG - Tệp đăng ký Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Tệp REG là gì?
Tệp REG chỉ đơn giản là một tệp văn bản có phần mở rộng .reg. Các tệp này thường được tạo bằng cách xuất các khóa điển hình từ Sổ đăng ký. Các tệp này cũng có thể được sử dụng làm bản sao lưu của sổ đăng ký (Đặc biệt bước này rất quan trọng trước khi thực hiện thay đổi!). Bạn có thể thấy rằng một số đã cung cấp chúng dưới dạng tệp có thể tải xuống trên cùng một trang web chỉ cho bạn cách thực hiện hack Registry. Tệp REG rất hữu ích trong việc thực hiện các thay đổi thủ công đối với Sổ đăng ký và xuất những thay đổi đó. Chỉ cần làm sạch các tập tin một chút và sau đó chia sẻ nó với những người khác.

## Định dạng tệp REG
Định dạng tệp REG được thiết kế để xuất và nhập các phần của sổ đăng ký Windows bằng cú pháp dựa trên INI. Windows Registry là một cơ sở dữ liệu quan hệ hoặc phân cấp giữ cài đặt cấp thấp cho hệ điều hành Microsoft Windows và các ứng dụng khác sử dụng sổ đăng ký Windows. Ngoài ra, có thể nói, sổ đăng ký hoặc Windows Registry bao gồm thông tin, tùy chọn, cài đặt và các giá trị khác cho các chương trình và phần cứng được cài đặt trên tất cả các phiên bản của hệ điều hành Microsoft Windows.
### Cú pháp của tệp REG
Dưới đây là một số yếu tố chính như là một phần của cú pháp tệp REG:
- **RegistryEditorVersion**: Ví dụ: "Windows Registry Editor Phiên bản 5.00" cho Windows 2000, Windows XP và Windows Server 2003.
- **Dòng trống**: Xác định điểm bắt đầu của đường dẫn đăng ký mới.
- **RegistryPathx**: Đường dẫn của khóa con chứa giá trị đầu tiên bạn đang nhập.
- **DataItemNamex**: Tên của mục dữ liệu mà bạn muốn nhập.
- **DataTypex**: Loại dữ liệu cho giá trị đăng ký.

Các khóa được lưu trữ trong tệp .reg bằng cú pháp sau:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Bạn có thể chỉnh sửa Giá trị mặc định của khóa bằng cách sử dụng "@" thay vì "Tên giá trị":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Thí dụ
Đây là một ví dụ về tệp REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Người giới thiệu

* [Windows Registry- của Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Cách thêm, sửa đổi hoặc xóa các giá trị và khóa con của sổ đăng ký bằng cách sử dụng tệp .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
