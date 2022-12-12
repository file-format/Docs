---
date: 2019-10-11
keywords: flv, .flv, định dạng tệp flv, định dạng tệp .flv, đuôi .flv, đuôi flv, định dạng video flv
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp FLV và các API có thể tạo và mở tệp FLV."
title: Định dạng tệp FLV
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Tệp FLV là gì? ##

FLV (Flash Video) là định dạng tệp chứa có phần mở rộng .flv. FLV được sử dụng để phân phối nội dung âm thanh/video qua internet bằng cách sử dụng Adobe Flash Player hoặc Adobe Air. Dữ liệu trong tệp FLV được mã hóa giống như tệp SWF. Hỗ trợ trực tiếp đã được thêm vào Flash Player 7 vào năm 2003. Hệ thống Adobe đã tạo F4V vào năm 2007 do các hạn chế của FLV.

### Mã hóa ###

Các tệp FLV chứa các luồng bit video của Sorenson Spark, một biến thể độc quyền của tiêu chuẩn video H.263. Đây là định dạng nén cần thiết cho Flash Player 6 và 7. Phiên bản 8 của Flash Player hỗ trợ cho các luồng bit video On2 TrueMotion VP6. Đây là định dạng nén được đề xuất cho Flash Player 8 trở lên. FLV hỗ trợ âm thanh ở định dạng MP3, Nellymoser Asao Codec và codec Speex mã nguồn mở. Nó cũng hỗ trợ âm thanh không nén hoặc âm thanh định dạng ADPCM. AAC (HE-AAC/AAC SBR, AAC Main Profile, và AAC-LC) được hỗ trợ bởi các phiên bản gần đây của Flash Player 9.

## Kết cấu ##

Tệp FLV bao gồm Tiêu đề và Gói. Tệp FLV bắt đầu bằng Tiêu đề. Tiêu đề có các trường sau.

- **Chữ ký**: Giá trị của nó là FLV
- **Phiên bản**: Giá trị mặc định của nó là 1. Chỉ 0x01 là hợp lệ.
- **Cờ**: 0x04 được sử dụng cho âm thanh và 0x01 được sử dụng cho video nên 0x05 được sử dụng cho cả âm thanh và video.
- **Kích thước tiêu đề**: Giá trị mặc định là 9. Giá trị này được sử dụng để bỏ qua tiêu đề được mở rộng mới hơn.

Sau tiêu đề là các Gói. Tệp FLV được chia thành nhiều gói được gọi là thẻ FLV có tiêu đề 15 byte. Các gói chứa siêu dữ liệu cho âm thanh, video, tập lệnh, thông tin mã hóa và tải trọng. Các gói FLV có các trường sau.

- **Dành riêng**: Nó được dành riêng cho FMS và phải là 0.
- **Filter**: Cho biết gói tin có được lọc hay không.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Packet Type**: Điều này xác định loại nội dung trong gói.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Kích thước dữ liệu**: Điều này biểu thị độ dài của tin nhắn.
- **Dấu thời gian thấp hơn**: Dấu thời gian này lưu trữ dấu thời gian tính bằng mili giây mà tại đó dữ liệu thẻ được áp dụng. Nó được đặt thành NULL cho gói đầu tiên.
- **Timestamp Upper**: Tiện ích mở rộng để tạo giá trị uint32_be.
- **ID luồng**: Giá trị này được đặt thành NULL cho luồng đầu tiên.
- **Dữ liệu tải trọng**: Đây là dữ liệu dựa trên loại gói.

## Người giới thiệu ##

- [Video Flash - Wikipedia](https://vi.wikipedia.org/wiki/Flash_Video)

