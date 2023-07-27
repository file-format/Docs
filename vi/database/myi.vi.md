---
date: 2020-11-11
keywords: myi, .myi, định dạng file myi, cách mở file myi, đuôi .myi, đuôi myi
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp MYI
linktitle: MYI
description: "Tìm hiểu về định dạng tệp MYI và các API có thể tạo và mở tệp MYI."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Tệp MYI là gì? ##

MYI còn được gọi là tệp Chỉ mục MySQL MyISAM. Nó được sử dụng để lưu trữ các chỉ mục cho bảng MyISAM của MySQL. Chỉ mục cơ sở dữ liệu MySQL xác định cấu trúc của bảng và chứa cơ chế kiểm soát để kiểm tra tính toàn vẹn của bảng.

## Định dạng tệp MYI ##

Tệp MYI có hai phần, tiêu đề và các giá trị chính.

### Tiêu đề MYI ###

Tiêu đề chứa thông tin về các tùy chọn, kích thước tệp và khóa. Các khóa trong MySQL được tạo bằng một lệnh như

```sql
CREATE [UNIQUE] INDEX.
```

Các tệp đọc và ghi tệp MYI nằm trong thư mục ./myisam. Nó có các tập tin sau:

- mi_open.c: File này chứa các thủ tục viết từng phần của header.
- mi_create.c: Tệp này có các thường trình gọi các thường trình mi_open.c.
- myisamdef.h: Tệp này có định nghĩa cấu trúc.

Tiêu đề có các phần sau:

- trạng thái: Trạng thái được viết bởi mi_open.c, mi_state_info_write(). Cấu trúc này xảy ra một lần trong tệp.
- cơ sở: Cơ sở được viết bởi mi_open.c, mi_base_info_write(). MI_BASE_INFO là cấu trúc tương ứng cho cơ sở trong myisamdef.h. Cấu trúc này xảy ra một lần trong tệp.
- keydef: Keydef được viết bởi mi_open.c, mi_keydef_write(). MI_KEYDEF là cấu trúc tương ứng cho keydef trong myisamdef.h. Nó là một cấu trúc nhiều lần xuất hiện cho mỗi chỉ mục.
- recinfo: recinfo được viết bởi mi_open.c, mi_recinfo_write(). MI_COLUMNDEF là cấu trúc tương ứng cho recinfo trong myisamdef.h. Đó là cấu trúc nhiều lần xuất hiện một lần của mỗi trường xuất hiện trong một khóa.

### Giá trị khóa ###

Các trang trong MySQL được gọi là khối. Các giá trị chính nằm trong các khối. Một khối chứa thông tin từ chỉ một chỉ mục. Mỗi khóa chứa toàn bộ nội dung của tất cả các cột. Độ dài khối bình thường là 0x0400 (1024) byte. Con trỏ có số kích thước cố định (4 byte) cho các bảng hàng cố định có chứa số hàng thứ tự. Nếu khóa là null thì byte là 0x00. Một khối bình thường đầy ít nhất 65% và thường là 80%.

Tệp myisamdef.h chứa thông tin sau được biểu thị bằng hằng số. Số khóa tối đa là 32 (MI_MAX_KEY) và số phân đoạn tối đa trong một khóa là 16 (MI_MAX_KEY_SEG). Độ dài tối đa của khóa là 500 (MI_MAX_KEY_LENGTH). Độ dài tối đa của khối là 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Người giới thiệu ##

- [Tệp .MYI](https://dev.mysql.com/doc/dev/mysql-server/latest/)

