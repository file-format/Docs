{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp WHL - Tệp gói bánh xe Python",
  "description":"Tìm hiểu về định dạng tệp WHL và API có thể tạo và mở tệp WHL.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Tệp WHL là gì?

Tệp WHL (Bánh xe) là tệp gói phân phối được lưu ở định dạng bánh xe của Python. Đây là bản cài đặt định dạng tiêu chuẩn của các bản phân phối Python và chứa tất cả các tệp và siêu dữ liệu cần thiết để cài đặt. Tệp WHL cũng chứa thông tin về các phiên bản Python và nền tảng được tệp bánh xe này hỗ trợ. Tương tự như tệp thiết lập [MSI](/vi/executable/msi/), định dạng tệp WHL là định dạng sẵn sàng cài đặt cho phép chạy gói cài đặt mà không cần xây dựng bản phân phối nguồn.

## Định dạng tệp WHL

Định dạng tệp WHL là tệp lưu trữ [ZIP](/vi/compression/zip/) (.zip) chứa tất cả tệp cài đặt và siêu dữ liệu mà trình cài đặt yêu cầu để cài đặt gói. Các tệp WHL này có thể được giải nén bằng tùy chọn giải nén hoặc các ứng dụng phần mềm giải nén tiêu chuẩn như WinZIP và WinRAR.

### Quy ước tên tệp WHL

Tệp WHL được đặt tên theo quy ước sau.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Một ví dụ về tên tệp WHL như sau.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `cryptography` là tên gói.
* `2.9.2` là phiên bản gói của mật mã. Một phiên bản là một chuỗi tuân thủ PEP 440, chẳng hạn như 2.9.2, 3.4 hoặc 3.9.0.a3.
* `cp35` là thẻ Python và biểu thị phiên bản và triển khai Python mà bánh xe yêu cầu.
* `abi3` là thẻ ABI. ABI là viết tắt của giao diện nhị phân ứng dụng.
* `macosx_10_9_x86_64` là thẻ nền tảng, điều này xảy ra khá nhiều.

## Người giới thiệu

* [Bánh xe Python là gì và tại sao bạn nên quan tâm?](https://realpython.com/python-wheels/)
* [Bánh xe Python](https://pypi.org/project/wheel/)

