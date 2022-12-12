---
date: 2019-10-11
keywords: toml, .toml, định dạng file toml, cách mở file toml, đuôi .toml, đuôi toml
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp TOML
linktitle: TOML
description: "Tìm hiểu về định dạng tệp TOML và các API có thể tạo và mở tệp TOML."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Tệp TOML là gì? ##

TOML (Tom's Obvious Minimal Language) là một định dạng tệp cấu hình tối thiểu sử dụng phần mở rộng .toml. TOML nhằm mục đích dễ đọc, ánh xạ rõ ràng tới từ điển và dễ phân tích thành các cấu trúc dữ liệu khác nhau. TOML có đặc điểm kỹ thuật mã nguồn mở đã nhận được sự đóng góp của cộng đồng. TOML được hỗ trợ bởi nhiều ngôn ngữ lập trình như C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, v.v. Loại MIME cho các tệp TOML là *application/toml*.


## Định dạng tệp TOML ##

Các tệp TOML chủ yếu bao gồm các Cặp khóa/giá trị, phần/bảng, nhận xét và phải là tài liệu Unicode được mã hóa UTF-8 hợp lệ. TOML hỗ trợ các kiểu dữ liệu Chuỗi, Số nguyên, Float, Boolean, Ngày giờ, Mảng và Bảng (bảng băm/từ điển). TOML là một ngôn ngữ phân biệt chữ hoa chữ thường.

### Cú pháp ###

- **Cặp khóa-giá trị**: Các cặp khóa-giá trị được phân tách bằng dấu bằng (=). Mỗi cặp phải nằm trên một dòng mới.

``` toml
đầu tiên = "Tom"
cuối cùng = "Preston-Werner"
```

- **Nhận xét**: Nhận xét bắt đầu bằng ký hiệu thăng (#).

``` toml
# Đây là tài liệu TOML.
```

- **Strings**: Chuỗi được bao quanh bởi dấu ngoặc kép (") .

``` toml
chuỗi = "Chuỗi ví dụ"
```

- **Chuỗi nhiều dòng**: Chuỗi nhiều dòng được bao quanh bởi ba dấu ngoặc kép (""").

``` toml
[địa chỉ nhà]
đường = """123 Ngõ Lốc Xoáy
Phòng 16"""
thành phố = "Đông Centerville"
trạng thái = "KS"
```

- **Số nguyên/Số float**

``` toml
số nguyên = 20
nổi = 20,5
```

- **Booleans**: Booleans luôn là chữ thường.

``` toml
bool1 = đúng
bool2 = sai
```

- **Ngày-Giờ**: Đối với Ngày-Giờ, bạn có thể sử dụng ngày-giờ được định dạng RFC 3339 như minh họa trong ví dụ bên dưới.

``` toml
offset_date_time = 1979-05-27 07:32:00Z
local_date_time = 1979-05-27T07:32:00
local_date = 1979-05-27
local_time = 07:32:00
```

- **Mảng**: Mảng được bao quanh bởi dấu ngoặc vuông, các phần tử được phân tách bằng dấu phẩy (,).

``` toml
màu = [ "đỏ", "vàng", "xanh" ]
```

- **Bảng**: Bảng là tập hợp các cặp khóa/giá trị được xác định bởi tiêu đề trên một dòng mới được bao quanh bởi dấu ngoặc vuông ([]). Bảng kết thúc khi tiêu đề mới được cung cấp hoặc khi tệp kết thúc.

``` toml
[địa chỉ nhà]
đường = """123 Ngõ Lốc Xoáy
Phòng 16"""
thành phố = "Đông Centerville"
trạng thái = "KS"

[địa chỉ văn phòng]
đường = """123 Ngõ Lốc Xoáy
Phòng 16"""
thành phố = "Đông Centerville"
trạng thái = "KS"
```

Các bảng nội tuyến được bao quanh bởi dấu ngoặc nhọn ({}) với mỗi cặp khóa/giá trị được phân tách bằng dấu phẩy (,).

``` toml
tên = { đầu = "Tom", cuối = "Pitt" }
```

## Người giới thiệu ##

- [TOML - Wikipedia](https://vi.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

