---
date: 2021-03-21
keywords: alac, định dạng tệp alac, phần mở rộng .alac
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp ALAC và các API có thể tạo và mở tệp ALAC."
title: ALAC - Định dạng tệp Codec âm thanh không mất dữ liệu của Apple
linktitle: ALAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-21
---

## Tệp ALAC là gì?

Định dạng tệp ALAC là Apple Lossless Audio Codec (ALAC) sử dụng bộ chứa QuickTime tuân thủ MPEG-4. Nó được giới thiệu vào năm 2004 dưới dạng định dạng tệp độc quyền, cho đến năm 2011 khi Apple cung cấp nó nguồn mở và miễn phí bản quyền. Định dạng này tương tự như [FLAC](/vi/audio/flac/) (Bộ giải mã âm thanh không mất dữ liệu miễn phí) nhưng cung cấp khả năng nén nhiều hơn một cách tương đối. Nó cung cấp âm thanh thay thế tốt hơn cho [AAC](/vi/audio/aac/) hoặc [MP3](/vi/audio/mp3/). Các tệp âm thanh được mã hóa bằng codec ALAC có thể được mở bằng Apple QuickTime, Apple iTunes và Micrsoft Windows Media Player với codec K-Lite.

## Định dạng tệp ALAC

Các tệp dựa trên codec ALAC là các tệp nhị phân có sẵn dưới dạng [nguồn mở trên GitHub](https://github.com/macosforge/alac) để nhà phát triển tham khảo. Nó chứa các nguồn cho bộ mã hóa và giải mã ALAC. Apple cũng đã cung cấp một tiện ích dòng lệnh, được gọi là `alacconvert`, để đọc và ghi dữ liệu âm thanh vào/từ các tệp Định dạng âm thanh lõi (CAF) và [WAVE](/vi/audio/wav/). Sau đây là một số điểm chính về định dạng tệp ALAC.

1. `Độ sâu bit` - 16, 20, 24 và 32 bit.
1. `Tốc độ mẫu` - Bất kỳ tốc độ lấy mẫu số nguyên tùy ý nào từ 1 đến 384.000 Hz. Tốc độ lý thuyết lên tới 4.294.967.295 (2^32 - 1) Hz có thể được hỗ trợ.
1. `Kích thước gói` - Kích thước gói mặc định mặc định là 4096 khung hình mẫu của âm thanh trên mỗi gói. Kích thước gói khác chắc chắn là có thể. Tuy nhiên, các kích thước gói không mặc định không được đảm bảo sẽ hoạt động bình thường trên tất cả các thiết bị phần cứng hỗ trợ Apple Lossless. Các gói trên 16.384 khung mẫu không được hỗ trợ.
1. `Kênh được hỗ trợ` - Nó hỗ trợ từ một đến tám kênh. Mỗi kênh có thứ tự thông tin như sau.

|Num Chan| Đặt hàng|
|---|---|
|1 |đơn|
|2 |âm thanh nổi (Trái, Phải)|
|3 |MPEG 3.0 B (Giữa, Trái, Phải)|
|4 |MPEG 4.0 B (Trung tâm, Trái, Phải, Xung quanh trung tâm)|
|5 |MPEG 5.0 D (Trung tâm, Trái, Phải, Âm thanh vòm trái, Âm thanh vòm phải)|
|6 |MPEG 5.1 D (Trung tâm, Trái, Phải, Âm thanh vòm trái, Âm thanh vòm phải, Hiệu ứng tần số thấp)|
|7 |Apple AAC 6.1 (Trung tâm, Trái, Phải, Âm thanh vòm bên trái, Âm thanh vòm bên phải, Âm thanh vòm trung tâm, Hiệu ứng tần số thấp)|
|8 |MPEG 7.1 B (Chính giữa, Chính giữa trái, Chính giữa phải, Trái, Phải, Bao quanh trái, Bao quanh phải, Hiệu ứng tần số thấp)|

## Người giới thiệu

* [ALAC - Wikipedia](https://en.wikipedia.org/wiki/Apple_Lossless)
* [Bộ giải mã âm thanh không mất dữ liệu của Apple](https://macosforge.github.io/alac/)
* [macosforge - alac trên GitHub](https://github.com/macosforge/alac)

