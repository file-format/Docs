---
date: 2022-01-06
keywords: vtt, .vtt, định dạng tệp vtt, định dạng tệp .vtt, đuôi .vtt, đuôi vtt
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Tìm hiểu về tệp .vtt và các API có thể tạo và mở tệp VTT."
title: Định dạng tệp VTT - Tệp theo dõi văn bản video trên web
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Tệp VTT là gì?

Tệp VTT là một tệp văn bản chứa thông tin để hiển thị các bản nhạc văn bản được định thời gian (chẳng hạn như phụ đề hoặc chú thích) bằng định dạng Bản nhạc văn bản video trên web (WebVTT). Các rãnh văn bản được định thời gian bao gồm thông tin như phụ đề hoặc chú thích. Mục đích của tệp VTT là thêm lớp phủ văn bản vào một<video> . Định dạng hơi giống với các tệp SRT. Các tệp văn bản dựa trên WebVTT được mã hóa bằng UTF-8. Tệp VTT chứa thông tin như phụ đề, mô tả, chú thích, mô tả, chương và siêu dữ liệu. Là tệp văn bản thuần túy, tệp VTT có thể được mở bằng trình soạn thảo văn bản như Microsoft Notepad, Apple TextEdit và Notepad ++.

## Định dạng tệp VTT - Thông tin khác

Các tệp VTT sử dụng định dạng tệp WebVTT để lưu thông tin theo dõi văn bản tuần tự. Mỗi rãnh văn bản được định thời gian bao gồm một dòng hoặc nhiều dòng, còn được gọi là `cue` như minh họa trong ví dụ sau.

### Ví dụ tệp VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Cấu trúc tệp VTT

Sau đây là yêu cầu về cấu trúc của tệp VTT.

* Dấu thứ tự byte tùy chọn (BOM).
* Chuỗi "WEBVTT".
* Tiêu đề văn bản tùy chọn ở bên phải WEBVTT.
* Một dòng trống, tương đương với hai dòng mới liên tiếp.
* Không hoặc nhiều tín hiệu hoặc nhận xét.
* Không hoặc nhiều dòng trống.

## Người giới thiệu

* [VTT - W3 Schools](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

