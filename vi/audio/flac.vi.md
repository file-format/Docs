---
date: 2019-12-13
keywords: flac, định dạng tệp flac, phần mở rộng .flac, tệp flac, flac vs mp3
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp FLAC và các API có thể tạo và mở tệp FLAC."
title: Định dạng tệp FLAC
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Tệp FLAC là gì?

FLAC(Free Lossless Audio Codec) là định dạng mã hóa âm thanh nén không mất dữ liệu được phát triển bởi Xiph.Org Foundation. FLAC là một định dạng mở miễn phí bản quyền được lưu với phần mở rộng .flac. Âm thanh kỹ thuật số được nén bằng thuật toán FLAC thường giảm kích thước xuống còn 50 đến 70 phần trăm. Các tệp FLAC có thể được giải nén thành một bản sao giống hệt của các tệp âm thanh gốc.

## Định dạng tệp FLAC

Đây là tổng quan về dòng bit FLAC.

- **điểm đánh dấu fLaC**: Điểm đánh dấu này được thêm vào đầu luồng. Nó được theo sau bởi một hoặc nhiều khối siêu dữ liệu.
- **Khối siêu dữ liệu**: FLAC hỗ trợ 128 loại khối siêu dữ liệu; hiện tại những điều sau đây được xác định.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: Dữ liệu âm thanh bao gồm một hoặc nhiều khung âm thanh.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Lịch sử tóm tắt về định dạng tệp FLAC

Josh Coalson bắt đầu phát triển FLAC vào năm 2000. Phiên bản đầu tiên của FLAC được phát hành vào ngày 20 tháng 7 năm 2001. FLAC được kết hợp dưới cờ Xiph.Org vào ngày 20 tháng 1 năm 2003. Sự phát triển của FLAC đã được chuyển sang kho git Xiph.Org với việc phát hành phiên bản 1.3.0 vào ngày 26 tháng 3 năm 2013.

## Thành phần của Dự án FLAC

Dự án FLAC bao gồm những điều sau đây:

- Định dạng luồng.
- Định dạng vùng chứa đơn giản cho luồng (FLAC).
- libFLAC: Thư viện mã hóa tham chiếu, bộ giải mã và giao diện siêu dữ liệu.
- libFLAC++: Trình bao bọc hướng đối tượng cho libFLAC.
- flac: Một chương trình dòng lệnh để mã hóa và giải mã các luồng FLAC.
- metaflac: Trình chỉnh sửa siêu dữ liệu dòng lệnh cho FLAC.
- Nhập các plugin cho trình phát nhạc như Winamp, XMMX, v.v.
- Định dạng vùng chứa Ogg (Ogg FLAC).

## Thiết kế FLAC

Tùy thuộc vào mật độ và biên độ của âm nhạc, kích thước của tệp nén có thể nhỏ hơn 80% so với tệp gốc.

### Bộ mã hóa nguồn ###

- Nó chỉ hỗ trợ các mẫu số nguyên và không dấu phẩy động. Nó có thể xử lý độ phân giải bit PCM từ 4 đến 32 bit trên mỗi mẫu và tốc độ lấy mẫu từ 1Hz đến 65.535 Hz. Mã hóa FLAC được giới hạn ở 24 bit cho mỗi mẫu.
- Các kênh có thể được nhóm lại để tận dụng mối tương quan giữa các kênh nhằm tăng khả năng nén.
- Tổng kiểm tra CRC được sử dụng để xác định các khung bị hỏng.
- Để chuyển đổi các mẫu âm thanh, FLAC sử dụng dự đoán tuyến tính.

### Metadata ###

- FLAC hỗ trợ ReplayGain (được sử dụng để cảm nhận và chuẩn hóa âm lượng trong âm thanh).
- FLAC sử dụng cùng một hệ thống được sử dụng trong các nhận xét của Vorbis để gắn thẻ.
- libFLAC được hầu hết các ứng dụng FLAC sử dụng để mã hóa/giải mã.
- API libFLAC được tổ chức thành các luồng, luồng có thể tìm kiếm và tệp để tăng tính trừu tượng từ luồng bit FLAC cơ sở.

### Nén ###

libFLAC sử dụng các mức nén từ 0 đến 8 trong đó 0 là nhanh nhất và 8 là mức nén chậm nhất. Các tệp nén luôn không mất dữ liệu mặc dù có sự đánh đổi giữa tốc độ và kích thước.

## FLAC so với MP3
MP3 là một định dạng nén mất dữ liệu có nghĩa là nó có thể cắt một phần âm thanh để giảm kích thước sau khi áp dụng nén. Trong khi đó, FLAC là định dạng tệp không mất dữ liệu, có nghĩa là bạn có thể nghe âm thanh ở dạng tinh khiết nhất. Trước đó, các định dạng tệp không mất dữ liệu là CDA hoặc WAV không có nhiều dung lượng hiệu quả như FLAC. Bảng sau đây sẽ cho thấy sự so sánh giữa hai định dạng này đối với một số thuật ngữ quan trọng:

|Thuật ngữ|FLAC|MP3|
---|---|---|
|**Chất lượng dữ liệu**|Không mất dữ liệu âm thanh| Một số dữ liệu có thể bị mất khi nén dữ liệu âm thanh|
|**Size**|Kích thước tệp lớn hơn so với các định dạng mất dữ liệu. Vì vậy cần dung lượng lưu trữ lớn hơn| Kích thước tệp nhỏ hơn, phù hợp để phát trên các thiết bị âm thanh nhỏ gọn với ít dung lượng lưu trữ |
|**Yêu cầu phần cứng**| Cần thiết bị âm thanh chất lượng cao và dung lượng lưu trữ lớn | Thư viện âm thanh khổng lồ có thể được lưu trong một không gian lưu trữ nhỏ hơn. Thích hợp cho các thiết bị cầm tay, chẳng hạn như máy nghe nhạc hoặc điện thoại di động|
|**Phân phối qua internet**|Không thể phân phối dễ dàng qua internet do kích thước tệp quá lớn |Kích thước tệp nhỏ gọn giúp dễ dàng phân phối qua internet|
|**Khả năng tương thích**|Bộ giải mã nghe nhạc và âm thanh phổ biến nhất tương thích với mọi thiết bị trên hành tinh Tương thích với PC, điện thoại, bộ thu AV, đầu phát blu-ray, thiết bị phát trực tuyến như Roku hoặc Fire TV thế hệ mới|

## Người giới thiệu ##

- [FLAC - Wikipedia](https://vi.wikipedia.org/wiki/FLAC)

