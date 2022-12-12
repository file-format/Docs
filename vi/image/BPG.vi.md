---
date: 2020-08-12
keywords: bpg, .bpg, định dạng file bpg, cách mở file bpg, đuôi .bpg, đuôi bpg
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp BPG
linktitle: BPG
description: "Tìm hiểu về định dạng tệp BPG và các API có thể tạo và mở tệp BPG."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Tệp BPG là gì? ##

BPG (Better Portable Graphics) là một định dạng tệp được tạo bởi Fabrice Bellard vào năm 2014 cho hình ảnh kỹ thuật số. Anh ấy đã đề xuất BPG để thay thế cho JPEG vì BPG nén hoặc kích thước hiệu quả hơn. BPG sử dụng mã hóa nội khung của tiêu chuẩn nén video HEVC (Mã hóa video hiệu quả cao).

BPG được thiết kế dưới dạng định dạng tiết kiệm bộ nhớ di động để hoạt động trên thiết bị cầm tay và thiết bị IoT. Hiện tại, các trình duyệt web không hỗ trợ định dạng BPG nhưng các trang web vẫn có thể phân phối hình ảnh BPG bằng cách sử dụng thư viện JavaScript do Bellard viết. BPG sử dụng cấu hình Ảnh tĩnh 4:4:4 16 Chính của HEVC tối đa 14 bit cho mỗi mẫu.

## Thông số kỹ thuật ##

Định dạng vùng chứa BPG là định dạng hình ảnh chung thay vì luồng bit thô được sử dụng trong HEVC. BPG hỗ trợ các định dạng màu 4:4:4, 4:2:2 và 4:2:0. Kênh Alpha cũng được hỗ trợ với một kênh bổ sung được mã hóa riêng hoặc kênh thứ tư của hình ảnh CMYK. BPG cung cấp hỗ trợ siêu dữ liệu cho Exif, cấu hình ICC và XMP. BPG hỗ trợ YCbCr (ITU-R BT.601, BT.709 và BT.2020 (độ sáng không cố định)), YCgCo, RGB, CMYK và không gian màu thang độ xám. BGP cũng hỗ trợ hoạt ảnh và nén dữ liệu HEVC không mất dữ liệu và không mất dữ liệu.

## Người giới thiệu ##

- [Đồ họa di động tốt hơn - Wikipedia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

