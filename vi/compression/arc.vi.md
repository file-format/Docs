---
date: 2019-12-09
keywords: arc, .arc, định dạng file arc, cách mở file arc, đuôi .arc, đuôi arc
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp ARC
linktitle: ARC
description: "Tìm hiểu về định dạng tệp ARC và các API có thể tạo và mở tệp ARC."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Tệp ARC là gì?

ARC là một định dạng lưu trữ và nén dữ liệu không mất dữ liệu được phát triển bởi Hiệp hội Cải tiến Hệ thống (SEA). Định dạng tệp và ứng dụng tạo ra nó đều được gọi là ARC. ARC rất phổ biến trong những ngày đầu của BBS quay số vì nó kết hợp các tính năng nén và lưu trữ nhiều tệp trong cùng một tệp. ARC sau đó đã được thay thế bằng [ZIP](/vi/compression/zip/) cung cấp tỷ lệ nén tốt hơn.

Phần mở rộng tệp .arc được sử dụng bởi một số loại tệp lưu trữ không liên quan khác như định dạng ARC được Lưu trữ Internet sử dụng để lưu trữ nhiều tài nguyên web, một định dạng ARC khác được trình lưu trữ FreeArc sử dụng, một định dạng khác được Nintendo sử dụng cho các tài nguyên, v.v. .

## Lịch sử tóm tắt về định dạng tệp ARC

Chương trình ARC được viết bởi Thom Henderson của Hiệp hội Tăng cường Hệ thống vào năm 1985. Chương trình này đã nhóm các tệp thành một tệp lưu trữ duy nhất và cũng nén chúng. Các tệp được tạo bởi chương trình ARC đã sử dụng phần mở rộng .arc. SEA đã phát hành mã nguồn cho ARC vào năm 1986 và ARC đã được chuyển sang Unix và Atari ST bởi Howard Chu vào năm 1987.

Phil Katz đã phát triển PKARC và PKXARC để lưu trữ và giải nén tệp. Các tệp hoạt động với định dạng tệp ARC và nhanh hơn đáng kể. Không giống như ARC, Katz phân chia các chức năng nén và lưu trữ giữa hai tệp khác nhau để giảm yêu cầu bộ nhớ để chạy chúng.

Sau vụ kiện giữa SEA và Katz, SEA đã rút khỏi thị trường phần mềm chia sẻ và phát triển ARC+Plus với giao diện người dùng toàn màn hình. Định dạng ARC không còn phổ biến trên PC nữa.

## Định dạng tệp ARC

Tệp ARC bao gồm một chuỗi tiêu đề tệp và tệp theo sau là điểm đánh dấu cuối kho lưu trữ như minh họa bên dưới.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### Tiêu đề tệp ARC ###

|Độ lệch|Nhãn|Loại|Giá trị|Mô tả|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Phương pháp|
|02|ARCFNT|DS|12|tên tệp|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Kích thước nén|
|13|ARCDAT|DW|0000|Ngày tệp (MSDOS)|
|15|ARCTIM|DW|0000|Thời gian tệp (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Kích thước không nén|
|1D|ARCFIL|DS|ARCNSZ| |

### Phương thức nén ###

Byte phương pháp nén cho biết phương pháp nén được sử dụng. Sau đây là các phương pháp nén được sử dụng cho tệp ARC.

|Phương thức|Tên|Mô tả|
|---|---|---|
|0|Đã lưu trữ|Không sử dụng nén|
|1|Đã đóng gói|Mã hóa độ dài chạy lặp lại (RLE)|
|2|Bóp|Mã hóa Huffman|
|3|Crunched|LZW với bộ đệm 4K, mã 12 bit|
|4|Crunched|Đóng gói đầu tiên, sau đó là bộ đệm LZW 4K với 12 bit|
|5|Crunched|Đóng gói, LZW, bộ đệm 4K, độ dài thay đổi (9-12 bit)|
|6|Squashed|LZW, bộ đệm 8K, độ dài thay đổi (9-13 bit)|
|7|Crushed|Đóng gói, sau đó là bộ đệm LZW 8K, 2-13 bit (PAK 1.0)|
|8|Chưng cất|Dynamic Huffman với bộ đệm 8K (PAK 2.0)|

## Người giới thiệu

- [ARC (định dạng tệp) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

