---
date: 2020-08-12
keywords: flif, .flif, định dạng file flif, cách mở file flif, đuôi .flif, đuôi flif
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp FLIF
linktitle: FLIF
description: "Tìm hiểu về định dạng tệp FLIF và các API có thể tạo và mở tệp FLIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Tệp FLIF là gì? ##

FLIF (Định dạng hình ảnh không mất dữ liệu miễn phí) là định dạng hình ảnh không mất dữ liệu sử dụng phần mở rộng .flif cho các tệp của nó. FLIF tuyên bố vượt trội hơn [PNG](/vi/image/png/), [WebP]không mất dữ liệu(/vi/image/webp/), BPG không mất dữ liệu và JPEG 2000 không mất dữ liệu về tỷ lệ nén. FLIF sử dụng xen kẽ lũy tiến, do đó bất kỳ tải xuống một phần nào của hình ảnh đều có thể được sử dụng làm mã hóa mất dữ liệu cho toàn bộ hình ảnh.

## Lược Sử ##

FLIF được công bố vào tháng 9 năm 2015 và phiên bản alpha được phát hành vào tháng 10 năm 2015. Vào tháng 9 năm 2016, phiên bản ổn định đầu tiên của FLIF được phát hành.

## Thiết kế FLIF ##

FLIF sử dụng một biến thể của CABAC (Mã hóa số học nhị phân thích ứng theo ngữ cảnh), MANIAC (Mã hóa số học số học gần như không thích ứng siêu dữ liệu) để nén. MANIAC là một thuật toán mã hóa entropy được phát triển bởi Jon Sneyers và Pieter Wuille. Trong MANIAC, ngữ cảnh là các nút của cây quyết định được học một cách linh hoạt tại thời điểm mã hóa. Điều này làm cho mô hình bối cảnh cụ thể hơn về hình ảnh và dẫn đến khả năng nén tốt hơn. FLIF có các tính năng sau:

- Hỗ trợ nén không mất dữ liệu
- Hỗ trợ nén mất dữ liệu với tiền xử lý bộ mã hóa
- Hỗ trợ thang độ xám, RGB và RGBA
- Hỗ trợ độ sâu màu từ 1 đến 16 bit trên mỗi kênh
- Hỗ trợ các tệp xen kẽ và không xen kẽ
- Hỗ trợ giải mã lũy tiến các tệp được tải xuống một phần
- Hỗ trợ hình ảnh động
- Hỗ trợ cấu hình màu ICC nhúng, siêu dữ liệu Exif và XMP
- Có hỗ trợ hạn chế để nén các tệp thô của máy ảnh (RGGB)

## Định dạng tệp FLIF ##

Tệp FLIF có bốn phần sau:

## Tiêu đề chính ##

Tiêu đề chính chứa siêu dữ liệu chính bao gồm chiều rộng, chiều cao, độ sâu màu, số lượng khung hình.

|Loại|Giá trị|Mô tả|
|---|---|---|
|4 byte|"FLIF"|Phép thuật|
|4 bit|3 = ni vẫn; 4 = tôi vẫn; 5 = ni thú; 6 = tôi hoạt hình|Xen kẽ, hoạt hình|
|4 bit|1 = Thang độ xám; 3 = RGB; 4 = RGBA|Số kênh (nb_channels)|
|1 byte|'0','1','2' ('0'=tùy chỉnh)|Số byte trên mỗi kênh (Bpc)|
|varint|chiều rộng-1|Chiều rộng|
|varint|height-1|Chiều cao|
|varint|nb_frames-2 (chỉ khi hoạt ảnh)|Số khung hình (nb_frames)|

## Đoạn siêu dữ liệu ##

Phần này chứa không phải pixel như siêu dữ liệu Exif/XMP, cấu hình màu ICC, v.v. được mã hóa bằng nén DEFLATE. Các khối này được định nghĩa tương tự như các khối PNG với điểm khác biệt là kích thước mâm cặp được mã hóa với số lượng byte thay đổi. Tên của các đoạn có thể là 4 chữ cái (4 byte) hoặc giá trị dưới 32 cho biết một đoạn không bắt buộc.

Sau đây là một ví dụ về mâm cặp tùy chọn:

|Tên đoạn|Mô tả|Nội dung (sau khi giải nén DEFLATE)|
|---|---|---|
|iCCP|Hồ sơ màu ICC|dữ liệu hồ sơ màu ICC thô|
|eXif|Exif metadata|Tiêu đề "Exif\0\0" theo sau là tiêu đề TIFF và dữ liệu EXIF|
|eXmp|Siêu dữ liệu XMP|XMP chứa trong xpacket chỉ đọc không có phần đệm|

### Quy ước đặt tên ###

- **Chữ cái đầu tiên**: Chữ hoa được sử dụng cho các phần quan trọng và chữ thường được sử dụng cho các phần không quan trọng.
- **Second Letter**: Chữ hoa được sử dụng cho phần công khai và chữ thường được sử dụng cho phần riêng tư
- **Chữ cái thứ ba**: Chữ hoa được sử dụng cho các ký tự cần thiết để hiển thị hình ảnh chính xác và chữ thường không quan trọng để hiển thị hình ảnh.
- **Chữ cái thứ tư**: Chữ hoa được sử dụng cho chữ cái có thể được sao chép một cách an toàn. Mâm cặp chữ thường phụ thuộc vào dữ liệu hình ảnh.

## Tiêu đề thứ hai ##

Điều này chứa thông tin liên quan đến mã hóa thực tế của các pixel.

|Loại|Mô tả|Điều kiện|Giá trị mặc định|
|---|---|---|---|
|1 byte|NUL byte (0x00), tên đoạn của dòng bit FLIF16||
|uni_int(1,16)|Số bit trên pixel của các kênh|Bpc == '0': repeat(nb_channels)|8 nếu Bpc == '1', 16 nếu Bpc == '2'|
|uni_int(0,1)|Cờ: alpha_zero|nb_channels > 3|0|
|uni_int(0,100)|Số vòng lặp|nb_frames > 1||
|uni_int(0,60_000)|Độ trễ khung tính bằng mili giây|nb_frames > 1: lặp lại(nb_frames)|
|uni_int(0,1)|Cờ: has_custom_cutoff_and_alpha|||
|uni_int(1,128)|cutoff|has_custom_cutoff_and_alpha|2|
|uni_int(2,128)|số chia alpha|has_custom_cutoff_and_alpha|19|
|uni_int(0,1)|Cờ: has_custom_bitchance|has_custom_cutoff_and_alpha|0|
|?|Bitchance|has_custom_bitchance||
|biến|Biến đổi (xem bên dưới)|||
|uni_int(1) = 0|Bit chỉ thị: thực hiện xong các phép biến đổi|||
|uni_int(0,2)|Dự đoán pixel vô hình|alpha_zero && phạm vi && alpha xen kẽ bao gồm 0||

**Kênh truyền hình**

|Số kênh|Mô tả|
|---|----|
|0|Đỏ hoặc Xám|
|1|Xanh lục|
|2|Xanh da trời|
|3|Alpha|

**Chuyển đổi**

|Loại|Mô tả|
|---|---|
|uni_int(1) = 1|Bit chỉ báo: chưa xong|
|uni_int(0,13)|Định danh chuyển đổi|
|biến|Dữ liệu chuyển đổi (phụ thuộc vào chuyển đổi)|

Chuyển đổi được sử dụng để sửa đổi dữ liệu pixel để nén tốt hơn và để theo dõi các giá trị pixel thực sự xảy ra.

## Dữ liệu pixel ##

Phần này chứa dữ liệu pixel thực tế được mã hóa bằng cách sử dụng mã hóa entropy MANIAC. Các pixel có thể được mã hóa bằng mã hóa xen kẽ hoặc không xen kẽ.

### Phương pháp xen kẽ ###

Trong phương pháp này, các mức thu phóng được xác định. Mức thu phóng 0 được sử dụng cho hình ảnh đầy đủ, mức thu phóng 1 được sử dụng cho tất cả các hàng được đánh số chẵn, mức thu phóng 2 được sử dụng cho tất cả các cột được đánh số chẵn của mức thu phóng 1. Nói cách khác, mọi mức thu phóng 2k được đánh số chẵn là phiên bản được lấy mẫu xuống của mức thu phóng 2k. hình ảnh, ở tỷ lệ 1:2^k. Mức thu phóng được mã hóa từ cao nhất đến thấp nhất.

### Phương pháp không xen kẽ ###

Trong phương pháp này, việc mã hóa các cây MANIAC bắt đầu ngay sau đó là mã hóa các pixel.

## Người giới thiệu ##

- [FLIF - Wikipedia](https://vi.wikipedia.org/wiki/Free_Lossless_Image_Format)
- [FLIF](http://flif.info/)

