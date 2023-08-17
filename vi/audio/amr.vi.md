{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "file", "extension", "format", "file amr là gì", "music", "amr file format", "amr file","convert file amr to mp3", "phát tệp amr" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp AMR và API có thể tạo, chuyển đổi và mở tệp AMR.",
  "title" :"AMR - Tệp mã hóa đa tốc độ thích ứng",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Tệp AMR là gì?
Tệp có phần mở rộng .amr là định dạng dữ liệu âm thanh có liên quan đến codec âm thanh **Đa tốc độ thích ứng**; bao gồm một codec thoại băng hẹp đa tốc độ mã hóa các tín hiệu băng hẹp ở tốc độ bit 4,75-12,2 kbit/s với chất lượng thoại thu phí bắt đầu từ 7,4 kbit/s; sử dụng thích ứng liên kết để chọn từ một trong tám tốc độ bit khác nhau dựa trên.

## Định dạng tệp AMR
Định dạng tệp AMR sử dụng nhiều kỹ thuật mã hóa, thuật toán ACELP (Dự đoán tuyến tính kích thích mã đại số) là một trong những kỹ thuật tốt nhất; được thiết kế để nén âm thanh nói của con người một cách hiệu quả hơn. AMR được 3GPP đặt làm codec giọng nói hoặc giọng nói tiêu chuẩn vào năm 1999. Định dạng tệp AMR cũng được sử dụng để lưu trữ âm thanh được nói bằng cách sử dụng codec âm thanh **Adaptive Multi-Rate** được nhiều điện thoại thông minh sử dụng để lưu trữ bản ghi bài phát biểu.

### Cấu trúc định dạng tệp
AMR (Đa tốc độ thích ứng) là một định dạng âm thanh; được sử dụng rộng rãi trong các ứng dụng và thiết bị di động khác nhau, điển hình là trong trình phát/ghi âm thanh hoặc trong loại ứng dụng VoIP. AMR có thể được phân loại thành:

1. AMR-NB (Băng tần hẹp)
2. AMR-WB (Băng rộng)

Thông thường, AMR đề cập đến AMR-NB. Định dạng tệp AMR có cấu trúc như sau:

Mỗi tệp AMR chứa tiêu đề 6 byte nhận dạng tệp dưới dạng âm thanh AMR. Tiêu đề này luôn được đặt thành:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Điều này thường tương tự trên tất cả các tệp AMR-NB. Nếu tiêu đề theo tiêu chuẩn, có khả năng tệp bị hỏng và không nên sử dụng. tệp AMR bao gồm toàn bộ số khung âm thanh được đóng gói. Mỗi khung hình này bao gồm 20 mili giây âm thanh. Mỗi khung hình có thể được mã hóa bằng bất kỳ chế độ AMR-NB hợp lệ nào (0-7, 8 SID ở chế độ DTX). Vì, các khung có thể được mã hóa ở các tốc độ bit khác nhau, nên phương pháp điển hình này được gọi là Đa tốc độ thích ứng (AMR).
#### Chế độ AMR
Sau đây là các chế độ AMR khác nhau và tốc độ bit tương ứng của chúng:

|CHẾ ĐỘ| TỶ SUẤT BIT|
---|---|
|0| AMR 4,75 - Mã hóa ở tốc độ 4,75kbit/s|
|1 | AMR 5.15 - Mã hóa ở tốc độ 5,15kbit/s|
|2 | AMR 5.9 - Mã hóa ở tốc độ 5,9kbit/s|
|3 | AMR 6.7 - Mã hóa ở tốc độ 6,7kbit/s|
|4 | AMR 7.4 - Mã hóa ở tốc độ 7,4kbit/s|
|5 | AMR 7,95 - Mã hóa ở tốc độ 7,95kbit/s|
|6 | AMR 10.2 - Mã hóa ở tốc độ 10,2kbit/s|
|7 | AMR 12.2 - Mã hóa ở tốc độ 12,2kbit/s|

Kích thước khung hình của các chế độ AMR tính bằng byte (bao gồm cả byte tiêu đề) được đưa ra dưới đây:

|CMR |CHẾ ĐỘ |KÍCH THƯỚC KHUNG (tính bằng byte )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7,95 |21|

## Người giới thiệu ##

* [Bộ giải mã âm thanh nhiều tốc độ thích ứng - Theo Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [Định dạng tải trọng RTP và Định dạng lưu trữ tệp cho codec âm thanh AMR và AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)

