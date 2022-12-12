---
date: 2019-10-11
keywords: srt, .srt, định dạng tệp srt, định dạng tệp .srt, phần mở rộng .srt, phần mở rộng srt
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp SRT và các API có thể tạo và mở tệp SRT."
title: Định dạng tệp SRT
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Tệp SRT là gì? ##

SRT (định dạng tệp SubRip) là một tệp phụ đề đơn giản được lưu ở định dạng tệp SubRip với phần mở rộng .srt. Nó chứa một số liên tiếp các phụ đề, dấu thời gian bắt đầu và kết thúc cũng như văn bản phụ đề. Các tệp SRT cho phép thêm phụ đề vào nội dung video sau khi sản xuất.

## Cấu trúc tệp SRT ##

Mỗi phụ đề có bốn phần trong tệp SRT.

1. Bộ đếm số cho biết số lượng hoặc vị trí của phụ đề.
1. Thời gian bắt đầu và kết thúc phụ đề cách nhau bởi -> ký tự
1. Văn bản phụ đề trong một hoặc nhiều dòng.
1. Một dòng trống cho biết phần cuối của phụ đề.

### Ví dụ về SRT ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Để chỉ định định dạng thời gian *giờ:phút:giây,mili giây (00:00:00,000)* được sử dụng.

## Định dạng tệp SRT ##

Định dạng của các tệp SRT được lấy từ các thẻ HTML. Các thẻ định dạng cho tệp SRT được liệt kê bên dưới.

| Hiệu ứng | Thẻ |
| --- | --- |
|Đậm|**\ <b>...\</b> ** hoặc {b}...{/b}|
|Italic|**\ <i>...\</i> ** hoặc **{i}...{/i}**|
|Gạch chân|**\ <u>...\</u> ** hoặc **{u}...{/u}**|
|Màu Phông|**\ <font color="white">...\</font> **|
|Vị trí dòng|**{\a3}** (cho biết văn bản sẽ bắt đầu xuất hiện trên dòng 3)

## Phần mềm SubRip ##

SubRip là một chương trình phần mềm miễn phí chạy trên Windows. Nó trích xuất phụ đề và thời gian của chúng từ các định dạng video khác nhau và lưu phụ đề ở định dạng SRT. SubRip sử dụng nhận dạng ký tự quang học để trích xuất phụ đề từ video trực tiếp, các tệp video khác và DVD.

## Người giới thiệu ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
