---
date: 2019-10-11
keywords: MP4, tệp, phần mở rộng, định dạng, định dạng video, MPEG-4
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp MP4 và các API có thể tạo và mở tệp MP4."
title: Định dạng tệp MP4
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Tệp MP4 là gì? ##

MP4 (viết tắt của MPEG-4 Phần 14) là định dạng tệp dựa trên ISO/IEC 14496-12:2004 dựa trên Định dạng tệp QuickTime nhưng chính thức chỉ định hỗ trợ cho Bộ mô tả đối tượng ban đầu (IOD) và các tính năng MPEG khác. Nó chủ yếu được sử dụng để lưu trữ video và âm thanh nhưng cũng có thể được sử dụng để lưu trữ phụ đề và hình ảnh tĩnh. Các tệp MP4 được lưu trữ với phần mở rộng .mp4. MP4 là một tiêu chuẩn mã hóa nghe nhìn quốc tế. Tương tự như hầu hết các định dạng chứa hiện đại, MP4 hỗ trợ phát trực tuyến qua internet. Do độ nén cao được sử dụng trong MP4, các tệp kết quả có kích thước nhỏ hơn với hầu hết chất lượng ban đầu được giữ lại.

## Lược Sử ##

Thông số kỹ thuật MP4 do Nhóm chuyên gia hình ảnh chuyển động (MPEG) phát triển và dựa trên định dạng QuickTime [MOV](/vi/video/mov/) được xuất bản vào năm 2001. Phiên bản đầu tiên (ISO/IEC 14496-1:2001) của MP4 là bản sửa đổi của MPEG-4 Phần 1: Thông số kỹ thuật hệ thống được xuất bản năm 1999. Định dạng tệp MP4 được khái quát hóa thành Định dạng tệp phương tiện cơ sở ISO ISO/IEC 14496-12:2004 đã xác định cấu trúc chung cho các tệp phương tiện dựa trên thời gian. Do đó, nó được sử dụng làm cơ sở cho các định dạng tệp khác.

## Cấu trúc của tệp MP4 ##

MP4 là một tệp chứa có thể mở rộng, nghĩa là nó không xác định cấu trúc nghiêm ngặt và cho phép cấu trúc và phân cấp tùy chỉnh cho từng loại phương tiện. Dữ liệu trong tệp MP4 được chia thành hai phần, phần thứ nhất chứa dữ liệu liên quan đến phương tiện và phần thứ hai chứa siêu dữ liệu. Dữ liệu phương tiện chứa âm thanh hoặc video và siêu dữ liệu cho biết cờ để truy cập ngẫu nhiên, dấu thời gian, v.v.
Các cấu trúc trong MP4 thường được gọi là nguyên tử hoặc hộp. Kích thước tối thiểu của một nguyên tử là 8 byte (4 byte đầu tiên chỉ định kích thước và 4 byte tiếp theo chỉ định loại). Dưới đây là danh sách các nguyên tử cấp gốc có trong các tệp MP:

- **ftyp**: Chứa loại tệp, mô tả và cấu trúc dữ liệu phổ biến được sử dụng.
- **pdin**: Chứa thông tin tải/tải video liên tục.
- **moov**: Nơi chứa tất cả siêu dữ liệu phim.
- **moof**: Vùng chứa các đoạn video.
- **mfra**: Vùng chứa có quyền truy cập ngẫu nhiên vào đoạn video
- **mdat**: Vùng chứa dữ liệu cho phương tiện.
- **stts**: bảng mẫu theo thời gian.
- **stsc**: bảng mẫu tới đoạn.
- **stsz**: kích thước mẫu (đóng khung)
- **meta**: Vùng chứa thông tin siêu dữ liệu.

Dưới đây là danh sách các nguyên tử cấp hai được sử dụng trong MP4:

- **mvhd**: Chứa thông tin tiêu đề video với đầy đủ chi tiết của video.
- **trak**: Vùng chứa có rãnh riêng lẻ.
- **udta**: Vùng chứa thông tin người dùng và theo dõi.
- **iods**: mô tả tập tin MP4

## Người giới thiệu ##

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

