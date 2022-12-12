{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Tệp mẫu báo cáo tiên dược",
  "description":"Tìm hiểu về tệp RML và các API có thể tạo và mở tệp RML.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Tệp RML là gì?

Tệp RML là một tệp mẫu báo cáo với công cụ báo cáo [Elixir Repertoire](https://elixirtech.com/repertoire-2/). Tệp mẫu được sử dụng để tạo báo cáo với nguồn dữ liệu được kết nối với Hệ thống tệp Elixir. Dữ liệu được đọc và điền vào tệp mẫu RML và có thể được xuất sang một số định dạng tệp khác nhau, chẳng hạn như [PDF](/vi/pdf/), [RTF](/vi/word-processing/rtf/) và bảng tính [XLS] (/vi/bảng tính/xls/). Công cụ báo cáo Elixir Repertoire có thể được kết nối với nhiều nguồn dữ liệu JDBC khác nhau.

## Định dạng tệp RML

Chi tiết cấu trúc tệp nội bộ của định dạng tệp RML không có sẵn công khai. Các tệp được tạo và lưu nội bộ bởi ứng dụng Elixir Repertoire để tạo báo cáo với dữ liệu được điền từ các nguồn dữ liệu được kết nối. Tệp mẫu RML chứa thông tin trình giữ chỗ và bố cục tổng thể của báo cáo cuối cùng sẽ được tạo từ dữ liệu.

## Làm cách nào để tệp mẫu RML?

Để tạo mẫu RML trong Tiết mục Tiên dược, có thể thực hiện theo các bước sau.

1. Kết nối nguồn dữ liệu JDBC với hệ thống tệp.
1. Khởi chạy Trình hướng dẫn Mẫu Báo cáo
1. Dùng phần mềm định vị file .ds nguồn dữ liệu
1. Chọn báo cáo dạng bảng làm lựa chọn xuất
1. Chọn các trường để đưa vào mẫu báo cáo
1. Cuối cùng, khi nhấp vào nút Kết thúc, First report.rml được thêm vào kho lưu trữ và được mở để hiển thị tab Bố cục.

## Người giới thiệu

* [Tiết mục Elixir](https://elixirtech.com/repertoire-2/)

