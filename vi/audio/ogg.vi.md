---
date: 2019-12-13
keywords: ogg, định dạng tệp ogg, phần mở rộng .ogg, định dạng âm thanh ogg
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp OGG và các API có thể tạo và mở tệp OGG."
title: Tệp OGG - Tệp âm thanh Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Tệp OGG là gì?

OGG là Tệp âm thanh nén Ogg Vorbis được lưu với phần mở rộng .ogg. Các tệp OGG được sử dụng để lưu trữ dữ liệu âm thanh và có thể bao gồm cả thông tin về nghệ sĩ và bản nhạc cũng như siêu dữ liệu. OGG là một định dạng vùng chứa mở và miễn phí được duy trì bởi Xiph.Org Foundation.

## Lịch sử tóm tắt về định dạng tệp OGG

Dự án Ogg bắt đầu như một phần của dự án lớn hơn vào năm 1993 và được đặt tên là Squish nhưng do nhãn hiệu hiện có nên nó được đổi tên thành OggSquish. Nó được mô tả là nỗ lực tạo ra một định dạng âm thanh nén linh hoạt cho các ứng dụng âm thanh hiện đại. Tài liệu tham khảo OGG đã được tách khỏi Vorbis vào ngày 2 tháng 9 năm 2000.

OGM được tạo ra vào năm 2002 do thiếu hỗ trợ video chính thức trong OGG. Điều này cho phép nhúng video từ khuôn khổ Microsoft DirectShow vào trình bao bọc dựa trên OGG. Đến năm 2006, OGG được hỗ trợ bởi nhiều công cụ trò chơi điện tử và thường được sử dụng để mã hóa nội dung miễn phí. Tổ chức Phần mềm Tự do đã bắt đầu một chiến dịch vào ngày 15 tháng 5 năm 2007 để tăng cường sử dụng Vorbis như một giải pháp thay thế ưu việt cho MP3. Đến ngày 30 tháng 6 năm 2009, OGG là định dạng vùng chứa duy nhất được hỗ trợ bởi triển khai HTML5 của Firefox 3.5.

## Định dạng tệp OGG

Định dạng OGG bao gồm các khối dữ liệu. Mỗi đoạn được gọi là một trang Ogg. Mỗi trang bắt đầu bằng "OggS" để xác định Định dạng Ogg. Tiêu đề chứa số sê-ri và số trang xác định mỗi trang là một phần của sê-ri. Trang bao gồm các thành phần sau.

- **Tiêu đề trang**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Chút | Giá trị | Mô tả |
| --- | --- | --- |
| 0 | 0x01 | Chỉ ra rằng gói đầu tiên của trang là phần tiếp theo của gói trước đó trong dòng bit logic. |
| 1 | 0x02 | Cho biết rằng trang này là trang đầu tiên trong dòng bit logic. |
| 2 | 0x04 | Cho biết rằng trang này là trang cuối cùng trong dòng bit hợp lý. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Siêu dữ liệu**: VorbisComment là cơ chế được hỗ trợ rộng rãi nhất để lưu trữ siêu dữ liệu. Các cơ chế khác bao gồm:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Người giới thiệu ##

- [OGG - Wikipedia](https://vi.wikipedia.org/wiki/Ogg)

