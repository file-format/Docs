---
date: 2019-10-11
keywords: f4v, .f4v, định dạng tệp f4v, định dạng tệp .f4v, đuôi .f4v, đuôi f4v, định dạng video f4v, cách mở tệp f4v, tệp f4v là gì
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp F4V và các API có thể tạo và mở tệp F4V"
title: Định dạng tệp F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Tệp F4V là gì? ##

F4V (Flash MP4 Video File) là một tệp video được lưu với phần mở rộng .f4v. Nó dựa trên định dạng tệp phương tiện cơ sở ISO (MPEG-4 Phần 12). Nó rất giống với [MP4](/vi/video/mp4/), đó là lý do tại sao nó còn được gọi một cách không chính thức là Flash MP4. [FLV](/vi/video/flv/) có giới hạn khi phát trực tuyến nội dung H.264/ACC dẫn đến việc Adobe Systems tạo định dạng F4V mới. Flash Player có thể phát các tệp F4V kể từ khi phát hành Flash Player 9 Update 3.

## Cấu trúc của tệp F4V ##

Định dạng tệp F4V dựa trên định dạng tệp phương tiện cơ sở ISO (MPEG-4 Phần 12) và rất giống với định dạng MP4. Để biết chi tiết về cấu trúc, vui lòng xem trang [MP4](/vi/video/mp4/). Sự khác biệt chính giữa F4V và MP4 là các định dạng siêu dữ liệu mà F4V có thể lưu trữ. Dưới đây là danh sách các định dạng siêu dữ liệu được hỗ trợ bởi định dạng F4V.

- **Hộp thẻ**: Bốn hộp thẻ tùy chọn bổ sung (xác thực, tiêu đề, dscp, cprt) trong hộp Phim (moov).
- **Hộp Siêu dữ liệu XMP**: Hộp này xuất hiện ngay sau hộp Phim (moov). Với điều này, tệp có thể giao tiếp siêu dữ liệu XMP với phim SWF thông qua ActionScript.
- **ilst box**: Hộp này xuất hiện bên trong hộp Meta (meta) và có thể chứa một số thẻ siêu dữ liệu. Các loại dữ liệu được hỗ trợ được đưa ra dưới đây.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Hộp Siêu dữ liệu theo dõi văn bản**: Các mẫu văn bản (văn bản hoặc tx3g) bên trong Hộp dữ liệu phương tiện (mdat). Nó có thể chứa các hộp siêu dữ liệu sau.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Người giới thiệu ##

- [Video Flash - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

