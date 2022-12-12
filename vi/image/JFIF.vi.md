---
date: 2020-08-12
keywords: jfif, .jfif, định dạng file jfif, cách mở file jfif, đuôi .jfif, đuôi jfif
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Tệp JFIF - Tệp .jfif là gì?
linktitle: JFIF
description: "Tìm hiểu về định dạng tệp JFIF và các API có thể tạo và mở tệp JFIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Tệp JFIF là gì?

JFIF (Định dạng trao đổi tệp JPEG (JFIF)) là một tệp định dạng hình ảnh sử dụng phần mở rộng .jfif. JFIF xây dựng trên JIF (Định dạng trao đổi JPEG) bằng cách giảm độ phức tạp và giải quyết các hạn chế của nó.

## Lược sử về JFIF

Việc phát triển tài liệu JFIF do Eric Hamilton phụ trách và một thỏa thuận về phiên bản đầu tiên được thiết lập vào cuối năm 1991. Phiên bản 1.02 được xuất bản vào ngày 7 tháng 9 năm 1992. RFC 2046 quy định rằng định dạng JFIF được sử dụng để truyền hình ảnh JPEG qua internet. JFIF được ECMA xuất bản vào năm 2009 và được ITU-T chuẩn hóa vào năm 2011 với tên Khuyến nghị T.871 và bởi ISO/IEC vào năm 2013 với tên ISO/IEC 10918-5

## Định dạng tệp JFIF ##

Tệp JFIF bao gồm một chuỗi các điểm đánh dấu như được định nghĩa trong phần 1 của Tiêu chuẩn JPEG. Mỗi điểm đánh dấu bao gồm hai byte (FF theo sau bởi một byte chỉ định loại điểm đánh dấu). Các điểm đánh dấu có thể độc lập hoặc chỉ ra điểm bắt đầu của đoạn đánh dấu.

JFIF cho phép nhiều thành phần như Y, Cb, Cr, có độ phân giải khác nhau nhưng sự liên kết của chúng không được xác định. Không giống như JPEG, JFIF có thể cung cấp thông tin về độ phân giải và tỷ lệ khung hình. JFIF cũng xác định mô hình màu sẽ được sử dụng.

### Cấu trúc tệp ##

|Phân đoạn|Mã|Mô tả|
|---|---|---|
|SOI|FF D8|Bắt đầu hình ảnh|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|đoạn đánh dấu bổ sung|
|SOS|FF DA|Bắt đầu quét|
||dữ liệu ảnh nén||
|EOI|FF D9|Kết thúc hình ảnh|

Tiêu chuẩn JFIF xác định các phân đoạn sau:

### Đoạn đánh dấu JFIF APP0 ###

Nó là đoạn bắt buộc chứa các thông số ảnh. Nó cũng có thể chứa một hình thu nhỏ không nén được nhúng.

|Trường|Kích thước (byte)|Mô tả|
|---|---|---|
|Đánh dấu APP0|2|FF E0|
|Chiều dài|2|Chiều dài của đoạn không bao gồm điểm đánh dấu APP0|
|Định danh|5|JFIF (4A 46 49 46 00) trong ASCII được kết thúc bởi một byte rỗng|
|Phiên bản JFIF|2|Phiên bản JFIF|
|Đơn vị mật độ|1|Đơn vị cho các trường mật độ pixel sau</br> 00 : Không có đơn vị; tỷ lệ khung hình chiều rộng:chiều cao bằng với Ydensity:Xdensity</br> 01 : Điểm ảnh trên mỗi inch</br> 02 : Điểm ảnh trên cm|
|Xdensity|2|Mật độ pixel ngang lớn hơn 0|
|Ydensity|2|Mật độ pixel dọc lớn hơn 0|
|Xthumbnail|1|Số pixel theo chiều ngang của hình thu nhỏ RGB được nhúng. Có thể bằng không|
|Ythumbnail|1|Số pixel dọc của hình thu nhỏ RGB được nhúng. Có thể bằng không|
|Dữ liệu hình thu nhỏ|3 × n|Dữ liệu hình thu nhỏ raster 24 bit RGB không nén|

### Đoạn đánh dấu APP0 mở rộng JFIF ###

Đây là phần tùy chọn mà nếu được xác định thì phải ngay sau đoạn đánh dấu JFIF APP0. Phần này được hỗ trợ bởi JFIF phiên bản 1.02 trở lên và cho phép nhúng các hình thu nhỏ ở ba định dạng khác nhau.

|Trường|Kích thước (byte)|Mô tả|
|---|---|---|
|Đánh dấu APP0|2|FF E0|
|Chiều dài|2|Chiều dài của đoạn không bao gồm điểm đánh dấu APP0|
|Định danh|5|JFXX (4A 46 58 58 00) trong ASCII được kết thúc bởi một byte rỗng|
|Định dạng hình thu nhỏ|1|Chỉ định định dạng dữ liệu nào được sử dụng cho hình thu nhỏ nhúng sau:</br> 10 : Định dạng JPEG</br> 11 : 1 byte cho mỗi pixel định dạng bảng màu</br> Định dạng RGB 13 : 3 byte cho mỗi pixel|
|Dữ liệu hình thu nhỏ|biến||

## Chuyển đổi JFIF sang các định dạng tệp hình ảnh khác

JFIF có thể được chuyển đổi sang các định dạng tệp hình ảnh phổ biến như [PNG](/vi/image/png/), [JPG](/vi/image/jpg/) và [PDF](/vi/pdf/).

## Người giới thiệu ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

