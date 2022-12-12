---
date: 2020-08-12
keywords: jxr, .jxr, định dạng file jxr, cách mở file jxr, đuôi .jxr, đuôi jxr
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp JXR
linktitle: JXR
description: "Tìm hiểu về định dạng tệp JXR và các API có thể tạo và mở tệp JXR."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Tệp JXR là gì? ##

JPEG XR (phạm vi mở rộng của JPEG) là định dạng tệp dành cho ảnh chụp có tông màu liên tục. Đây là một tiêu chuẩn nén ảnh tĩnh dựa trên HD Photo do Microsoft phát triển. Nó hỗ trợ cả nén mất dữ liệu và không mất dữ liệu.

## Lược Sử ##

Windows Media Photo lần đầu tiên được Microsoft công bố tại WinHEC 2006. Nó được đổi tên thành HD Photo vào tháng 11 năm 2006. JPEG XR đã được phê duyệt là Tiêu chuẩn quốc tế ISO/IEC 29199-2 vào ngày 19 tháng 6 năm 2009. ITU-T và ISO/IEC đã công bố một kiến nghị đặc tả định dạng (ITU-T T.833 | ISO/IEC 29199-3), bộ kiểm tra sự phù hợp (ITU-T T.834 | ISO/IEC 29199-4) và phần mềm tham chiếu (ITU-T T.835 | ISO /IEC 29199-5) cho JPEG XR sau khi hoàn thành đặc tả mã hóa hình ảnh vào năm 2010. Một báo cáo kỹ thuật mô tả kiến trúc quy trình làm việc cho JPEG XR đã được xuất bản vào năm 2011.

## Thiết kế JPEG XR ##

So với JPEG, JPEG XR cung cấp một số cải tiến bao gồm:

- **Nén tốt hơn**: JPEG XR cung cấp tỷ lệ nén cao hơn.
- **Nén không mất dữ liệu**: JPEG XR hỗ trợ nén không mất dữ liệu.
- **Cấu trúc ô xếp**: Hình ảnh JPEG XR có thể được phân đoạn thành các vùng ô xếp trong đó mỗi vùng có thể được giải mã riêng.
- **Độ chính xác màu cao hơn**: JPEG XR bao gồm chuyển đổi bên trong sang không gian màu YCoCg để hỗ trợ hình ảnh sử dụng không gian màu RGB. JPEG XR cũng hỗ trợ mô hình màu CMYK số nguyên 16 bit cho mỗi thành phần (64 bit cho mỗi pixel). JPEG XR hỗ trợ định dạng màu dấu chấm động chia sẻ số mũ RGBE cho hình ảnh HDR. JPEG XR cũng hỗ trợ mã hóa thang độ xám và màu đa kênh.
- **Bản đồ độ trong suốt**: JPEG XR hỗ trợ kênh alpha cho độ trong suốt.
- **Sửa đổi hình ảnh trong miền nén**: Hình ảnh JPEG XR có thể được chuyển đổi thành mã hóa mất dữ liệu, giảm độ phân giải, cắt xén, lật, xoay và có thể thay đổi toàn bộ cấu trúc ô mà không cần giải mã đầy đủ tệp.
- **Hỗ trợ siêu dữ liệu**: Tệp hình ảnh JPEG XR có thể chứa cấu hình màu ICC để thể hiện màu nhất quán trên nhiều thiết bị. Định dạng này cũng hỗ trợ định dạng siêu dữ liệu Exif và XMP.

## Định dạng vùng chứa ##

Dữ liệu hình ảnh JPEG XR có thể được lưu trữ ở định dạng bộ chứa giống TIFF bằng cách sử dụng bảng thẻ Thư mục tệp hình ảnh (IFT). Tệp JXR chứa các nội dung sau trong thẻ IFD:

- Dữ liệu ảnh: Là dữ liệu ảnh khép kín liền kề.
- Dữ liệu kênh alpha tùy chọn: Nếu có, dữ liệu hình ảnh có thể được nén riêng cho phép hỗ trợ các ứng dụng không hỗ trợ độ trong suốt.
- Metadata
- Siêu dữ liệu XMP tùy chọn
- Siêu dữ liệu Exif tùy chọn

Vì nó dựa trên định dạng TIFF nên nó kế thừa tất cả các giới hạn của định dạng TIFF như giới hạn kích thước tệp 4 GB.

## Người giới thiệu ##

- [JPEG XR - Wikipedia](https://vi.wikipedia.org/wiki/JPEG_XR)

