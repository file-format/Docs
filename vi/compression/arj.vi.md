---
date: 2019-12-09
keywords: arj, .arj, định dạng file arj, cách mở file arj, đuôi .arj, đuôi arj
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp ARJ
linktitle: ARJ
description: "Tìm hiểu về định dạng tệp ARJ và các API có thể tạo và mở tệp ARJ."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Tệp ARJ là gì? ##

ARJ (Được lưu trữ bởi Robert Jung) là một tệp lưu trữ nén hiệu quả cao được phát triển bởi Robert K. Jung. ARJ được phát triển cho DOS và các phiên bản đầu tiên của Windows vào đầu những năm 1990. Các tệp ARJ rất hữu ích để sao lưu hoặc chia sẻ một số lượng lớn tệp vì bạn không phải theo dõi tất cả các tệp đó và chỉ có một tệp duy nhất để xử lý. Phần mở rộng .arj được sử dụng cho các tệp lưu trữ ARJ.

## Định dạng tệp ARJ ##

Tệp ARJ chứa hai loại tiêu đề:

- Tiêu đề chính: Có một tiêu đề chính ở đầu tệp lưu trữ.
- Tiêu đề cục bộ: Tiêu đề cục bộ hiện diện trước mỗi tệp.

|Độ lệch|Loại|Đếm|Mô tả|
|---|---|---|---|
|0000h|từ|1|ID=0EA60h|
|0002h|từ|1|kích thước tiêu đề cơ bản|
|0004h|byte|1|Kích thước của tiêu đề|
|0005h|byte|1|Số phiên bản trình lưu trữ|
|0006h|byte|1|Số phiên bản tối thiểu cần thiết|
|0007h|byte|1|Hệ điều hành máy chủ:</br> 0 - MS-DOS</br> 1 - NGUYÊN TẮC</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (Hệ thống xx)</br> 5 - Hệ điều hành/2</br> 6 - ỨNG DỤNG GS</br> 7 - CÔNG TY CỔ PHẦN THƯƠNG MẠI</br> 8 - Tiếp theo</br> 9 - VAX VMS|
|0008h|byte|1|Cờ nội bộ, ánh xạ bit:</br> 0 - không có mật khẩu / mật khẩu</br> 1 - dành riêng</br> 2 - tập tin tiếp tục trên đĩa tiếp theo</br> 3 - trường vị trí bắt đầu tệp có sẵn</br> 4 - dịch đường dẫn ( "\" thành "/" )|
|0009h|byte|1|Phương pháp nén:</br> 0 - được lưu trữ</br> 1 - nén nhiều nhất</br> 2 - nén</br> 3 - nén nhanh hơn</br> 4 - nén nhanh nhất|
|000Ah|byte|1|Loại tệp:</br> 0 - nhị phân</br> 1 - văn bản 7 bit</br> 2 - tiêu đề bình luận</br> 3 - thư mục</br> 4 - nhãn tập|
|000Bh|byte|1|dành riêng|
|000Ch|dword|1|Ngày/Giờ của tệp gốc ở định dạng MS-DOS|
|0010h|dword|1|Kích thước tệp nén|
|0014h|dword|1|Kích thước của tệp gốc"|
|0018h|dword|1|CRC-32 của tệp gốc|
|001Ah|từ|1|Vị trí đặc tả tệp trong tên tệp|
|001Ch|từ|1|Thuộc tính tệp|
|001Eh|từ|1|Dữ liệu máy chủ|
|?|dword|1|Vị trí bắt đầu tệp mở rộng|
|????h|dword|1|CRC-32 của tiêu đề cơ bản|
|????h|từ|1|Kích thước của tiêu đề mở rộng đầu tiên|
|????h+"SIZ"+2|dword|1|CRC-32 của tiêu đề mở rộng|
|????h+"SIZ"+6|byte|?|Tập tin nén|

## Người giới thiệu ##

- [ARJ - Wikipedia](https://vi.wikipedia.org/wiki/ARJ)

